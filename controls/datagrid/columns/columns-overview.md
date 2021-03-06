---
title: Overview
page_title: Columns Overview
position: 0
slug: datagrid-columns-overview
---

# Columns Overview #

You can add columns in your RadDataGrid by working with the Columns collection of the control. Generally, there are three approaches that you can take to define differrent columns:

* **Manually**: by adding columns to the *RadDataGrid.Columns* collection
* **Automatically**: by setting *RadDataGrid.AutoGenerateColumns="True"*
* **Mixed**: by adding columns to the *RadDataGrid.Columns* collection and also set *RadDataGrid.AutoGenerateColumns="True"*

The **RadDataGrid** control provides the following type of columns:

* **Template Column**: Represents a column that uses a DataTemplate to describe the content of each associated grid cell.
* **Boolean Column**: A special DataGridTypedColumn implementation that presents boolean data.
* **Date Column:** An extended DataGridTextColumn that presents data of type DateTime. 
* **Numerical Column**: Represents an extended DataGridTextColumn that presents numerical data(int and double types). 
* **Text Column**: Represents a column that converts the content of each associated cell to a System.String object.
* **Time Column**: Represents an extended DataGridTextColumn that presents the **TimeOfDay** of a **DateTime** type. 
* **Picker Column**: Represents an extended DataGridTextColumn that uses a Picker editor to select value from a collection. 


>note When RadDataGrid.AutoGenerateColumns="True" the RadDataGrid generates typed columns depending on the underlying data type.

## Properties

All types of columns inherit from the **DataGridColumn** class which provides the following properties:

* **CellDecorationStyle** (DataGridBorderStyle): Gets or sets the Style object that defines the background of each cell associated with this column. The TargetType property of the Style object is Rectangle.
* **CellDecorationStyleSelector** (DataGridStyleSelector): Gets or sets the StyleSelector instance that allows for dynamic decoration on a per cell basis.
* **HeaderText** (string): Gets or sets the content to be displayed in the Header UI that represents the column.
* **HeaderStyle** (DataGridColumnHeaderStyle): Gets or sets the Style instance that defines the appearance of the DataGridColumnHeader control.
* **HeaderContentTemplate** (DataTemplate): Gets or sets the DataTemplate instance that defines the appearance of the header.
* **SizeMode** (DataGridColumnSizeMode): Gets or sets the DataGridColumnSizeMode value that controls how the column and its associated cells are sized horizontally.
  * Fixed: The column has a fixed width as defined by its Width property.
  * Stretch: The column is stretched to the available width proportionally to its desired width.
  * Auto: The columns is sized to its desired width. That is the maximum desired width of all associated cells.
* **Width** (double): - Gets or sets the fixed width for the column. Applicable when the SizeMode property is set to DataGridColumnSizeMode.Fixed.
* **ActualWidth** (double): Gets the actual width of the column.
* **IsAutoGenerated** (bool): Gets a value indication whether the column is auto-generated internally.
* **CanUserEdit** (bool): Gets or sets a value indicating whether the user can edit the values in this column.
* **CanUserGroup** (bool): Gets or sets a value indicating whether the user can group-by this column by using the built-in Grouping UI.
* **CanUserFilter** (bool): Gets or sets a value indicating whether the user can filter this column by using the built-in Filtering UI.
* **CanUserSort** (bool): Gets or sets a value indicating whether the user can sort the data by the values in this column.
* **IsVisible** (bool): Gets a value indicating if a specific column should be visualized.

>note In order to enable the user edit mode of the RadDataGrid cell, set the *RadDataGrid.UserEditMode="Cell"*.

## Example

Here is an example containing all types of columns RadDataGrid control provides.

Use the following snippet to declare a RadDataGrid in XAML: 
<snippet id='datagrid-columns-xaml'/>

Where the **telerikGrid** namespace is the following:

```xml
xmlns:telerikGrid="clr-namespace:Telerik.XamarinForms.DataGrid;assembly=Telerik.XamarinForms.DataGrid"
```

The **ViewModel** class is declared as following:

<snippet id='datagrid-columns-viewmodel'/>
	
And the **Club** custom object:

<snippet id='datagrid-columns-data'/>

>important An example with DataGrid columns can be found in the DataGrid/Columns folder of the [SDK Samples Browser application]({%slug developer-focused-examples%}).

## See Also

- [Picker Column]({%slug datagrid-columns-picker-column %})
- [Template Column]({%slug datagrid-columns-template-column %})
- [Text Column]({%slug datagrid-columns-text-column %})
