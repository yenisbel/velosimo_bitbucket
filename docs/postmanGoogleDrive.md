### Get File

#### Sample Request

GET/ Get File https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=googledrive

(`https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=googledrive&keys=["NULLISLAND","CAP","REC20-00000-00092"]&method=Get File`)

#### Response

```json
{
  "StatusCode": 200,
  "StatusDescription": "success",
  "Data": {
    "settings": {
      "url": "https://www.googleapis.com/drive/v3/files/{{file_id}}",
      "path": "/29-04-2020/RES-NEW-20-000001/",
      "parent": "11IrFoS585JGg4oPpUbLH43eRJK6kGxCo"
    },
    "credentials": {
      "access_token": "ya29.a0AfH6SMA772g1nSvYneOlXCIvA2QEHO9Se8jJQMyNx5T36ThpPv7bjI0iGr9Pakhhp6zIIob1rNS3EI9kymBobgjOZbb056LvYJQ8n9zAgPLg-I79SUhfEMQhT8hVLJUz8Ga7w_G0DYJZ9EadbBmvHzk688BObHnrvdWifA",
      "refresh_token": null
    },
    "mappings": {},
    "logs": { "url": "https://dev.velosimo.io/app/dev-edms/logging" }
  }
}
```

### Get Files

#### Sample Request

GET/ Get Files https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=googledrive

(`https://dev.velosimo.io/app/dev-edms/settings?storage=googledrive&keys=["velosimo","CAP","20CAP-00000-00002"]&method=Get Files`)

**`keys` ["NULLISLAND","CAP","REC20-00000-00092"]**

#### Response

```json
{
  "StatusCode": 200,
  "StatusDescription": "success",
  "Data": {
    "settings": {
      "url": "https://www.googleapis.com/drive/v3/files",
      "path": "/29-04-2020/RES-NEW-20-000001/",
      "parent": "11IrFoS585JGg4oPpUbLH43eRJK6kGxCo"
    },
    "credentials": {
      "access_token": "<your_access_token>",
      "refresh_token": null
    },
    "mappings": {},
    "logs": { "url": "https://dev.velosimo.io/app/dev-edms/logging" }
  }
}
```

### Delete File

#### Sample Request

DELETE/ Delete File https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=googledrive

(`https://dev.velosimo.io/app/dev-edms/settings?storage=googledrive&keys=["velosimo","CAP","20CAP-00000-00002"]&method=Delete File`)

**`keys`["NULLISLAND","CAP","REC20-00000-00092"]**

#### Response

```json
{
  "StatusCode": 200,
  "StatusDescription": "success",
  "Data": {
    "settings": {
      "url": "https://www.googleapis.com/drive/v3/files/{{file_id}}",
      "path": "/29-04-2020/RES-NEW-20-000001/",
      "parent": "11IrFoS585JGg4oPpUbLH43eRJK6kGxCo"
    },
    "credentials": {
      "access_token": "<your_access_token>",
      "refresh_token": null
    },
    "mappings": {},
    "logs": { "url": "https://dev.velosimo.io/app/dev-edms/logging" }
  }
}
```

### Update File

#### Request

PUT/ Update File https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=googledrive

(`https://dev.velosimo.io/app/dev-edms/settings?storage=googledrive&keys=["velosimo","CAP","20CAP-00000-00002"]&method=Update File`)

**`keys` ["NULLISLAND","CAP","REC20-00000-00092"]**

#### Response

```json
{
  "StatusCode": 200,
  "StatusDescription": "success",
  "Data": {
    "settings": {
      "url": "https://www.googleapis.com/upload/drive/v3/files/{{file_id}}",
      "path": "/29-04-2020/RES-NEW-20-000001/",
      "parent": "11IrFoS585JGg4oPpUbLH43eRJK6kGxCo"
    },
    "credentials": {
      "access_token": "<your_access_token>",
      "refresh_token": null
    },
    "mappings": {},
    "logs": { "url": "https://dev.velosimo.io/app/dev-edms/logging" }
  }
}
```

### Create File

#### Request

POST/ Create File https://dev.velosimo.io/app/velosimoaccela-edms/settings?storage=googledrive

(`https://dev.velosimo.io/app/dev-edms/settings?storage=googledrive&keys=["velosimo","CAP","20CAP-00000-00002"]&method=Create File`)

**`keys` ["NULLISLAND","CAP","REC20-00000-00092"]**
`

#### Response

```json
{
  "StatusCode": 200,
  "StatusDescription": "success",
  "Data": {
    "settings": {
      "url": "https://www.googleapis.com/drive/v3/files",
      "path": "/29-04-2020/RES-NEW-20-000001/",
      "parent": "11IrFoS585JGg4oPpUbLH43eRJK6kGxCo"
    },
    "credentials": {
      "access_token": "<your_access_token>",
      "refresh_token": null
    },
    "mappings": {},
    "logs": { "url": "https://dev.velosimo.io/app/dev-edms/logging" }
  }
}
```
