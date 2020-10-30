---
id: 5107408e-dfa8-4d7f-928e-f6758731e5a1
title: Soapcallout
desc: ''
updated: 1603093603639
created: 1603093603639
stub: false
---
# Soapcallout

Integration : [[computer-science.lang.apex.integration]]

Apex can also make callouts to SOAP web services using XML but the process can be painful.
Fortunately, we have tools to make the process easier.
WSDL2Apex automatically generates Apex classes from a WSDL document. 

- From Setup -> Apex Classes -> Click Generate from WSDL.
- save a .xml file you'll use
- Click Parse WSDL
- Click Generate Apex code (the wizard generate for us the Apex code)

- [ ] create the class
- [ ] create the mock class (implement the interface mock)
- [ ] create the test class 


---

References:
#WSDL is a xml format
[Trailhead SOAP callout](https://trailhead.salesforce.com/content/learn/modules/apex_integration_services/apex_integration_soap_callouts)
[JSON2Apex](https://json2apex.herokuapp.com/) (parser)
