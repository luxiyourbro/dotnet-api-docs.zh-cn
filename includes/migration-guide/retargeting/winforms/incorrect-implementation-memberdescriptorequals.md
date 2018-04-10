### <a name="incorrect-implementation-of-memberdescriptorequals"></a>不正确的 MemberDescriptor.Equals 的实现

|   |   |
|---|---|
|详细信息|原始实现&quot;等于&quot;方法将从下比较的对象的两个不同的字符串属性进行比较： 到描述字符串的类别名称。 解决方法是比较&quot;类别&quot;到第一个对象的&quot;类别&quot;的第二个和&quot;说明&quot;到&quot;说明&quot;。 为 true 以选择退出该新行为，如果面向 4.6.2 或为 false 时确定目标 framework 版本低于 4.6.2 启用此修补程序，可以设置 MemberDescriptorEqualsReturnsFalseIfEquivalent 配置值。|
|建议|如果你的应用程序依赖于 MemberDescriptor.Equals 有时返回 false 时描述符是等效的并且目标 4.6.2 版本的.NET Framework 中，有几个选项：<ol><li>更改代码以比较&quot;类别&quot;和&quot;说明&quot;手动除了运行 Equals 方法的字段。</li><li>选择退出此更改通过将以下值添加到 app.config 文件：</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>如果你的应用程序所针对 4.6.1 或较低版本的.NET Framework 中，并且你想要启用此更改，可以通过将以下值添加到 app.config 文件的兼容性开关设置为 false:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.6.2|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

