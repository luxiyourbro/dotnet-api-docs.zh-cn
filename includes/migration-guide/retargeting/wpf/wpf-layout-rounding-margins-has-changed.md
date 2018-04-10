### <a name="wpf-layout-rounding-of-margins-has-changed"></a>WPF 布局舍入的边距已更改

|   |   |
|---|---|
|详细信息|边距舍入的方式以及边框和边框内的背景已更改。 此更改的结果是：<ul><li>元素的宽度或高度最多可以扩大或收缩一个像素。</li><li>对象的位置最多可以移动一个像素。</li><li>居中的元素最多可以垂直或水平地偏离中心一个像素。</li></ul>默认情况下，仅对面向 .NET Framework 4.6 的应用启用此新布局。|
|建议|由于这种修改往往会消除的右侧或底部高 Dpi 处 WPF 控件的剪辑，面向早期版本的.NET Framework 但在.NET Framework 4.6 上运行的应用可选择加入此新行为将添加以下行将对<code>&lt;runtime&gt;</code> app.config 文件的部分：<code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=false&quot; /&gt;</code>应用面向.NET Framework 4.6 但希望 WPF 控件来呈现使用以前的布局算法可以执行操作来添加以下行将对<code>&lt;runtime&gt;</code>app.config 文件的部分：<code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=true&quot; /&gt;</code>.|
|范围|次要|
|版本|4.6|
|类型|重定目标|

