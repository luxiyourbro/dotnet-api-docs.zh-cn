### <a name="wpf-pointer-based-touch-stack"></a>WPF 基于指针的触摸堆栈

|   |   |
|---|---|
|详细信息|此更改将添加能够启用可选 WM_POINTER 基于 WPF 触摸/触笔堆栈。  不要显式启用此选项的开发人员应查看 WPF 触摸/触笔行为方面没有变化。已知问题与可选 WM_POINTER 当前基于触摸/触笔堆栈：<ul><li>不支持实时墨迹书写。</li><li>时墨迹和 StylusPlugins 仍将起作用，则将在这会导致性能不佳的 UI 线程上进行处理。</li><li>由于从触摸/触笔事件提升到鼠标事件中的更改的行为更改</li><li>操作的行为可能不同</li><li>拖放将不会显示相应触控输入反馈</li><li>这不会影响触笔输入</li><li>不再可在触摸/触笔事件上启动拖放</li><li>这可能会在检测到鼠标输入前导致应用程序挂起。</li><li>相反，开发者应通过鼠标事件启动拖放行为。</li></ul>|
|建议|开发人员想要启用此堆栈可以添加转换/合并到其应用程序的 App.config 文件以下：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Input.Stylus.EnablePointerSupport=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>删除这或将该值设置为 false 将关闭此可选堆栈。请注意，此堆栈是仅在 Windows 10 创建者 Update 及以上版本可用。|
|范围|边缘|
|版本|4.7|
|类型|重定目标|

