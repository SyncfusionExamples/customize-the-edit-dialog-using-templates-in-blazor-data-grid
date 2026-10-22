# Customize the Edit Dialog Using Templates in Blazor Data Grid

## Overview

This sample demonstrates how to customize the edit dialog of the Syncfusion [Blazor DataGrid](https://www.syncfusion.com/blazor-components/blazor-datagrid) by using dialog templates and embedding multiple editor components within the editing form. The implementation uses custom editors such as TextBox, NumericTextBox, AutoComplete, DatePicker, and DropDownList inside the dialog template to provide a tailored data-entry experience. The grid displays order data through an `OrderDetails` model and supports dialog-based record editing. An action handler is also used to detect add operations and dynamically adjust dialog behavior when creating new records.

## Key Features

- Uses the Syncfusion Blazor DataGrid with dialog-based editing.
- Customizes the edit dialog through a template instead of the default editor layout.
- Integrates Syncfusion `TextBox` components for text input fields.
- Integrates Syncfusion `NumericTextBox` components for numeric fields.
- Integrates Syncfusion `AutoComplete` components for assisted text selection.
- Integrates Syncfusion `DatePicker` components for date editing.
- Integrates Syncfusion `DropDownList` components for predefined selections.
- Uses an `OrderDetails` data model containing fields such as `OrderID`, `CustomerID`, `Freight`, `ShipCity`, `OrderDate`, `ShipName`, `ShipCountry`, and `ShipAddress`.
- Maintains editable order records using an in-memory `List<OrderDetails>` collection.
- Implements `OnActionBeginHandler(ActionEventArgs args)` to identify add operations and update the `IsAddNew` state when `RequestType` equals `Action.Add`. 【2-671b11】

## Prerequisites

- Visual Studio 2022 or Visual Studio Code
- .NET 10.0 SDK

## How to Run the Project

**Visual Studio 2022**

1. Clone or download the repository.
2. Open the project file `CustomizingEditDialog.csproj`.
3. Restore all NuGet packages.
4. Build and run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Open the repository folder in Visual Studio Code.
2. Open the integrated terminal.

```bash
dotnet restore
dotnet run
```

3. Open the local URL displayed in the terminal after the application starts.

## Project Structure (.NET 10 standalone Blazor WebAssembly)

- `CustomizingEditDialog.csproj` — the Blazor WebAssembly app project (`net10.0`).
- `Program.cs` — app entry point; registers Syncfusion Blazor services.
- `App.razor` / `_Imports.razor` — root component and global using directives.
- `Layout/` — `MainLayout.razor` and `NavMenu.razor` shared layouts.
- `Pages/Index.razor` — contains the DataGrid implementation, dialog template configuration, custom editor components, sample order data, `OrderDetails` model, and `OnActionBeginHandler` logic.
- `wwwroot/index.html` — hosts the app and references the Syncfusion theme and scripts.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- For feature documentation, see the Syncfusion Blazor DataGrid Editing documentation: https://help.syncfusion.com/grid-sdk/blazor/data-grid/dialog-editing

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.
