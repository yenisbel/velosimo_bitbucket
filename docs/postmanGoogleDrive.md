## Overview

In this section we will test the **`get_settings algorithm`** for <b>Google Drive</b> storage using the <b>Postman</b> tool, also the requests can be executed in any browser.

## Methods

**`get_settings algorithm`** , is called by the access adapter when a submission is made, it receives as **`parameters`** the storages, the keys and the method.

For this algorithm there are five **`methods`**, and for each one the algorithm returns a series of **`parameters`** necessary for the work of the adapter.

> The following points show the different requests with the expected responses.

### Get File

#### Sample Request

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

GET/ Get File https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=laserfiche

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

**`keys` ["NULLISLAND","CAP","REC20-00000-00092"]**
`

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
