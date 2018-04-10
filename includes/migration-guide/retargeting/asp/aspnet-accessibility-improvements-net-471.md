### <a name="aspnet-accessibility-improvements-in-net-471"></a>在.NET 4.7.1 ASP.NET 可访问性改进

|   |   |
|---|---|
|详细信息|从.NET Framework 4.7.1 开始，ASP.NET 改进了 ASP.NET Web 控件与 Visual Studio 中的辅助功能技术，以与客户更好的支持 ASP.NET 的工作方式。  这些方法包括以下更改：<ul><li>更改以在控件中，实现缺少 UI 可访问性模式，例如在详细信息视图向导中，添加字段对话框或 ListView 向导的配置 ListView 对话框。</li><li>更改，以提高在高对比度模式，例如数据页导航字段编辑器中的显示。</li><li>更改，以提高键盘导航遇到的控件，如 DataPager 控件、 配置 ObjectContext 对话框中或配置数据源向导的配置数据所选项对话框的编辑页导航字段向导中的字段对话框。</li></ul>|
|建议|<strong>如何选择加入或退出这些更改</strong>使 Visual Studio 设计器，以利用这些更改，它必须运行.NET Framework 4.7.1 上或更高版本。 Web 应用程序可以利用这些更改通过以下方式之一：<ul><li>安装 Visual Studio 2017 15.3 或更高版本，默认情况下支持与以下 AppContext 交换机的新辅助功能。</li><li>通过添加选择退出旧的可访问性行为<code>Switch.UseLegacyAccessibilityFeatures</code>AppContext 切换到<code>&lt;runtime&gt;</code>在 devenv.exe.config 文件中的节，并将它设置为<code>false</code>，如下面的示例所示。</li></ul><pre><code class="language-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;...&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false&#39;  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;...;Switch.UseLegacyAccessibilityFeatures=false&quot; /&gt;&#13;&#10;...&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>面向.NET Framework 4.7.1 的应用程序或更高版本，并且想要保留旧可访问性行为来选择加入的旧的可访问性功能的使用通过此 AppContext 开关显式设置为<code>true</code>。|
|范围|次要|
|版本|4.7.1|
|类型|重定目标|

