### <a name="resizing-a-grid-can-hang"></a>调整网格的大小会挂起

|   |   |
|---|---|
|详细信息|无限循环可能会发生布局<code>T:System.Windows.Controls.Grid</code>下列情况下：<ul><li>行定义包含两个 * 的行，这两个声明 MinHeight 和 MaxHeight。</li><li>内容的 *-行未超过相应 MaxHeight</li><li>第一个 MinHeight 超出网格的可用高度 （以及任何其他修复或自动行）</li><li>应用程序面向.Net 4.7，或通过设置选择 4.7 分配算法 <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>两个以上的行，或在为列类似的情况下，循环将也会发生。在.Net 4.7.1 解决该问题。|
|建议|升级到.Net 4.7.1。  或者，如果你不需要 4.7 分配算法可以使用以下配置设置：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.7|
|类型|运行时|

