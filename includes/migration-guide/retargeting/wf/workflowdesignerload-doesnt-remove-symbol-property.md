### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a>WorkflowDesigner.Load 并不会删除符号属性

|   |   |
|---|---|
|详细信息|在面向.NET Framework 4.5 工作流设计器中，和加载的重新承载 3.5 工作流中<xref:System.Activities.Presentation.WorkflowDesigner.Load>方法，<xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name>保存工作流时引发。|
|建议|此 bug 仅清单时以.NET Framework 4.5 中工作流设计器中，目标，因此它可以通过设置解决<code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code>到 4.0 的.NET Framework.Alternatively，可能通过使用避免此问题<xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)>方法以加载工作流而不是<xref:System.Activities.Presentation.WorkflowDesigner.Load>。|
|范围|主要|
|版本|4.5|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|

