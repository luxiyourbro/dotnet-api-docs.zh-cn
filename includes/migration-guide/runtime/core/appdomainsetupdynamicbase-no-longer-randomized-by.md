### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a>通过 UseRandomizedStringHashAlgorithm 不再随机 AppDomainSetup.DynamicBase

|   |   |
|---|---|
|详细信息|在.NET Framework 4.6 的值之前<xref:System.AppDomainSetup.DynamicBase>会将它随机应用程序域之间或进程，之间，如果在应用程序的配置文件中启用了 UseRandomizedStringHashAlgorithm。 从.NET Framework 4.6，开始<xref:System.AppDomainSetup.DynamicBase>的运行的应用程序，不同实例之间以及其他应用程序域之间，将返回一个稳定的结果。 动态基仍将不同于不同的应用程序;此更改仅删除相同的应用程序的不同实例的随机命名元素。|
|建议|请注意，允许<code>UseRandomizedStringHashAlgorithm</code>不会导致<xref:System.AppDomainSetup.DynamicBase>正在随机。 如果需要随机基，则必须在您的应用程序代码而不是通过此 API 生成它。|
|范围|边缘|
|版本|4.6|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|

