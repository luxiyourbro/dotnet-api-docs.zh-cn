### <a name="improved-accessibility-for-some-net-sdk-tools"></a>一些.NET SDK 工具的改进辅助功能

|   |   |
|---|---|
|详细信息|在.NET Framework SDK 4.7.1 中，svcconfigedit.exe 和 svctraceviewer.exe 工具已得到改进通过修复各种可访问性问题。 这些大部分了未定义的名称或未被正确实现特定的 UI 自动化模式等的小问题。 虽然许多用户不会注意这些不正确的值，使用辅助技术，如屏幕阅读器的客户将发现这些 SDK 工具更易于访问。 当然，这些修补程序更改某些以前的行为，如键盘焦点订单。若要获取所有可访问性修复在这些工具中，可以以下到 app.config 文件：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.7.1|
|类型|重定目标|

