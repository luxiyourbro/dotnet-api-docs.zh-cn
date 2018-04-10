### <a name="assemblies-compiled-with-regexcompiletoassembly-breaks-between-40-and-45"></a>具有 Regex.CompileToAssembly 4.0 和 4.5 之间的分隔线编译的程序集

|   |   |
|---|---|
|详细信息|如果已编译的正则表达式的程序集生成.NET Framework 4.5 但目标.NET Framework 4 中，尝试使用正则表达式之一，因为安装程序集具有.NET Framework 4 的系统上引发异常。|
|建议|若要解决此问题，可执行下列操作之一：<ul><li>生成包含.NET Framework 4 的正则表达式的程序集。</li><li>使用已解释的正则表达式。</li></ul>|
|范围|次要|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName)?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[])?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[],System.String)?displayProperty=nameWithType></li></ul>|

