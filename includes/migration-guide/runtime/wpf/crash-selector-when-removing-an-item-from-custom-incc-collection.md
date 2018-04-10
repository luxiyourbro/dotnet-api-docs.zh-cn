### <a name="crash-in-selector-when-removing-an-item-from-a-custom-incc-collection"></a>从自定义的 INCC 集合删除项时，选择器中出现故障

|   |   |
|---|---|
|详细信息|<code>T:System.InvalidOperationException</code>可以发生在以下方案：<ul><li>有关 ItemsSource<code>T:System.Windows.Controls.Primitives.Selector</code>是一个集合的自定义实现<code>T:System.Collections.Specialized.INotifyCollectionChanged</code>。</li><li>从集合中移除所选的项。</li><li><code>T:System.Collections.Specialized.NotifyCollectionChangedEventArgs</code>具有<code>P:System.Collections.Specialized.NotifyCollectionChangedEventArgs.OldStartingIndex</code>=-1 （指示未知的位置）。</li></ul>异常的调用堆栈开头 System.Windows.Threading.Dispatcher.VerifyAccess() 在 System.Windows.Controls.Primitives.Selector.GetIsSelected （将在 System.Windows.DependencyObject.GetValue (DependencyProperty dp)元素） 的应用程序具有多个调度程序线程，会在.Net 4.5 中发生此异常。 在.Net 4.7 也可以与单个调度程序线程的应用程序中出现异常。 在.Net 4.7.1 解决该问题。|
|建议|升级到.Net 4.7.1。|
|范围|次要|
|版本|4.7|
|类型|运行时|

