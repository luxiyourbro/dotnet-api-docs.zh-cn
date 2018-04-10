### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a>工作流现在引发原始异常而不是 NullReferenceException 在某些情况下

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6.2 和早期版本中，在工作流活动的 Execute 方法引发的异常时<code>null</code>值<xref:System.Exception.Message>属性，则 System.Activities 工作流运行时会引发<xref:System.NullReferenceException?displayProperty=name>、 蒙版原始异常。在.NET Framework 4.7，以前掩蔽引发异常。|
|建议|如果你的代码依赖于处理<xref:System.NullReferenceException?displayProperty=name>，将其更改为捕获可能从自定义活动时引发的异常。|
|范围|次要|
|版本|4.7|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|

