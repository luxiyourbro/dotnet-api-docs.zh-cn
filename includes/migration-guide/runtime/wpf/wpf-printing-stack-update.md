### <a name="wpf-printing-stack-update"></a>WPF 打印堆栈更新

|   |   |
|---|---|
|详细信息|WPF 的打印 Api 使用<xref:System.Printing.PrintQueue?displayProperty=name>现在调用窗口打印文档包现已弃用的 XPS 打印 API 支持的 API。 更改与记住; 的可维护性用户和开发人员都不应该看到中行为或 API 使用的任何更改。 在 Windows 10 创建者更新中运行时，将默认启用新的打印堆栈。 旧的打印堆栈仍将继续在较旧版本的 Windows 像以前那样工作。|
|建议|若要使用 Windows 10 创建者更新旧的堆栈，设置<code>UseXpsOMPrinting</code>REG_DWORD 值<code>HKEY_CURRENT_USER\Software\Microsoft\.NETFramework\Windows Presentation Foundation\Printing</code>注册表项设置为<code>1</code>。|
|范围|边缘|
|版本|4.7|
|类型|运行时|

