### <a name="htmltextwriter-does-not-render-br-element-correctly"></a>HtmlTextWriter 不呈现`<br/>`元素正确

|   |   |
|---|---|
|详细信息|从 .NET Framework 4.6 开始，调用带有 <code>&lt;BR /&gt;</code> 的 <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)> 和 <xref:System.Web.UI.HtmlTextWriter.RenderEndTag> 将正确插入唯一 <code>&lt;BR /&gt;</code>（而非两个）|
|建议|如果应用依赖于多余的 <code>&lt;BR /&gt;</code> 标记，应再次调用 <xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)>。 请注意此行为的更改仅影响面向.NET Framework 4.6 或更高版本，以便另一个选项是为了获取这一旧行为面向以前版本的.NET framework 的应用。|
|范围|边缘|
|版本|4.6|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.UI.HtmlTextWriter.RenderBeginTag(System.Web.UI.HtmlTextWriterTag)?displayProperty=nameWithType></li></ul>|

