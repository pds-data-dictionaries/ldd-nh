# LDD Conventions for This Project

When updating, modifying, or otherwise contributing to the New Horizons namespace,
please observe the following conventions.

## Process

* Before you begin work on a new development task or bugfix, raise an issue for it in the ldd-nh repo
  [Issues list](https://github.com/pds-data-dictionaries/ldd-nh/issues). We will be using this for communication amongst the various developers (typically 
  the local Issues list is *not* used for tracking LDD issues). Reference the local issue in your 
  commit message(s).
* Build and test locally before commiting to the repo. 
  Commiting a new IngestLDD file triggers the autobuild function of the repo. There are limits on the
  resources available for building and testing the namespace in any and all branches. It is not difficult
  to exhaust these resources. Once they are exhausted, no one can build anything in the repo for 24-48 
  hours, which could be a major problem if we're trying to prep a release.
* Note that any unexpected regression test failure will result in all schemas built being removed. It 
  is, therefore, particularly importent to make sure your regression test perform correctly before
  committing a new IngetLDD.


## In PDS4_NH_IngestLDD.xml

### General Notes

* When you begin work on a significant change, please note it in the &lt;comment&gt; at the top
of the file.
* If you change the definition of an existing attribute or class, update the &lt;version_id&gt; of that 
particular element and either replace or add your initials/identifier to the &lt;submitter_name&gt; field.

### Naming Classes and Attributes

It is important that classes and attributes have names that are meaningful to knowledgeable, 
but not expert, users because we expect humans to have to make decisions for directing software
based on the metadata returned - and "metadata" is both the names *and* values of attributes 
and classes 
in our labels. When designinf names for classes and attributes, keep the following in mind:

* You can assume that a human will have ready access to other things in the label for context. 
  That is, you can assume they either know or can easily discover the name and ID of the mission,
  spacecraft, instrument, and even operating modes if they are included elsewhere in the metadata
  (with good supporting definitions, of course).
* You should not assume a human has a SIS open before them, or has memorized the content of such
  a document, for decoding acronyms and abbreviations that refer to details of instrument or 
  spacecraft design, telemetry parsing, commanding, or similar engineering and pipeline 
  processing jargon. These things should be avoided in favor of plain English wherever possible,
  or robust attribute and permissible value definitions when it is not possible.
* Wherever possible, the combination of (attribute name, unit of measure, value) should be
  sufficiently meaningful to a user that the user can make a decision based on the value. So, for
 
      <cal_flag>true</cal_flag>
      
  is not actionable because I don't know for sure what "cal" means, nor if the "true" value 
  indicates that calibration is done, calibration should be done, or if the data I am looking 
  at are for use in calibration. Better names would be:
  
      <calibration_completed>true</calibration_completed>
      <data_are_calibrated>true</data_are_calibrated>
      <calibration_successful>true</calibration_successful>
      
  depending on the context of the flag. As an even more explicit alternative, "_flag" could be
  added to any of the three examples as well, if there is a convention within the namespace to
  indicate all boolean attributes by a "_flag" suffix on their names.
  
  Similarly, something like:
  
        <dettemp>70</dettemp>
              
  is not actionable, whereas something like:
  
        <detector_temperature unit="K">70</detector_temperature>
        
  leaves very little to the imagination.
   
### Attribute Data Types

A number of facets are provided for customizing data types of attributes. Some things to keep in
mind:

* PDS predefines an array of data types, including types for positive and non-negative integers 
  and true/false flags.
  Use the existing type that most closely aligns with the actual range of your data for your
  base type.
* When your data are further constrained than the base type, 
  do add those constraints to your &lt;DD_Attribute&gt;
  definitions. These are enforced by XSD, which is faster at validating its constraints than
  Schematron rules would be. (Permissible value lists are enforced by Schematron rules, however.)
* If you are defining a boolean attribute (i.e., values of literally only 
  "true" and "false" or "TRUE" and "FALSE"), *use the ASCII_Boolean data type*. Do not create 
  a new permissible value list to mimic the boolean type because this masks the true data type from 
  schema-aware software.
* If you are defining a data type that makes use of the &lt;pattern&gt; facet, you should also
  provide regression tests to demonstrate that the regular expressions are properly filtering
  the attribute content.  
  

### Writing &lt;description&gt; and &lt;value_meaning&gt; Definitions

Definitions need to be written in such a way that users can understand them whenever they encounter them.
It is highly unlikely that a user will be reading through the entire schema, or looking at an
interface document, but it is likely that a user 
will be looking at a label. The definition you write 
should provide useful information if, for example, a user 
were to hover
over an attribute name or permissible value long enough to trigger a pop-up containing the definition. In
fact, this is probably the right situation to imagine as you formulate your definitions.

In terms of style:

* Write in complete sentences in standard English.
* Avoid circular definitions ("nh:A_is_B indicates that A is B", e.g.). Permissible values
  can, admittedly, sometimes be impossible to describe otherwise.
* Include the namespace prefix whenever referencing something in the nh: or any other namespace, 
  including the name of the attribute or class you are defining. So,
  for example:

      <description>The nh:arrokoth_constant supplies the...</description>
      
* Do not use acronyms like "TBD" or "TBS" alone to indicate missing information. If it is not 
  possible to provide a complete definition, then preface the definition with the string "[INCOMPLETE]".
  For example: 

      <description>[INCOMPLETE] The nh:spin_rate is TBD.</description>
    
* If you are not confident that a definition or some part of it is correct, preface the description with
  "[CHECK]" so it can be found later for verification. For example:

      <value_meaning>[CHECK] Data were obtained using the blue channel detector. 
      The blue filter covers the range (?) 400-550nm.</value_meaning>

* Do not invent other flag values to indicate missing or uncertain information, or any other 
  odd situation in the IngestLDD file. If you need one, raise it as an Issue *first*.       

### Schematron Rules

Schematron Rules are used to enforce things that the XSD language has difficulty with. This
usually involves tests based on optional elements or specific values existing in the label.

* Write a Schematron rule when certain optional elements must be present in order for the user to
be able to use or understand the data. 
* If you cannot verify code or formulate the XSD to the point of being 
100% certain that dependent
conditions will always be satisified by pipeline output, write a Schematron rule to enforce it.
* There is no need to write a Schematron rule for anything that can be enforced by a structural
  constraint in XSD.
* XSD validation is **much** more efficient than Schematron validation. 
  Use XSD validation whenever possible.
* Do not use Schematron rules to enforce constraints that could have been included in a 
  &lt;DD_Attribute&gt; definition.
* Every Schematron rule you right should be accompanied by at least one and generally two 
  regression tests. 

## Regression Tests

* There's not a lot of point in writing regression tests for most XSD changes.
The notable exception to this is *anything* involving an *xs:choice* list.
It is possible, and generally likely, that choice lists will allow invalid combinations of
selections to be present in the label. In general, they should be avoided for that reason alone.
If a choice list is, for some reason, required, several regression test scenarios need to be
included to demonstrate that invalid repetition and omission of elements is being effectively
identified and prohibited.
* If a class is defined with many optional elements (that is, attributes and/or classes), 
  a Schematron rule might be required to 
  ensure that either a minimal set of elements, a compatible set of elements, 
  or both are present in any given label.
* As noted above, every Schematron rule you right should be accompanied by at least one 
  and generally two 
  regression tests: One that demonstrates that no error is signaled when the correct situation
  occurs in the label; and one that demonstrates that the Schematron check, and only the Schematron
  check, signals an error when an incorrect situation arises that only Schematron can detect. 


## Documentation

New classes, attributes, and permissible values may need to be explicitly mentioned in the
namespace documentation, depending on their level. 

### pds-data-dictionaries.github.io/ldd-nh

The goal of the 
https://pds-data-dictionaries.github.io/ldd-nh documentation site is to provide a relatively
high-level overview of the entire NH namespace. The detailed documentation for each and every
class, attribute, and permissible value is generated (semi)automatically on release - so it
is not necessary to document *every* change. Use the existing documentation as a guide:

* If you are adding a new instrument class, for example, that is at the same nesting level
  as another class for the same or a different instrument, then add it to the user documentation
  following the model of the existing class.
* If you have modified a class that is already documented, update the documentation.
* If you have added a new permissible value to a list for which the existing values are all 
  listed in the documentation, add the new value information.

Some additional places to check for needed updates:

* If you've added a high-level class (akin to &lt;nh:MVIC_Calibration_Information&gt;, you'll 
  need to update both the *Overview* page and the *Organization of Classes and Attributes* page.
* All new classes and attributes need to be represented in the *New Horizons Mission Namespace 
  Outline* page.
* Most new and modified classes will need to be represented either by a new mock-up label in the 
  *EXAMPLES* list, or by a change to an existing label.
  
### ChangeLog.md

This file, located in the root of the repo, should be updated whenever a change is made, and
could be helpful in coordinating simultaneous editing by multiple parties.

* Note intended changes even before you start the editing. Include the issue number for
  reference.
* Doesn't have to be pretty - we'll clean up and 
  consolidate redundant or unnecessary details before release.
