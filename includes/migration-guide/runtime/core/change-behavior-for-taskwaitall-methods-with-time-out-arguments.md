### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>带超时自变量的 Task.WaitAll 方法的行为更改

|   |   |
|---|---|
|详细信息|Task.WaitAll 行为是为了更加一致.NET 4.5.In.NET Framework 4 中，这些方法的行为不一致。 当超时到期时，如果在调用此方法之前已完成或已取消一个或多个任务，则此方法会引发 <xref:System.AggregateException?displayProperty=name> 异常。 在超时到期时，如果在调用此方法之前尚未完成或取消任何任务，但在调用此方法之后，一个或多个任务进入了这些状态，则该方法返回 false。<br/><br/>在.NET Framework 4.5，这些方法重载现在时返回 false 的任何任务仍在运行时的超时间隔过期，并且它们将引发<xref:System.AggregateException?displayProperty=name>异常仅当取消某个输入的任务 （无论它是之前或之后方法调用） 和任何其他任务仍在运行。|
|建议|如果<xref:System.AggregateException?displayProperty=name>正在捕获作为一种检测已取消正在调用 WaitAll 调用之前，代码应改为执行通过 IsCanceled 属性相同的检测的任务 (例如:。Any(t =&gt; t.IsCanceled)) 因为如果在超时之前完成所有等待的任务，仅将在这种情况下引发.NET 4.6。|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

