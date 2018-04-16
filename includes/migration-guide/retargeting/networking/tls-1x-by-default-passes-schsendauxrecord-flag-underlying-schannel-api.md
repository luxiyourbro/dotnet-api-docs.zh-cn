### <a name="tls-1x-by-default-passes-the-schsendauxrecord-flag-to-the-underlying-schannel-api"></a><span data-ttu-id="c10ea-101">TLS 1.x 默认情况下的将 SCH_SEND_AUX_RECORD 标志传递给基础 SCHANNEL API</span><span class="sxs-lookup"><span data-stu-id="c10ea-101">TLS 1.x by default passes the SCH_SEND_AUX_RECORD flag to the underlying SCHANNEL API</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c10ea-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="c10ea-102">Details</span></span>|<span data-ttu-id="c10ea-103">使用 TLS 时 1.x，依赖于基础 Windows SCHANNEL API 的.NET Framework。</span><span class="sxs-lookup"><span data-stu-id="c10ea-103">When using TLS 1.x, the .NET Framework relies on the underlying Windows SCHANNEL API.</span></span> <span data-ttu-id="c10ea-104">从.NET Framework 4.6 开始[SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx)标志会传递默认情况下，SCHANNEL 给。</span><span class="sxs-lookup"><span data-stu-id="c10ea-104">Starting with .NET Framework 4.6, the [SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx) flag is passed by default to SCHANNEL.</span></span> <span data-ttu-id="c10ea-105">这将导致 SCHANNEL 拆分到两个单独的记录，为单字节和第二个作为第一个要加密数据<em>n</em>-1 字节。在极少数情况下，这会中断客户端和假设的数据位于单个记录中的现有服务器之间的通信。</span><span class="sxs-lookup"><span data-stu-id="c10ea-105">This causes SCHANNEL to split data to be encrypted into two separate records, the first as a single byte and the second as <em>n</em>-1 bytes.In rare cases, this breaks communication between clients and existing servers that make the assumption that the data resides in a single record.</span></span>|
|<span data-ttu-id="c10ea-106">建议</span><span class="sxs-lookup"><span data-stu-id="c10ea-106">Suggestion</span></span>|<span data-ttu-id="c10ea-107">如果此更改会中断与现有的服务器的通信，则可以禁用发送[SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx)标志，并还原不将数据拆分为单独的记录通过添加以下切换到以前的行为[ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md)中[ \` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)的你的应用配置文件：</span><span class="sxs-lookup"><span data-stu-id="c10ea-107">If this change breaks communication with an existing server, you can disable sending the [SCH_SEND_AUX_RECORD](https://msdn.microsoft.com/library/windows/desktop/aa379810.aspx) flag and restore the previous behavior of not splitting data into separate records by adding the following switch to the [\<AppContextSwitchOverrides>](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) in the [\`](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) of your app configuration file:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontEnableSchSendAuxRecord=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] <span data-ttu-id="c10ea-108">为了向后兼容仅提供了此设置。</span><span class="sxs-lookup"><span data-stu-id="c10ea-108">This setting is provided for backward compatibility only.</span></span> <span data-ttu-id="c10ea-109">否则不建议使用。</span><span class="sxs-lookup"><span data-stu-id="c10ea-109">Its use is otherwise not recommended.</span></span></blockquote> |
|<span data-ttu-id="c10ea-110">范围</span><span class="sxs-lookup"><span data-stu-id="c10ea-110">Scope</span></span>|<span data-ttu-id="c10ea-111">边缘</span><span class="sxs-lookup"><span data-stu-id="c10ea-111">Edge</span></span>|
|<span data-ttu-id="c10ea-112">版本</span><span class="sxs-lookup"><span data-stu-id="c10ea-112">Version</span></span>|<span data-ttu-id="c10ea-113">4.6</span><span class="sxs-lookup"><span data-stu-id="c10ea-113">4.6</span></span>|
|<span data-ttu-id="c10ea-114">类型</span><span class="sxs-lookup"><span data-stu-id="c10ea-114">Type</span></span>|<span data-ttu-id="c10ea-115">重定目标</span><span class="sxs-lookup"><span data-stu-id="c10ea-115">Retargeting</span></span>|
|<span data-ttu-id="c10ea-116">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="c10ea-116">Affected APIs</span></span>|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|
