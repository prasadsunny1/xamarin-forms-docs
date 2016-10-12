---
title: Reorder Items
page_title: Reorder Items
position: 
slug: listview-features-reorder-items
---

# Reorder Items

The items reorder feature allows end-users reorder the list view data items. If the feature is enabled, when the user holds on an item, the reorder mode is triggered and the user can move and release the item at the desired position. This will perform reorder operation on the data.

Reorder functionality can be enabled by setting the **IsItemsReorderEnabled** property to `true`.

## Example

This example will demonstrate how to enable the items reorder functionality and style the list view items.

Here is the definition of the list view in Xaml:

<snippet id='listview-gestures-cellswipe-reorderitems-listview'/>

We will set the source in the code behind of the page:

<snippet id='listview-gestures-cellswipe-reorderitems-code'/>

Here is the result:

![](images/listview-gestures-reorder.png)


## See Also