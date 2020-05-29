## Overview

> In this section we will test the get_settings algorithm for laser storage using the postman tool, also requests can be executed in any browser

## Methods

> the get_settings algorithm is called by the access adapter when a submission is made, it receives as parameters the storages, the keys and the method.
> For this algorithms there are 5 methods, and for each one the algorithm returns a series of parameters necessary for the work of the adapter.
> The following points show the different requests with the expected responses.

### Get File

##### Request

```
https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche&keys=["NULLISLAND","CAP","REC20-00000-00092"]&method=Get File
```

##### Response

> {
> "StatusCode":200,
> "StatusDescription":"success",
> "Data":{
> "settings":{"url":"http://connect.velosimo.com:3081/laserfiche/api/documents/{{id}}",
> "path":"/AccelaTest/BLD20-00176/"
> },
> "credentials":{
> "username":"velosimo",
> "password":"v\$!"Elosimo,
> "server":"http://laserfiche.velosimo.com",
> "repository":"velosimo",
> "license":""
> },
> "mappings":{
> "templateId":52,
> "templateName":"Professional test template",
> "templateFields":[{
>
> "fieldId":15,
> "fieldName":"First Name",
> "fieldValue":"recordId",
> "fieldType":"String",
> "isAssigned":false}]}}}

### Get Files

##### Request

```
https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche&keys=["NULLISLAND","CAP","REC20-00000-00092"]&method=Get Files
```

##### Response

> {"StatusCode":200,"StatusDescription":"success","Data":{"settings":{
> "url":"http://connect.velosimo.com:3081/laserfiche/api/documents",
> "path":"/AccelaTest/BLD20-00176/"},"credentials":{"username":"velosimo","password":"v\$Elosimo!",>"server":"http://laserfiche.velosimo.com","repository":"velosimo","license":""},"mappings":{"templateId":52,"templateName":"Professional test template","templateFields":[{"fieldId":15,"fieldName":"First Name","fieldValue":"recordId","fieldType":"String","isAssigned":false}]}}}

### Delete File

##### Request

```
https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche&keys=["NULLISLAND","CAP","REC20-00000-00092"]&method=Delete File
```

##### Response

> {"StatusCode":200,"StatusDescription":"success","Data":{"settings":{"url":"http://connect.velosimo.com:3081/laserfiche/api/documents/{{id}}","path":"/AccelaTest/BLD20-00176/"},"credentials":{"username":"velosimo","password":"v$Elosimo!","server":"http://laserfiche.velosimo.com","repository":"velosimo","license":""},"mappings":{"templateId":52,"templateName":"Professional test template","templateFields":[{"fieldId":15,"fieldName":"First Name","fieldValue":"recordId","fieldType":"String","isAssigned":false}]}}}

### Update File

##### Request

```
https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche&keys=["NULLISLAND","CAP","REC20-00000-00092"]&method=Update File
```

##### Response

> {"StatusCode":200,"StatusDescription":"success","Data":{"settings":{"url":"http://connect.velosimo.com:3081/laserfiche/api/documents/{{file_id}}","path":"/AccelaTest/BLD20-00176/"},"credentials":{"username":"velosimo","password":"v$Elosimo!","server":"http://laserfiche.velosimo.com","repository":"velosimo","license":""},"mappings":{"templateId":52,"templateName":"Professional test template","templateFields":[{"fieldId":15,"fieldName":"First Name","fieldValue":"recordId","fieldType":"String","isAssigned":false}]}}}

### Create File

##### Request

```
https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche&keys=["NULLISLAND","CAP","REC20-00000-00092"]&method=Create File
```

##### Response

> {"StatusCode":200,"StatusDescription":"success","Data":{"settings":{"url":"http://connect.velosimo.com:3081/laserfiche/api/documents","path":"/AccelaTest/BLD20-00176/"},"credentials":{"username":"velosimo","password":"v$Elosimo!","server":"http://laserfiche.velosimo.com","repository":"velosimo","license":""},"mappings":{"templateId":52,"templateName":"Professional test template","templateFields":[{"fieldId":15,"fieldName":"First Name","fieldValue":"recordId","fieldType":"String","isAssigned":false}]}}}
