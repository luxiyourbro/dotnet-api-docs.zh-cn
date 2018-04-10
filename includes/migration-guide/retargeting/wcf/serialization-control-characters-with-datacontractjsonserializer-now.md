### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>序列化带 DataContractJsonSerializer 的控制字符现与 ECMAScript V6 和 V8 兼容

|   |   |
|---|---|
|详细信息|在.NET framework 4.6.2 和早期版本中，<xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name>未序列化某些特殊控制字符，如 \b、 \f、 和 \t，与 ECMAScript V6 和 V8 标准兼容的方式。 从.NET Framework 4.7 开始，这些控件字符的序列化是与 ECMAScript V6 和 V8 兼容。|
|建议|对于面向.NET Framework 4.7 的应用程序，默认情况下启用此功能。 如果不需要此行为，可以在 app.config 或 web.config 文件的 <code>&lt;runtime&gt;</code> 部分中添加下面的代码行，从而选择禁用此功能：<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.7|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

