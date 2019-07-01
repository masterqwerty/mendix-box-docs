# Copy File

Copies a file based on given file ID to folder with given folder ID.

## Parameters

* _Required_ **Box file param** - A `BoxFile` object that represents the file to copy. Make sure the `_id` attribute is set.
* _Required_ **Dest box folder** - A `BoxFolder` object that represents the folder you wish to copy your file to. Make sure the `_id` attribute is set.
* **Version** - A string representing the version of the object you wish to copy.
* **Name** - A string representing the name of the file you copied.

## Return Value

A `BoxFile` object that represents the file you just copied.

## Microflow Example

This microflow takes a file ID and folder ID and copies the respective file to the respective folder.

![](../../res/file/copy-file/microflow.png)
