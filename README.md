# How to Add a Benchmark Line in a Blazor Chart Using Chart Annotations

## Overview

This sample demonstrates how to add a benchmark line to a Syncfusion [Blazor Charts](https://www.syncfusion.com/blazor-components/blazor-charts) component by using the `ChartAnnotations` collection. The chart displays country medal data as a column series and overlays a benchmark indicator using annotation content rendered within the chart area.

The approach allows developers to visually compare actual values against a target threshold without modifying the underlying data series. By combining `ChartAnnotation` and `ContentTemplate`, custom HTML content can be positioned precisely within the chart.

## Key Features

- Uses the `SfChart` component to render the chart.
- Configures `ChartPrimaryXAxis` with `ValueType="ValueType.Category"` for category-based data visualization.
- Adds custom benchmark visuals through the `ChartAnnotations` collection.
- Uses `ChartAnnotation` elements with:
  - `X`
  - `Y`
  - `Region`
  - `CoordinateUnits`
- Uses the `ContentTemplate` property to render custom HTML content inside the chart area.
- Creates a benchmark line using an HTML `<hr>` element rendered through an annotation template.
- Displays a benchmark label using a second annotation positioned relative to a chart data point.
- Binds chart data through the `ChartSeries` component using:
  - `DataSource`
  - `XName`
  - `YName`
  - `Type="ChartSeriesType.Column"`

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download the repository.
2. Open the project file:
   - `Benchmark/Benchmark.csproj`
3. Restore NuGet packages.
4. Build the project.
5. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Clone or download the repository.
2. Open the repository folder in Visual Studio Code.
3. Open the integrated terminal.
4. Navigate to the project directory.

```bash
cd Benchmark
```

5. Restore NuGet packages:

```bash
dotnet restore
```

6. Run the application:

```bash
dotnet run
```

7. Open the local URL displayed in the console output.

## Project Structure

`Benchmark/Pages/Index.razor` - Demonstrates the benchmark-line implementation using `SfChart`, `ChartAnnotations`, `ChartAnnotation`, and a column series.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Official documentation: https://help.syncfusion.com/chart-sdk/blazor/charts/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.