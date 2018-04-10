### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>WCF PipeConnection.GetHashAlgorithm 现在使用 SHA256

|   |   |
|---|---|
|详细信息|从.NET Framework 4.7.1 开始，Windows Communication Foundation 使用 SHA256 哈希来生成随机的命名管道的名称。 在.NET Framework 4.7 和早期版本中，它使用 SHA1 哈希。|
|建议|如果在.NET Framework 4.7.1 上遇到进行此更改后的兼容性问题或更高版本，你可以选择退出它通过添加以下行将对<code>&lt;runtime&gt;</code>app.config 文件的部分：<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|范围|次要|
|版本|4.7.1|
|类型|运行时|

