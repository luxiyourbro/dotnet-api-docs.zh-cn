### <a name="wpf-windows-are-rendered-without-clipping-when-extending-outside-a-single-monitor"></a>在扩展超出单个监视器时，会不经剪辑呈现是 WPF 窗口

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6 运行 Windows 8 和更高版本中，整个窗口超出多监视器方案中的单个显示屏时会不经剪辑呈现。 这是不同于以前版本的.NET Framework，它将剪辑超出单个显示屏扩展的 WPF 窗口。|
|建议|此行为 （是否剪切或不） 可以显式设置使用<code>&lt;EnableMultiMonitorDisplayClipping&gt;</code>中的元素<code>&lt;appSettings&gt;</code>在应用程序的配置文件中，或通过设置<code>EnableMultiMonitorDisplayClipping</code>属性在应用启动。|
|范围|次要|
|版本|4.6|
|类型|运行时|

