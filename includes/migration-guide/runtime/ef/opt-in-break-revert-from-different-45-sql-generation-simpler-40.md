### <a name="opt-in-break-to-revert-from-different-45-sql-generation-to-simpler-40-sql-generation"></a>选择加入中断可恢复从不同 4.5 SQL 生成到更简单 4.0 的 SQL 生成

|   |   |
|---|---|
|详细信息|生成联接语句并包含的调用的查询对限制操作但未事先现在使用 OrderBy 产生更简单的 SQL。 升级到.NET Framework 4.5 后，这些查询生成了比以前版本更复杂的 SQL。|
|建议|在默认情况下，禁用此功能。 如果实体框架生成可导致性能降低的额外 JOIN 语句，你可以启用此功能，通过添加以下条目到<code>&lt;appSettings&gt;</code>的应用程序配置 (app.config) 文件的部分：<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyLimitOperations&quot; value=&quot;true&quot; /&gt;&#13;&#10;</code></pre>|
|范围|透明|
|版本|4.5.2|
|类型|运行时|

