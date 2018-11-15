<!-- default file list -->
*Files to look at*:

* [HomeController.cs](./CS/Dashboard_WidgetAccess_MVC/Controllers/HomeController.cs) (VB: [HomeController.vb](./VB/Dashboard_WidgetAccess_MVC/Controllers/HomeController.vb))
* [WidgetsCustomization.js](./CS/Dashboard_WidgetAccess_MVC/Scripts/WidgetsCustomization.js) (VB: [WidgetsCustomization.js](./VB/Dashboard_WidgetAccess_MVC/Scripts/WidgetsCustomization.js))
* [_DashboardViewerPartial.cshtml](./CS/Dashboard_WidgetAccess_MVC/Views/Home/_DashboardViewerPartial.cshtml)
* [Index.cshtml](./CS/Dashboard_WidgetAccess_MVC/Views/Home/Index.cshtml)
<!-- default file list end -->
# How to access API of underlying widgets in the MVC Viewer


<strong>Note:</strong> <em>Starting with v17.1, we recommend using the <a href="https://documentation.devexpress.com/Dashboard/CustomDocument16976.aspx">ASPxDashboard control</a> or a corresponding <a href="https://documentation.devexpress.com/Dashboard/CustomDocument16977.aspx">ASP.NET MVC extension</a> to display dashboards within web applications.</em><br><br>This example demonstrates how to customize client widgets used to visualize data within dashboard items at runtime using <a href="http://documentation.devexpress.com/#Dashboard/clsDevExpressDashboardWebScriptsASPxClientDashboardViewertopic">ASPxClientDashboardViewer</a>'s API.<br>The following options are changed

* Highlighting of the hovered grid row is enabled in the underlying dxDataGrid in the <a href="http://documentation.devexpress.com/#Dashboard/DevExpressDashboardWebScriptsASPxClientDashboardViewer_ItemWidgetCreatedtopic">ItemWidgetCreated</a> event handler.
* A standard tooltip that is invoked when an end-user hovers over a chart series point is disabled. You can invoke a tooltip by clicking the required label on the argument axis. The argumentAxisClick event is used for this purpose. Subscription and unsubscription to/from the argumentAxisClick event are performed in the <a href="http://documentation.devexpress.com/#Dashboard/DevExpressDashboardWebScriptsASPxClientDashboardViewer_ItemWidgetCreatedtopic">ItemWidgetCreated</a> and <a href="http://documentation.devexpress.com/#Dashboard/DevExpressDashboardWebScriptsASPxClientDashboardViewer_ItemBeforeWidgetDisposedtopic">ItemBeforeWidgetDisposed</a> event handlers respectively.
* A pie legend is shown for the underlying dxPieChart.

<br/>


