---
id: a49fa920-c87c-457a-9d2e-e406601c22df
title: Api
desc: ''
updated: 1602840671936
created: 1602840671936
stub: false
---

## APIs and API first Approach

- [Rest Api](https://trailhead.salesforce.com/content/learn/modules/api_basics/api_basics_rest)
- [Soap Api](https://trailhead.salesforce.com/content/learn/modules/api_basics/api_basics_soap)
- [Bulk Api](https://trailhead.salesforce.com/content/learn/modules/api_basics/api_basics_bulk)
- [Streaming Api](https://trailhead.salesforce.com/content/learn/modules/api_basics/api_basics_streaming)
- ...
- Limits: Setup->...->API Usage Notifications
-Usage: Setup->...->System Overview

### Rest API
A REST request consists of four components:
- a resource URI
- an HTTP method
- request headers
- a request body

---

### SOAP API

 #### terms:
- Web Services Description Language (WSDL) 
- Web Services Connector (WSC)
Enable it:
- [ ] setup -> API -> and download the file
- [ ] use [SoapUI](https://www.soapui.org/downloads/soapui/) to consume our enterprise WSDL file.

---

### BULK API
[Trailhead bulk API](https://trailhead.salesforce.com/content/learn/modules/api_basics/api_basics_bulk), condensed here:
Based on asynchronous REST.
- [ ] to create a job using the URI: /services/data/v XX.0/jobs/ingest  - and for the POST http method and add this req body:

- [ ] add data to a job (PUT http method): /services/data/v XX.0/jobs/ingest/ jobID/batches where jobID is found on result from workbench Post request.
check header and set to this since importing from CSV: Content-Type: text/csv
The job can be lookup in Setup -> ... -> Bulk Data Load Jobs
You should geta 201 response
- [ ] now we need to let SF know we want to process the data (PATCH http method): go to this URI: /services/data/v XX.0/jobs/ingest/*jobID and add a request body:
{
   "state" : "UploadComplete"
}
and reset Headers to: Content-Type to application/json
You should get a 200 status code.
- [ ] to check any failed results use a GET (http method) at this URI: /services/data/v XX.0/jobs/ingest/*jobID/failedResults

---

### Streaning API

A PushTopic is an sObject that contains the criteria of events you want to listen to.
|NotifyForFields  Value|Description|
|--- |--- |
|All|Notifications are generated for all record field changes, provided the evaluated records match the criteria specified in the WHERE clause.|
|Referenced (default)|Changes to fields referenced in the SELECT and WHERE clauses are evaluated. Notifications are generated for the evaluated records only if they match the criteria specified in the WHERE clause.|
|Select|Changes to fields referenced in the SELECT clause are evaluated. Notifications are generated for the evaluated records only if they match the criteria specified in the WHERE clause.|
|Where|Changes to fields referenced in the WHERE clause are evaluated. Notifications are generated for the evaluated records only if they match the criteria specified in the WHERE clause.|

Plublish platform events:
* Process Builder using the Create a Record action
* Flow using a Create Records element
* Apex EventBus.publish() method
* REST API sobjects resource
* SOAP API create() call

Generic Streaming
Durable Streaming


---
### References:
[Trailhead](https://trailhead.salesforce.com/en/content/learn/modules/api_basics/api_basics_overview)
[Rest API Develoepr Guide](https://developer.salesforce.com/docs/atlas.en-us.224.0.api_rest.meta/api_rest/intro_what_is_rest_api.htm)
[SOAP API Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.224.0.api.meta/api/)
[SOAP Cheatsheet](http://resources.docs.salesforce.com/rel1/doc/en-us/static/pdf/SF_Soap_API_cheatsheet_web.pdf)
[Bulk API](https://developer.salesforce.com/docs/atlas.en-us.224.0.api_asynch.meta/api_asynch/asynch_api_intro.htm)
[Bulk API 2](https://developer.salesforce.com/docs/atlas.en-us.api_bulk_v2.meta/api_bulk_v2/introduction_bulk_api_2.htm)
[convert CSV files online on the fly, drag & drop](https://app.rawgraphs.io/)
