### <a name="long-path-support"></a><span data-ttu-id="1d360-101">长路径支持</span><span class="sxs-lookup"><span data-stu-id="1d360-101">Long path support</span></span>

|   |   |
|---|---|
|<span data-ttu-id="1d360-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="1d360-102">Details</span></span>|<span data-ttu-id="1d360-103">从应用开始，支持.NET Framework 4.6.2，长路径 (最多 32 个 K 字符），该目标和 260 个字符 (或<code>MAX_PATH</code>) 已删除路径的长度限制。对于应用程序编译为面向.NET Framework 4.6.2，代码路径之前引发<xref:System.IO.PathTooLongException?displayProperty=name>因为路径超过 260 个字符将立即引发<xref:System.IO.PathTooLongException?displayProperty=name>仅在以下情况：</span><span class="sxs-lookup"><span data-stu-id="1d360-103">Starting with apps that target the .NET Framework 4.6.2, long paths (of up to 32K characters) are supported, and the 260-character (or <code>MAX_PATH</code>) limitation on path lengths has been removed.For apps that are recompiled to target the .NET Framework 4.6.2, code paths that previously threw a <xref:System.IO.PathTooLongException?displayProperty=name> because a path exceeded 260 characters will now throw a <xref:System.IO.PathTooLongException?displayProperty=name> only under the following conditions:</span></span><ul><li><span data-ttu-id="1d360-104">路径的长度大于<xref:System.Int16.MaxValue>(32,767) 个字符。</span><span class="sxs-lookup"><span data-stu-id="1d360-104">The length of the path is greater than <xref:System.Int16.MaxValue> (32,767) characters.</span></span></li><li><span data-ttu-id="1d360-105">操作系统返回 <code>COR_E_PATHTOOLONG</code> 或其等同项。</span><span class="sxs-lookup"><span data-stu-id="1d360-105">The operating system returns <code>COR_E_PATHTOOLONG</code> or its equivalent.</span></span></li></ul><span data-ttu-id="1d360-106">对于面向.NET Framework 4.6.1 及更早版本的应用程序，则运行时会自动引发<xref:System.IO.PathTooLongException?displayProperty=name>每当路径超过 260 个字符。</span><span class="sxs-lookup"><span data-stu-id="1d360-106">For apps that target the .NET Framework 4.6.1 and earlier versions, the runtime automatically throws a <xref:System.IO.PathTooLongException?displayProperty=name> whenever a path exceeds 260 characters.</span></span>|
|<span data-ttu-id="1d360-107">建议</span><span class="sxs-lookup"><span data-stu-id="1d360-107">Suggestion</span></span>|<span data-ttu-id="1d360-108">对于面向.NET Framework 4.6.2 的应用程序，你可以选择退出长路径支持如果这是不值得通过添加以下<code>&lt;runtime&gt;</code>部分你<code>app.config</code>文件：</span><span class="sxs-lookup"><span data-stu-id="1d360-108">For apps that target the .NET Framework 4.6.2, you can opt out of long path support if it is not desirable by adding the following to the <code>&lt;runtime&gt;</code> section of your <code>app.config</code> file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre><span data-ttu-id="1d360-109">对于面向的应用的.NET framework 的早期版本但在.NET Framework 4.6.2 上运行或更高版本，你可以选择在长路径支持通过添加以下<code>&lt;runtime&gt;</code>部分你<code>app.config</code>文件：</span><span class="sxs-lookup"><span data-stu-id="1d360-109">For apps that target earlier versions of the .NET Framework but run on the .NET Framework 4.6.2 or later, you can opt in to long path support by adding the following to the <code>&lt;runtime&gt;</code> section of your <code>app.config</code> file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.BlockLongPaths=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="1d360-110">范围</span><span class="sxs-lookup"><span data-stu-id="1d360-110">Scope</span></span>|<span data-ttu-id="1d360-111">次要</span><span class="sxs-lookup"><span data-stu-id="1d360-111">Minor</span></span>|
|<span data-ttu-id="1d360-112">版本</span><span class="sxs-lookup"><span data-stu-id="1d360-112">Version</span></span>|<span data-ttu-id="1d360-113">4.6.2</span><span class="sxs-lookup"><span data-stu-id="1d360-113">4.6.2</span></span>|
|<span data-ttu-id="1d360-114">类型</span><span class="sxs-lookup"><span data-stu-id="1d360-114">Type</span></span>|<span data-ttu-id="1d360-115">重定目标</span><span class="sxs-lookup"><span data-stu-id="1d360-115">Retargeting</span></span>|
