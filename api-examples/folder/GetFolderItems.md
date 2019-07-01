# Get Folder Items

This function will get a list of `BoxItem` entities that represent the individual items inside a folder that you specify.

## Required Values

* **Box folder param** - A `BoxFolder` entity that specifies which folder you want the items of. When you create a `BoxFolder` entity to pass into this microflow, make sure that at least the `_id` property is given.
* **Limit** - An Integer/Long that specifies the limit of items you want the action to return.
* **Offset** - An Integer/Long that specifies which item you want to start listing from.
* **Fields** - A list of `BoxItemFields` entities whose purpose I'm not sure of. Initially I thought it was for which fields the action would return, but I can access fields that I didn't list in that list, so I don't know.

## Microflow example

![](../res/get-folder-items.png)

