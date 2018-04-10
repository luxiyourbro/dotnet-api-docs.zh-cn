### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a>分析 ASP.Net MVC4 应用程序可能会导致执行引擎错误

|   |   |
|---|---|
|详细信息|使用 NGEN /Profile 程序集的探查器可能会崩溃进行事件探查的 ASP.NET MVC4 应用程序在启动时出现致命执行引擎异常|
|建议|在.NET Framework 4.5.2 中修复此问题。 或者，探查器可以避免此问题，通过指定<code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code>其事件掩码中。|
|范围|边缘|
|版本|4.5|
|类型|运行时|

