# Upload File

This activity uploads a file to box.

## Required Values

* **File to upload** - A `System.FileDocument` object or an object with the `System.FileDocument` specialization. This is the file you will upload.
* **Box folder param** - A `BoxFolder` entity. This is the folder that you are uploading the file to.

## Return Value

A `BoxFile` object that is the file you just uploaded.

## Microflow Example

![](../../res/file/upload-file/microflow.png)