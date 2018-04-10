### <a name="binaryformatter-can-fail-to-find-type-from-loadfrom-context"></a>BinaryFormatter 可能会失败，若要查找类型从 LoadFrom 上下文

|   |   |
|---|---|
|详细信息|.NET Framework 4.5，大量的截至<xref:System.Xml.Serialization.XmlSerializer?displayProperty=name>时使用，更改可能会导致反序列化中的差异<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>反序列化具有 LoadFrom 上下文中已加载的类型。 这些更改是由于新的方式<xref:System.Xml.Serialization.XmlSerializer?displayProperty=name>现在加载这会导致不同的行为的类型时<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>尝试反序列化该类型到更高版本上。 默认序列化联编程序不会自动搜索 LoadFrom 上下文中，尽管它可能在某些情况下，基于旧的 XmlSerializer 行为方式工作。 由于更改，正在从在不同上下文中，加载的程序集加载类型时<xref:System.IO.FileNotFoundException?displayProperty=name>可能引发。|
|建议|如果显示此异常，<code>Binder</code>属性<xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>可以将设置为一个自定义 binder，它将找到正确的类型。<pre><code class="language-C#">var formatter = new BinaryFormatter { Binder = new TypeFinderBinder() }&#13;&#10;</code></pre>然后自定义的联编程序：<pre><code class="language-C#">public class TypeFinderBinder : SerializationBinder&#13;&#10;{&#13;&#10;private static readonly string s_assemblyName = Assembly.GetExecutingAssembly().FullName;&#13;&#10;&#13;&#10;public override Type BindToType(string assemblyName, string typeName)&#13;&#10;{&#13;&#10;return Type.GetType(String.Format(CultureInfo.InvariantCulture, &quot;{0}, {1}&quot;, typeName, s_assemblyName));&#13;&#10;}&#13;&#10;}&#13;&#10;</code></pre>|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

