### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>System.Threading.Tasks.Task 释放对象后不再引发 ObjectDisposedException

|   |   |
|---|---|
|详细信息|除<xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>，<xref:System.Threading.Tasks.Task?displayProperty=name>方法将不再引发<xref:System.ObjectDisposedException?displayProperty=name>异常后释放此对象。此更改支持缓存任务的使用。 例如，方法会返回一个缓存任务来表示已完成的操作，而不是分配新任务。 在以前的 .NET Framework 版本中无法执行此操作，因为任务的任何使用者都可以处置它（呈现为不可用）。|
|建议|请注意，可能不再引发任务方法<xref:System.ObjectDisposedException?displayProperty=name>在情况下当释放此对象。 如果应用程序已根据知道任务已处理此异常，它应更新显式检查任务的状态使用<xref:System.Threading.Tasks.Task.Status>。|
|范围|次要|
|版本|4.5|
|类型|运行时|

