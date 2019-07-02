# Upload File Version

Upload a new version for an existing file. This function is broken as is, and you will need to fix it if you wish to use it. To fix this one, go to the project directory, and find `javasource/boxconnector/actions/UploadFileVersionCall.java`. Then on line 64, change
```java
postMethod.setRequestHeader("Authorization", "Bearer " + this.AccessTokenParam);
```
to
```java
postMethod.setRequestHeader("Authorization", "Bearer " + this.AccessTokenParam.gettoken());
```
The variable `AccessTokenParam` is an object that contains the access token, but isn't the access token itself, so if this isn't changed you will get a 401 error, or `Authentication error` (See [Short Errors](../../troubleshooting/ShortErrors.md))

## Parameters

* _Required_ **Box file param** - A `BoxFile` object representing the file you are uploading a new version for. Make sure the `_id` attribute is set.
* _Required_ **File to upload** - A `System.FileDocument` object or a specialization of `System.FileDocument`. This is the actual file you are uploading.

## Return Value



## Microflow Example

