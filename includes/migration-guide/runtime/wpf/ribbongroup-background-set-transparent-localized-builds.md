### <a name="ribbongroup-background-is-set-to-transparent-in-localized-builds"></a>RibbonGroup 背景设置为透明的本地化版本

|   |   |
|---|---|
|详细信息|<xref:System.Windows.Controls.Ribbon.RibbonGroup?displayProperty=name> 本地化版本上的背景始终已绘制使用透明画笔，导致不佳的 UI 体验。 这固定在.NET 4.7 WPF 修复通过更新的本地化的资源<xref:System.Windows.Controls.Ribbon.RibbonGroup?displayProperty=name>，后者反过来确保选择正确的画笔。|
|建议|升级到.NET 4.7|
|范围|边缘|
|版本|4.6.2|
|类型|运行时|

