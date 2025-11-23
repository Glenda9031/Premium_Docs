# Tables

Tables are used for tabular data. Back in the day, tables were used for layout purposes, but that is no longer the case. Tables should only be used for tabular data.

The `<table>` element is used to create a table. The `<tr>` element is used to define a row in a table. The `<th>` element is used to define a header cell in a table. The `<td>` element is used to define a data cell in a table.

Here is an example of a simple table:

```html
<table>
  <tr>
    <th>First Name</th>
    <th>Last Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>John</td>
    <td>Doe</td>
    <td>25</td>
  </tr>
  <tr>
    <td>Jane</td>
    <td>Doe</td>
    <td>22</td>
  </tr>
</table>
```

The above code will create a table with two rows and three columns. The first row is a header row, and the second and third rows are data rows.

### `<thead>`, `<tbody>`, and `<tfoot>`

The `<thead>` element is used to group the header content in a table. The `<tbody>` element is used to group the body content in a table. The `<tfoot>` element is used to group the footer content in a table.

Here is an example of a table with a header, body, and footer:

```html
<table>
  <thead>
    <tr>
      <th>First Name</th>
      <th>Last Name</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John</td>
      <td>Doe</td>
      <td>25</td>
    </tr>
    <tr>
      <td>Jane</td>
      <td>Doe</td>
      <td>22</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Footer</td>
    </tr>
  </tfoot>
</table>
```

The above code will create a table with a header row, two data rows, and a footer row.

### `colspan` and `rowspan

The `colspan` attribute is used to specify the number of columns a cell should span. The `rowspan` attribute is used to specify the number of rows a cell should span.

Here is an example of a table with cells that span multiple columns and rows:

```html
<table>
  <tr>
    <th>Name</th>
    <th colspan="2">Telephone</th>
  </tr>
  <tr>
    <td>John Doe</td>
    <td>555 77 854</td>
    <td>555 77 855</td>
  </tr>
  <tr>
    <td>Jane Doe</td>
    <td>555 77 856</td>
    <td>555 77 857</td>
  </tr>
</table>
```

### `<colgroup>` and `<col>`

The `<colgroup>` element is used to group columns in a table. The `<col>` element is used to define the properties of each column in a table.

Here is an example of a table with a column group:

```html
<table>
  <colgroup>
    <col style="background-color: yellow;" />
    <col style="background-color: lightblue;" />
    <col style="background-color: lightgreen;" />
  </colgroup>
  <tr>
    <th>First Name</th>
    <th>Last Name</th>
    <th>Age</th>
  </tr>
  <tr>
    <td>John</td>
    <td>Doe</td>
    <td>25</td>
  </tr>
  <tr>
    <td>Jane</td>
    <td>Doe</td>
    <td>22</td>
  </tr>
</table>
```
