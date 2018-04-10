### <a name="wpf-spell-checking-in-text-enabled-controls-will-not-work-in-windows-10-for-languages-not-in-the-oss-input-language-list"></a>WPF 拼写检查启用文本的控件中将不适合 Windows 10 中的操作系统的输入的语言列表中没有的语言

|   |   |
|---|---|
|详细信息|Windows 10 上运行时，拼写检查器可能无法 WPF 文本启用控件的工作，因为平台拼写检查功能仅适用于输入的语言列表中存在的语言。在 Windows 10 中，一种语言添加到可用键盘列表时 Windows 自动下载并安装相应的功能按需 (FOD) 包，以提供拼写检查功能。 通过将语言添加到输入语言列表，将支持拼写检查器。|
|建议|请注意，必须作为一种输入语言进行拼写检查 Windows 10 中的工作添加的语言或文本进行拼写检查。|
|范围|边缘|
|版本|4.6|
|类型|运行时|

