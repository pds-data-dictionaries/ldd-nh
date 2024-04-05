# LDD Conventions for This Project

When updating, modifying, or otherwise constributing to the New Horizons namespace,
please observe the following conventions.

## Process

* Before you begin work on a new development task or bugfix, raise an issue for it in the ldd-nh repo
  "Issues" list. We will be using this for communication amongst the various developers (typically 
  the local "Issues" list is *not* used for tracking LDD issues). Reference the local issue in your 
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
 
### Writing &lt;description&gt; and &lt;value_meaning&gt; Content

Definitions need to be written in such a way that users can understand them whenever they encounter them.
It is highly unlikely that a user will be reading through the entire schema, but it is likely that a user 
will be looking at a label. The description should provide useful information if, for example, a user 
were to hover
over an attribute name or permissible value long enough to trigger a pop-up containing the definition. In
fact, this is probably the right situation to image as you formulate your definitions.

In terms of style:

* Write in complete sentences in standard English.
* Include the namespace prefix whenever referencing something in the nh: or any other namespace, including
* the name of an attribute or class you are defining. So,
  for example, "&lt;description&gt;The nh:arrokoth_constant supplies the...&lt;/description&gt;".
* Do not use acronyms like "TBD" or "TBS" alone to indicate missing information. If it is not 
  possible to provide a complete definition, then preface the definition with the string "[INCOMPLETE]".
  For example: 

        ``&lt;description&gt;[INCOMPLETE] The nh:spin_rate is TBD.&lt;/description&gt;``
    
* If you are not confident that a definition or some part of it is correct, preface the description with
  "[CHECK]" so it can be found later for verification. For example:

        ``<value_meaning>[CHECK] Data were obtained using the blue channel detector. The blue
          filter covers the range (?) 400-550nm.</value_meaning>``

* Do not invent other flag values.       

### Schematron Rules

Schematron Rules are used to enforce things that the XSD language has difficulty with. This
usually involved tests based on optional elements or specific value existing in the label.
Write a Schematron rule when certain optional elements must be present in order for the user to
be able to use a label. If you cannot verify code or formulate the XSD to the point of being 
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
The notable exception to this is anything involving an *xs:choice* list.
It is possible, and generally likely, that choice lists will allow invalid combinations of
selections to be present in the label. In general, they should be avoided for that reason alone.
If a choice list is, for some reason, required, several regression test scenarios need to be
included to demonstrate that invalid repetition and omission of elements is being effectively
constrained.
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
* If you have added a new permissible value to a list for which the existing value are all 
  documented, add the new value information to the documentation.

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
  reference and identify yourself as the assignee for the particular task.
* Doesn't have to be pretty - we'll clean up and 
  consolidate redundant or unnecessary details before release.
