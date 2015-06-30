# DummyTM - Dummy Threat Modeling Tracking

One-page helper for threat modeling tracking using the advices of the *[Threat Modeling: Designing for Security](http://threatmodelingbook.com/)* book.

![Screenshot](https://i.imgur.com/wIlgmkN.png "Screenshot")

## Framework

It consists of only two files:
* a diagram (html or image) : represents the system to analyze
* an html document editable in-browser : contains the diagram and a threat table


## Workflow

The workflow mocks the one treated on the book and includes
* drawing a simple diagram representing the entities forming the system to analyze, along with trust borders, accompanied by notes and indexes
* compiling a threat table with certain attributes during threat identification.

The page is largely editable and can be printed (on paper or pdf document) to save it.

## Diagram

The diagram can be drawn as you prefer and imported in the html document.
By default it expects an html file named `diagram.html` exported with an UML tool like [draw.io](http://draw.io).

You can define entities as UML Objects, trust borders as Frames, index elements with subscripts and put notes.
Add a brief description directly on the diagram to use it separately and edit the text above to introduce the document.

## Threat Table

Is an editable html5 table. You can add, remove and move rows (thanks to @ashblue for the design) and should be filled like this:

**Diagram Element** : the index of the diagram entity to be considered

**Threat Type** : the [STRIDE](https://www.owasp.org/index.php/Threat_Risk_Modeling#STRIDE) category of the identified threat (a link is provided in-page for consultation)

 **Threat Description** : self-explanatory description

 **Assumption** : a presupposition for how to address the threat (e.g: *It's OK to ignore DoS because there's a backup server*)

 **DREAD Score** : a 0-10 number indicating the risk score according to the [DREAD](https://www.owasp.org/index.php/Threat_Risk_Modeling#DREAD) classification scheme (a link is provided in-page for consultation)

 **Bug Tracking / Vulnerability CVE or CWE** : a bug tracking ID from a bug tracking platform, a CVE ID for Common Vulnerabilities and Exposures or a CWE ID for Common Weakness Enumeration.

 The whole table serves the purpose of tracking and addressing the identified threats and giving an immediate feedback of the threat modeling process.
