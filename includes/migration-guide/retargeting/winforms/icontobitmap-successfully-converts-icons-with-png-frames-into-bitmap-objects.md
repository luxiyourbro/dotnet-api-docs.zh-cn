### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap 成功将带 PNG 帧的图标转换为位图对象

|   |   |
|---|---|
|详细信息|从面向.NET Framework 4.6，应用开始<xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType>方法已成功将带 PNG 帧的图标转换为位图对象。在面向.NET Framework 4.5.2 及早期版本中，应用程序，<xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType>方法抛出异常<xref:System.ArgumentOutOfRangeException>如果图标对象具有 PNG 帧的异常。此更改仅影响的应用程序编译为面向.NET Framework 4.6 和实施特殊处理的有关<xref:System.ArgumentOutOfRangeException>图标对象具有 PNG 帧时引发。 在.NET Framework 4.6 下运行时，转换成功，不再引发 <xref:System.ArgumentOutOfRangeException> ，因此不再调用异常处理程序。|
|建议|如果不需要此行为，你可以通过添加到下面的元素保留以前的行为<code>&lt;runtime&gt;</code>app.config 文件的部分：<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>如果 app.config 文件已包含<code>AppContextSwitchOverrides</code>元素，应与如下 value 属性合并新值：<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.6|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

