### <a name="chained-popups-with-staysopenfalse"></a>链接与 StaysOpen 的弹出窗口 = False

|   |   |
|---|---|
|详细信息|弹出一个 StaysOpen = False 应该关闭弹出项外部单击时。 当链接两个或多个此类显示弹出窗口 （即有一个包含另一个），没有很多问题，包括：<ul><li>打开两个级别，单击位于 P2 外部，但在 P1。  不发生任何事件。</li><li>打开两个级别，单击外部 P1。  这两个弹出窗口关闭。</li><li>打开和关闭两个级别。  然后尝试再次打开 P2。  不发生任何事件。</li><li>尝试打开三个级别。  你不能。  （不执行任何操作或关闭的前两个级别，具体取决于您单击的位置。）这种情况下 （和其他变体） 现在按预期方式工作。</li></ul>|
|范围|边缘|
|版本|4.7.1|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|

