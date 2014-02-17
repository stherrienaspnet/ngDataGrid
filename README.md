ngDataGrid
==========

Angular Data Grid

As i wanted to learn Angular.js and need to focus on my requirement, so i decided to build my own data grid directive mainly base on nice feature list provided by ng-grid directive.
I you are interested to a grid directive that provide a way more feature look at the nice directive ng-grid!


**gridOptions:**

```headerRowHeight``` (default: **25**): The height of the header row in pixels.

```rowHeight``` (default: **26**): Row height of rows in grid.

```footerRowHeight``` (default: **32**): Defining the height of the footer in pixels.

```enableSorting``` (default: **true**):  Enables or disables sorting in grid.

```enablePaging``` (default: **false**): Enables the client-side paging feature

```multiSelect``` (default: **true**): Set this to false if you only want one item selected at a time

```keepLastSelected``` (default: **true**): Prevent unselections when in single selection mode

```enableColumnResize``` (default: **false**): Enable or disable resizing of columns

```primaryKey```(default: **undefined**): Primary Key field name used for tracking selector [**required**]

```columnDefs:``` (default: **undefined**): Definitions of columns as an array [], if not defined columns are auto-generated.


**gridOptions.columnDefs Options:**

```field``` (default: **''**): The string name of the property in your data model you want that column to represent.

```displayName``` (default: **''**): Sets the pretty display name of the column.

```visible``` (default: **true**): Whether or not the column is visible by default.

```sortable``` (default: **true**): Whether or not column is sortable.

```resizable``` (default: **true**): Whether or not column is resizable.

```width```(default: **'*'**): Sets the width of the column. Can be a fixed width in pixels as an int (42), string px('42px'), percentage string ('42%'), weighted asterisks (width divided by total number of *'s is all column definition widths)


**dataSource Options:**

```local``` (default: **undefined**): Data being provided localy by the controller.

```remote```(default: **undefined**): Date being provided remotly by ajax call.


**dataSource.remote Options:**

```url``` (default: **undefined**): Url used to retrieve remote data.

```parameters``` (default: **undefined**): Parameters used to retrieve remote data.











