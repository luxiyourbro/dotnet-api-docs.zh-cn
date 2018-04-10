### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a>COR_PRF_GC_ROOT_HANDLEs 不会使用探查器正在枚举

|   |   |
|---|---|
|详细信息|在.NET Framework v4.5.1，分析 API<code>RootReferences2()</code>永远不会错误地返回<code>COR_PRF_GC_ROOT_HANDLE</code>(作为返回<code>COR_PRF_GC_ROOT_OTHER</code>相反)。 开始在.NET Framework 4.6 中修复此问题。|
|建议|此问题已修复在.NET Framework 4.6 中，并可以通过升级到该版本的.NET Framework 进行寻址。|
|范围|次要|
|版本|4.5.1|
|类型|运行时|

