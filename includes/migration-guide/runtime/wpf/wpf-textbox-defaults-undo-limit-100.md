### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a><span data-ttu-id="d0f19-101">WPF 文本框中默认为撤消 100 个的限制</span><span class="sxs-lookup"><span data-stu-id="d0f19-101">WPF TextBox defaults to undo limit of 100</span></span>

|   |   |
|---|---|
|<span data-ttu-id="d0f19-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="d0f19-102">Details</span></span>|<span data-ttu-id="d0f19-103">在 .NET 4.5 中，WPF 文本框的默认撤消限制是 100（.NET 4.0 则没有限制）</span><span class="sxs-lookup"><span data-stu-id="d0f19-103">In .NET 4.5, the default undo limit for a WPF textbox is 100 (as opposed to being unlimited in .NET 4.0)</span></span>|
|<span data-ttu-id="d0f19-104">建议</span><span class="sxs-lookup"><span data-stu-id="d0f19-104">Suggestion</span></span>|<span data-ttu-id="d0f19-105">如果一个撤消限制为 100 太低，可以显式设置限制与 <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit></span><span class="sxs-lookup"><span data-stu-id="d0f19-105">If an undo limit of 100 is too low, the limit can be set explicitly with <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit></span></span>|
|<span data-ttu-id="d0f19-106">范围</span><span class="sxs-lookup"><span data-stu-id="d0f19-106">Scope</span></span>|<span data-ttu-id="d0f19-107">边缘</span><span class="sxs-lookup"><span data-stu-id="d0f19-107">Edge</span></span>|
|<span data-ttu-id="d0f19-108">版本</span><span class="sxs-lookup"><span data-stu-id="d0f19-108">Version</span></span>|<span data-ttu-id="d0f19-109">4.5</span><span class="sxs-lookup"><span data-stu-id="d0f19-109">4.5</span></span>|
|<span data-ttu-id="d0f19-110">类型</span><span class="sxs-lookup"><span data-stu-id="d0f19-110">Type</span></span>|<span data-ttu-id="d0f19-111">运行时</span><span class="sxs-lookup"><span data-stu-id="d0f19-111">Runtime</span></span>|
|<span data-ttu-id="d0f19-112">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="d0f19-112">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

