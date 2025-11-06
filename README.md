# Request message specification

This is a very, very simple NIEM 6.0 message specification.  It is much like the examples shown in section 3 of the NIEM 6 Naming and Design Rules.

## Contents

* *model.xsd:*  An XML schema document pile representing the NIEM model for the Request message type
* *model.cmf:* The CMF representation of the same NIEM model
* *model.ttl:*  RDF entailed by the NIEM model, using OWL and RDFS.  *Experimental*
* *message.xsd:* A simplified message schema for validating Request messages in XML format
* *message.json:* A JSON Schema file for validating Request messages in JSON format
* *examples:* Sample messages in XML and JSON format; *msg1.xml* is equivalent to *msg1.json*, etc.

## NIEM 6 features illustrated

* Substitution groups replaced with xs:choice in the message schema
* No object references (`structures:id`, etc.) in the message schema.  You don't get those in NIEM 6 unless you ask for them.

## Tool demonstration

This message specification can be used to demonstrate two open-source developer tools provided by NIEMOpen:

* CMFTool converts model representations between CMF and XSD, and generates message schemas to validate XML and JSON messages.
* NIEMTran converts messages beteween XML and JSON formats

`make clean` removes everything except the XSD model representation and the XML message examples.

`make all` uses CMFTool and NIEMTran to generate everything else.  In a tool demonstration, you can do the same thing, one command at a time.



