### Get File

#### Sample Request

GET/ Get File https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche

`https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche&keys=["NULLISLAND","CAP","REC20-00000-00092"]&method=Get File`

#### Response

```json
{
  "StatusCode": 200,
  "StatusDescription": "success",
  "Data": {
    "settings": {
      "url": "http://connect.velosimo.com:3081/laserfiche/api/documents/{{id}}",
      "path": "/AccelaTest/BLD20-00176/"
    },
    "credentials": {
      "username": "<your_username>",
      "password": "<your_password>",
      "server": "http://laserfiche.velosimo.com",
      "repository": "velosimo",
      "license": ""
    },
    "mappings": {
      "templateId": 52,
      "templateName": "Professional test template",
      "templateFields": [
        {
          "fieldId": 15,
          "fieldName": "First Name",
          "fieldValue": "recordId",
          "fieldType": "String",
          "isAssigned": false
        }
      ]
    }
  }
}
```

### Get Files

#### Sample Request

GET/ Get Files https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche

`https://dev.velosimo.io/app/dev-edms/settings?storage=laserfiche&keys=["velosimo","CAP","20CAP-00000-00002"]&method=Get Files`

**`keys` ["NULLISLAND","CAP","REC20-00000-00092"]**

#### Response

```json
{
  "StatusCode": 200,
  "StatusDescription": "success",
  "Data": {
    "settings": {
      "url": "http://connect.velosimo.com:3081/laserfiche/api/documents",
      "path": "/AccelaTest/BLD20-00176/"
    },
    "credentials": {
      "username": "<your_username>",
      "password": "<your_password>",
      "server": "http://laserfiche.velosimo.com",
      "repository": "velosimo",
      "license": ""
    },
    "mappings": {
      "templateId": 52,
      "templateName": "Professional test template",
      "templateFields": [
        {
          "fieldId": 15,
          "fieldName": "First Name",
          "fieldValue": "recordId",
          "fieldType": "String",
          "isAssigned": false
        }
      ]
    }
  }
}
```

### Delete File

#### Sample Request

DELETE/ Delete File https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche

`https://dev.velosimo.io/app/dev-edms/settings?storage=laserfiche&keys=["velosimo","CAP","20CAP-00000-00002"]&method=Delete File`

**`keys`["NULLISLAND","CAP","REC20-00000-00092"]**

#### Response

```json
{
  "StatusCode": 200,
  "StatusDescription": "success",
  "Data": {
    "settings": {
      "url": "http://connect.velosimo.com:3081/laserfiche/api/documents/{{id}}",
      "path": "/AccelaTest/BLD20-00176/"
    },
    "credentials": {
      "username": "<your_username>",
      "password": "<your_password>",
      "server": "http://laserfiche.velosimo.com",
      "repository": "velosimo",
      "license": ""
    },
    "mappings": {
      "templateId": 52,
      "templateName": "Professional test template",
      "templateFields": [
        {
          "fieldId": 15,
          "fieldName": "First Name",
          "fieldValue": "recordId",
          "fieldType": "String",
          "isAssigned": false
        }
      ]
    }
  }
}
```

### Update File

#### Request

PUT/ Update File https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche

`https://dev.velosimo.io/app/dev-edms/settings?storage=laserfiche&keys=["velosimo","CAP","20CAP-00000-00002"]&method=Update File`

**`keys` ["NULLISLAND","CAP","REC20-00000-00092"]**

#### Response

```json
{
  "StatusCode": 200,
  "StatusDescription": "success",
  "Data": {
    "settings": {
      "url": "http://connect.velosimo.com:3081/laserfiche/api/documents/{{file_id}}",
      "path": "/AccelaTest/BLD20-00176/"
    },
    "credentials": {
      "username": "<your_username>",
      "password": "<your_password>",
      "server": "http://laserfiche.velosimo.com",
      "repository": "velosimo",
      "license": ""
    },
    "mappings": {
      "templateId": 52,
      "templateName": "Professional test template",
      "templateFields": [
        {
          "fieldId": 15,
          "fieldName": "First Name",
          "fieldValue": "recordId",
          "fieldType": "String",
          "isAssigned": false
        }
      ]
    }
  }
}
```

### Create File

#### Request

POST/ Create File https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche

`https://dev.velosimo.io/app/dev-edms/settings?storage=laserfiche&keys=["velosimo","CAP","20CAP-00000-00002"]&method=Create File`

**`keys` ["NULLISLAND","CAP","REC20-00000-00092"]**

#### Response

```json
{
  "StatusCode": 200,
  "StatusDescription": "success",
  "Data": {
    "settings": {
      "url": "http://connect.velosimo.com:3081/laserfiche/api/documents",
      "path": "/AccelaTest/BLD20-00176/"
    },
    "credentials": {
      "username": "<your_username>",
      "password": "<your_password>",
      "server": "http://laserfiche.velosimo.com",
      "repository": "velosimo",
      "license": ""
    },
    "mappings": {
      "templateId": 52,
      "templateName": "Professional test template",
      "templateFields": [
        {
          "fieldId": 15,
          "fieldName": "First Name",
          "fieldValue": "recordId",
          "fieldType": "String",
          "isAssigned": false
        }
      ]
    }
  }
}
```
