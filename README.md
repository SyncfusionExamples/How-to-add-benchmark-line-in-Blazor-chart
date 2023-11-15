# How-to-add-benchmark-line-in-Blazor-chart

This article explains how to add a benchmark line in Blazor chart.

**Creating benchmark line in blazor chart using ChartAnnotations**

You can represent a Benchmark line in [Blazor chart](https://www.syncfusion.com/blazor-components/blazor-charts) component by using [ChartAnnotations](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartAnnotations.html). Annotations are texts, shapes, or images that are used to highlight a specific region on interest in chart.

The [ChartAnnotations](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartAnnotations.html) property allows to add annotations to the chart. Specify the ID of the element that needs to be displayed in the chart area by using the [Content](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartAnnotation.html#Syncfusion_Blazor_Charts_ChartAnnotation_Content) property of the annotation.

The below code snippet shows how to insert a html element in blazor chart using annotations.

```cshtml

<ChartAnnotations>
    <ChartAnnotation X="33.94" Y="100"  Region="Regions.Series" CoordinateUnits="Units.Pixel">
        <ContentTemplate>
            <div id="bench-mark">
                <hr id="test" style="border-top: 2px solid orange;opacity:100%; width: 10000px"/>                        
            </div>                  
        </ContentTemplate>                
    </ChartAnnotation>   
    <ChartAnnotation X="@Country" Y="65" Region="Regions.Series" CoordinateUnits="Units.Point">
        <ContentTemplate  >
            <div style="font-size:90%; opacity:1; color:blue;position: absolute; top: 30px; left:-550px;">Benchmark</div>                
        </ContentTemplate>            
    </ChartAnnotation>
</ChartAnnotations>

```

The below code example illustrates this.

**Index.razor**

```cshtml

@using Syncfusion.Blazor.Charts

<SfChart Title="Olympic Medals">
    <ChartPrimaryXAxis ValueType="Syncfusion.Blazor.Charts.ValueType.Category">
    </ChartPrimaryXAxis>
    <ChartAnnotations>
        <ChartAnnotation X="33.94" Y="100"  Region="Regions.Series" CoordinateUnits="Units.Pixel">
            <ContentTemplate>
                <div id="bench-mark">
                    <hr id="test" style="border-top: 2px solid orange;opacity:100%; width: 10000px"/>                        
                </div>                  
            </ContentTemplate>                
        </ChartAnnotation>   
        <ChartAnnotation X="@Country" Y="65" Region="Regions.Series" CoordinateUnits="Units.Point">
            <ContentTemplate  >
                <div style="font-size:90%; opacity:1; color:blue;position: absolute; top: 30px; left:-418px;">Benchmark</div>                
            </ContentTemplate>            
        </ChartAnnotation>
    </ChartAnnotations>
    <ChartSeriesCollection>
        <ChartSeries DataSource="@MedalDetails" XName="Country" YName="Gold" Type="ChartSeriesType.Column">
        </ChartSeries>
    </ChartSeriesCollection>
</SfChart>

@code {

    string Country = "Australia";

    public class ChartData
    {
        public string Country { get; set; }
        public double Gold { get; set; }
    }

    public List<ChartData> MedalDetails = new List<ChartData>
    {
        new ChartData{ Country= "USA", Gold=50  },
        new ChartData{ Country= "China", Gold=40 },
        new ChartData{ Country= "Japan", Gold=70 },
        new ChartData{ Country= "Australia", Gold=60},
        new ChartData{ Country= "France", Gold=50 },
        new ChartData{ Country= "Germany", Gold=40 },
        new ChartData{ Country= "Italy", Gold=40 },
        new ChartData{ Country= "Sweden", Gold=30 }
    };
}

```

The following screenshot illustrate the output of the above code snippet.

**Output:**

 ![](/benchmark.png)

**Conclusion**

I hope you enjoyed learning how to add benchmark line in Blazor chart component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!
