### <a name="wcf-addressheadercollection-now-throws-an-argumentexception-if-an-addressheader-element-is-null"></a>WCF AddressHeaderCollection 现在引发 ArgumentException 如果 addressHeader 元素为 null

|   |   |
|---|---|
|详细信息|从.NET Framework 4.7.1，开始<xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})>构造函数引发<xref:System.ArgumentException>如果其中一个元素是<code>null</code>。 在.NET Framework 4.7 和早期版本中，不引发异常。|
|建议|如果你遇到与在.NET Framework 4.7.1 或更高版本上此更改兼容性问题，你可以选择退出的它通过添加以下行将对<code>&lt;runtime&gt;</code>app.config 文件的部分::<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.7.1|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})?displayProperty=nameWithType></li></ul>|

