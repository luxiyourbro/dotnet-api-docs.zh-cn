### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>如果使用 EntityDeploySplit 或 EntityClean 任务生成 edmx 实体框架 Visual Studio 2013 可能失败，错误 MSB4062

|   |   |
|---|---|
|详细信息|MSBuild 12.0 工具 （包括在 Visual Studio 2013） 更改 MSBuild 文件位置，从而导致较旧的实体框架目标文件无效。 结果是 <code>EntityDeploySplit</code> 和 <code>EntityClean</code> 任务失败，因为它们无法找到 <code>Microsoft.Data.Entity.Build.Tasks.dll</code>。 请注意，此中断由于工具集 (MSBuild/VS) 发生变化，不是由于.NET Framework 发生变化。 它仅在升级开发人员工具时才会发生，仅升级 .NET Framework 不会发生。|
|建议|实体框架的目标文件被固定的以便使用.NET Framework 4.6 中的新 MSBuild 布局开头。 升级到该版本的 Framework 将解决此问题。 或者，可使用[此](http://stackoverflow.com/a/24249247/131944)解决方法直接修补目标文件。|
|范围|主要|
|版本|4.5.1|
|类型|重定目标|

