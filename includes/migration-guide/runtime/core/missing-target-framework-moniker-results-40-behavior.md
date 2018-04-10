### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>缺少目标框架名字对象会导致 4.0 行为

|   |   |
|---|---|
|详细信息|没有应用程序<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>在使用.NET Framework 4.0 的语义 (quirks) 自动运行该程序集级别将应用。 若要确保高质量，建议所有二进制文件显式均归因与<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>表示它们生成所用的.NET framework 的版本。 请注意，在项目文件中使用的目标框架名字对象将导致 MSBuild 自动应用<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>。|
|建议|A<xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>应提供，通过将特性添加到程序集的直接或通过指定中的目标框架[项目文件或通过 Visual Studio 项目属性 GUI](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx)。|
|范围|主要|
|版本|4.5|
|类型|运行时|

