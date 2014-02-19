ngDataGrid
==========

Angular Data Grid

Since I wanted to learn Angular.js, but still needed to focus on the requirements of my job’s project, I decided to build my own simple data grid directive mainly based on the features provided by ng-grid (http://angular-ui.github.io/ng-grid/). If you are interested in a directive with way more features, you can check out ng-grid.

**One commun mistake is to forget to specify a width parameter to this directive who can lead to layout issue**

**gridOptions:**

```headerClass``` (default: **''**): Appends a css class for the column header.

```headerRowHeight``` (default: **25**): The height of the header row in pixels.

```rowHeight``` (default: **26**): Row height of rows in grid.

```footerRowHeight``` (default: **32**): Defining the height of the footer in pixels.

```enableSorting``` (default: **true**):  Enables or disables sorting in grid.

```enablePaging``` (default: **false**): Enables the client-side paging feature

```multiSelect``` (default: **true**): Set this to false if you only want one item selected at a time

```keepLastSelected``` (default: **true**): Prevent unselections when in single selection mode

```enableColumnResize``` (default: **false**): Enable or disable resizing of columns

```primaryKey```(default: **undefined**): Primary Key field name used for tracking selector [**required**]

```columnDefs``` (default: **undefined**): Definitions of columns as an array [], if not defined columns are auto-generated.


**gridOptions.columnDefs Options:**

```cellClass``` (default: **''**): Appends a css class for the column cells.

```field``` (default: **''**): The string name of the property in your data model you want that column to represent.

```displayName``` (default: **''**): Sets the pretty display name of the column.

```visible``` (default: **true**): Whether or not the column is visible by default.

```sortable``` (default: **true**): Whether or not column is sortable.

```resizable``` (default: **true**): Whether or not column is resizable.

```width``` (default: **"*"**): Sets the width of the column. Can be a fixed width in pixels ('42px'), percentage string ('42%'), weighted asterisks (width divided by total number of star 's is all column definition widths). 


**dataSource Options:**

```local``` (default: **undefined**): Data being provided localy by the controller.

```remote```(default: **undefined**): Date being provided remotly by ajax call.


**dataSource.remote Options:**

```url``` (default: **undefined**): Url used to retrieve remote data.

```parameters``` (default: **undefined**): Parameters used to retrieve remote data.

```pooling``` (default: **false**): Whether or not the pooling is active.

```poolingRate``` (default: **30000**): Polling rate used to retrieve remote data when pooling is active.


**gridOptions.pagingOptions Options:**

```pageSizes``` (default: **[250, 500, 1000]**): List of available page sizes.

```pageSize``` (default: **250**): List of available page sizes.

```currentPage``` (default: **1**):  Current page.









