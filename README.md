ngDataGrid
==========

Angular Data Grid

![alt tag](https://raw.github.com/stherrienaspnet/ngDataGrid/master/ngDataGrid/ngDataGridDemo.png)

Since I wanted to learn Angular.js, but still needed to focus on the requirements of my job’s project, I decided to build my own simple data grid directive mainly based on the features provided by ng-grid (http://angular-ui.github.io/ng-grid/). If you are interested in a directive with way more features, you can check out ng-grid.

**One commun mistake is to forget to specify [heigh] and [width] parameters to this directive who can lead to layout issue**.

*If you plan to mix fixed (px) and variable width (%), make sure variable summation is lower than 100%.


**gridOptions:**

```headerClass``` (default: **''**): Appends a css class for the column header.

```headerRowHeight``` (default: **25**): The height of the header row in pixels.

```rowHeight``` (default: **25**): Row height of rows in grid.

```showFooter``` (default: **false**): Show or hide the footer the footer is disabled by default.

```footerTemplate``` (default: **''**): Define a footer template for customization.

```footerRowHeight``` (default: **32**): Defining the height of the footer in pixels.

```enableSorting``` (default: **true**):  Enables or disables sorting in grid.

```enablePaging``` (default: **false**): Enables the client-side paging feature

```multiSelect``` (default: **true**): Set this to false if you only want one item selected at a time

```keepLastSelected``` (default: **true**): Prevent unselections when in single selection mode

```enableColumnResize``` (default: **false**): Enable or disable resizing of columns

```primaryKey```(default: **undefined**): Primary Key field name used for tracking selector [**required**]

```columnDefs``` (default: **undefined**): Definitions of columns as an array [], if not defined columns are auto-generated.

```headerCellTemplate``` : Sets the template for the column header cell.

(default: 
**```<span ng-show="!isSortable(column)">{{ column.displayName }}</span>```**
**```<a ng-show="isSortable(column)" ng-click="sortBy(column)">{{ column.displayName }}```**
**```<span class="ng-data-grid-sort-icon"></span></a><span ng-show="isResizable(column)"```**
**```ng-style="{height:headerRowHeight-10}" class="ng-data-grid-column-resizer"```**
**```ng-mousedown="onMousedown($event, $index)"></span>```**)

**gridOptions.columnDefs Options:**

```cellClass``` (default: **''**): Appends a css class for the column cells.

```cellStyle``` (default: **undefined**): Allow to apply style to a cell using a function of object. 

  Usage sample:
  
    cellStyle: { color: '#FF00FF', backgroundColor: '#00FF00'}
    OR
    cellStyle: alarmColumnCustomStyle
    function alarmColumnCustomStyle(row) {
      return { color: '#FF00FF', backgroundColor: '#00FF00'};
    }
           


```field``` (default: **''**): The string name of the property in your data model you want that column to represent.

```displayName``` (default: **''**): Sets the pretty display name of the column.

```visible``` (default: **true**): Whether or not the column is visible by default.

```sortable``` (default: **true**): Whether or not column is sortable.

```resizable``` (default: **true**): Whether or not column is resizable.

```excludeFromSelection```(default: **false**): Whether or not column is exlude from selection.

```cellTemplate``` (default: **{{row[column.field]}}**): Sets the cell template for the column.

```width``` (default: **"*"**): Sets the width of the column. Can be a fixed width in pixels ('42px'), percentage string ('42%'), weighted asterisks (width divided by total number of star 's is all column definition widths). 


**dataSource Options:**

```local``` (default: **undefined**): Data being provided localy by the controller.

```remote```(default: **undefined**): Date being provided remotly by ajax call.


**dataSource.remote Options:**

```url``` (default: **undefined**): Url used to retrieve remote data.

```parameters``` (default: **undefined**): Parameters used to retrieve remote data.

```pooling``` (default: **false**): Whether or not the pooling is active.

```poolingRate``` (default: **30000**): Polling rate used to retrieve remote data when pooling is active.

```autoStart``` (default: **false**): Start poolling automatically.


**gridOptions.pagingOptions Options:**

```pageSizes``` (default: **[250, 500, 1000]**): List of available page sizes.

*Page size selector is visible when there is multiple size defined into [pageSizes] parameter.

```pageSize``` (default: **250**): List of available page sizes.

```currentPage``` (default: **1**):  Current page.

```autoPage``` (default: **false**):  Automatic page size calculation base on available space for rows. This will override pageSize value.


**gridOptions.sortOptions Options:**

```direction``` (default: **''**):  Sort directions ['asc', 'desc'], directions are case-insensitive

```field``` (default: **''**):  Sort field, there is no support for multiple field yet!


**Methods:**

```deselectAll()```: Deselect all rows.

```selectAll()```: Select all rows.

```forceRefresh()```: Force data source refresh.

```startPooling()```: Start data source pooling.

```stopPooling()```: Stop data source pooling.

```getTotalItemsCount()```: Return total items count.

```getSelectedItems()```: Return selected items.
