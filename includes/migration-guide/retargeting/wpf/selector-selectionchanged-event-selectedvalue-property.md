### <a name="selector-selectionchanged-event-and-selectedvalue-property"></a>选择器 SelectionChanged 事件和 SelectedValue 属性

|   |   |
|---|---|
|详细信息|开始使用.Net Framework 4.7.1，<xref:System.Windows.Controls.Primitives.Selector>始终更新的值，其<xref:System.Windows.Controls.Primitives.Selector.SelectedValue%2A>属性之前引发<xref:System.Windows.Controls.Primitives.Selector.SelectionChanged>时其所选内容更改事件。 这使得 SelectedValue 属性与其他选择属性一致 (<xref:System.Windows.Controls.Primitives.Selector.SelectedItem%2A>和<xref:System.Windows.Controls.Primitives.Selector.SelectedIndex%2A>)，在引发事件之前更新其。在大多数情况下，事件之前 SelectedValue 的更新发生在.NET Framework 4.7 和早期版本中，但如果所选内容更改引起的更改发生在事件后<xref:System.Windows.Controls.Primitives.Selector.SelectedValue%2A>属性。|
|建议|面向.NET Framework 4.7.1 或更高版本可以选择退出此应用更改，并通过添加以下使用旧行为<code>&lt;runtime&gt;</code>应用程序配置文件节：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>应用程序面向.NET Framework 4.7 或更早版本，但在.NET Framework 4.7.1 上运行或更高版本可以通过添加以下行将对启用新的行为<code>&lt;runtime&gt;</code>的应用程序.configuration 文件的部分：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.7.1|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|

