### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a><span data-ttu-id="988c6-101">WPF 列表框、 列表视图或选中项的 DataGrid 上的调用 Items.Refresh 可能导致重复的项显示在元素</span><span class="sxs-lookup"><span data-stu-id="988c6-101">Calling Items.Refresh on a WPF ListBox, ListView, or DataGrid with items selected can cause duplicate items to appear in the element</span></span>

|   |   |
|---|---|
|<span data-ttu-id="988c6-102">详细信息</span><span class="sxs-lookup"><span data-stu-id="988c6-102">Details</span></span>|<span data-ttu-id="988c6-103">在.NET Framework 4.5，而在中选择项从代码调用 ListBox.Items.Refresh<xref:System.Windows.Controls.ListBox?displayProperty=name>可能会导致在列表中复制所选的项目。</span><span class="sxs-lookup"><span data-stu-id="988c6-103">In the .NET Framework 4.5, calling ListBox.Items.Refresh from code while items are selected in a <xref:System.Windows.Controls.ListBox?displayProperty=name> can cause the selected items to be duplicated in the list.</span></span> <span data-ttu-id="988c6-104">使用时出现类似问题<xref:System.Windows.Controls.ListView?displayProperty=name>和<xref:System.Windows.Controls.DataGrid?displayProperty=name>。</span><span class="sxs-lookup"><span data-stu-id="988c6-104">A similar issue occurs with <xref:System.Windows.Controls.ListView?displayProperty=name> and <xref:System.Windows.Controls.DataGrid?displayProperty=name>.</span></span> <span data-ttu-id="988c6-105">此问题已在 .NET Framework 4.6 中解决。</span><span class="sxs-lookup"><span data-stu-id="988c6-105">This is fixed in the .NET Framework 4.6.</span></span>|
|<span data-ttu-id="988c6-106">建议</span><span class="sxs-lookup"><span data-stu-id="988c6-106">Suggestion</span></span>|<span data-ttu-id="988c6-107">通过以编程方式取消之前的项的选中情况下，此问题可能会得到解决<xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name>调用，并且在调用完成后再重新选择它们。</span><span class="sxs-lookup"><span data-stu-id="988c6-107">This issue may be worked around by programatically unselecting items before <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> is called and then re-selecting them after the call is completed.</span></span> <span data-ttu-id="988c6-108">此外，此问题已在 .NET Framework 4.6 中解决，因此升级到该版本的 .NET Framework 即可解决该问题。</span><span class="sxs-lookup"><span data-stu-id="988c6-108">Alternatively, this issue has been fixed in the .NET Framework 4.6 and may be addressed by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="988c6-109">范围</span><span class="sxs-lookup"><span data-stu-id="988c6-109">Scope</span></span>|<span data-ttu-id="988c6-110">次要</span><span class="sxs-lookup"><span data-stu-id="988c6-110">Minor</span></span>|
|<span data-ttu-id="988c6-111">版本</span><span class="sxs-lookup"><span data-stu-id="988c6-111">Version</span></span>|<span data-ttu-id="988c6-112">4.5</span><span class="sxs-lookup"><span data-stu-id="988c6-112">4.5</span></span>|
|<span data-ttu-id="988c6-113">类型</span><span class="sxs-lookup"><span data-stu-id="988c6-113">Type</span></span>|<span data-ttu-id="988c6-114">运行时</span><span class="sxs-lookup"><span data-stu-id="988c6-114">Runtime</span></span>|
|<span data-ttu-id="988c6-115">受影响的 API</span><span class="sxs-lookup"><span data-stu-id="988c6-115">Affected APIs</span></span>|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|
