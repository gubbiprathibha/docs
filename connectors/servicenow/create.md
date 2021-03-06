---
title: Workato connectors - ServiceNow create record actions
date: 2018-05-30 06:00:00 Z
---

# ServiceNow - Create record actions

## Create record
This action creates a single record into any table in your ServiceNow instance.

![Create record action](/assets/images/connectors/servicenow/create-record-action.png)
*Create record action*

### Input fields

<table class="unchanged rich-diff-level-one">
  <thead>
    <tr>
        <th width='25%'>Input field</th>
        <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="#table">Table</a></td>
      <td>
        Select a table to create a record in.
      </td>
    </tr>
    <tr>
      <td><a href="#new-record-values">New record values</a></td>
      <td>
        Provide data for each column of the record to be created.
      </td>
    </tr>
  </tbody>
</table>

### Output fields
The output datatree of this action contains the full set of columns from the selected table. All default and custom columns are supported. The output fields will be displayed only after a table is provided, either by selecting a table from the pick list or by providing the full table name.

![Output fields](/assets/images/connectors/servicenow/extended-output.gif)
*Output fields*

## Create record using a template
This action creates a single record into any table in your ServiceNow instance by applying a template to the newly created record.

After a template is chosen, you can map additional datapills to the new record. The template values will be applied on top of your mapping. You can choose to retain or override the template values in this action.

![Create record using a template action](/assets/images/connectors/servicenow/create-record-using-template-action.png)
*Create record using a template action*

### Input fields

<table class="unchanged rich-diff-level-one">
  <thead>
    <tr>
        <th width='25%'>Input field</th>
        <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="#table">Table</a></td>
      <td>
        Select a table to create a record in.
      </td>
    </tr>
    <tr>
      <td><a href="#template">Template</a></td>
      <td>
        Select a template associated with the selected table.
      </td>
    </tr>
    <tr>
      <td><a href="#override-template">Override template</a></td>
      <td>
        Choose whether you want to override the default template values with the data provided in <b>New record values</b>.
      </td>
    </tr>
    <tr>
      <td><a href="#new-record-values">New record values</a></td>
      <td>
        Provide data for each column of the record to be created.
      </td>
    </tr>
  </tbody>
</table>

### Output fields
The output datatree of this action contains the full set of columns from the selected table. All default and custom columns are supported. The output fields will be displayed only after a table is provided, either by selecting a table from the pick list or by providing the full table name.

Additionally, the sys ID of the template applied to this record is also included in the output.

![Output fields](/assets/images/connectors/servicenow/extended-output.gif)
*Output fields*

## Input field definitions

### Table
Select the table to create a record in. This can be done either by selecting a table from the pick list, or toggling the input field to text mode and typing the full table name.

Make sure that the connected user has [sufficient access control](/connectors/servicenow.md#roles-and-permissions-required-to-connect) to the selected table.

### Template
Select the template to be applied to the newly created record. This can be done either by selecting a template from the pick list, or toggling the input field to text mode and providing the template sys ID. This template must be associated with the selected table.

Make sure that the connected user has [sufficient access control](/connectors/servicenow.md#roles-and-permissions-required-to-connect) to the selected template.

### Override template
You can choose to override the pre-defined template values that will be automatically applied to the newly created record. If **Yes** is selected, any data provided for columns will be applied instead of template default values. This field defaults to **No**.

### New record values
Provide data for every column that needs to be filled for the new record in the selected table. This can be done by mapping datapills from previous triggers or actions into the respective columns.
