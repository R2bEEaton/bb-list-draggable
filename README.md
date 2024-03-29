# BB-List-Draggable
This is the read me for the draggable/sortable list plugin.

# Description
With this plugin you are able to order a list by dragging the different elements around in the browser.

## Features
* Reorder a list by dragging

## Instructions
* Create a table with the following fields.
    * A label field, which can be named whatever you want
    * An order field, which must be numeric and can be named whatever you want
    * Choose the label and order field as appropriate from the element's settings
    * The table can have any additional fields, but at least the first two are required

    ### Additional Notes
    * Change the sort direction via the settings
    * Make sure that the order column contains unique integers as the sorting depends on it
    * To add a row to the list, I would recommend first performing a query to get the highest value in the order column and setting the new row to that + 1. This means new rows will show up at one end of the list, depending on how you have it sorted. Otherwise, the ordering may break.

## Demo
As explained in the Disclaimer section, this is how I would recommend setting up the plugin visually for your users.
![list-draggable-demo](https://github.com/R2bEEaton/bb-kanban-draggable/assets/34921506/54985b26-7b91-4b18-8f24-4f8fe4e38292)

## Disclaimer
* Most of this plugin was copied/modified from the column reordering capability of @ConorWebb96's [Kanban plugin](https://github.com/ConorWebb96/bb-kanban-draggable/blob/main/src/components/ColumnsSort.svelte)
* I initially wanted to make the sorting work directly in a table, but I feel that this is better. You can display the sorted data with a table and have a "reorder" button that opens a sidebar with the Draggable List element. Then, use an [Interval](https://github.com/MartinPicc/budibase-interval-plugin) (one of my favorite plugins) to refresh a dataprovider on the table periodically. If you use an external database, you can get away with refreshing pretty often. Or, have a button to close the sidebar that also refreshes the data provider for your table.
