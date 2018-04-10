### <a name="sharing-session-state-with-aspnet-stateserver-requires-all-servers-in-the-web-farm-to-use-the-same-net-framework-version"></a>与 Asp.Net StateServer 共享会话状态需要使用相同的.NET Framework 版本 web 场中所有服务器

|   |   |
|---|---|
|详细信息|启用时<xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=name>会话状态时，所有给定的 web 场中的服务器必须使用相同版本的.NET Framework 以使状态正确共享。|
|建议|请务必升级同时共享状态的 web 服务器上的.NET Framework 版本。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=nameWithType></li></ul>|

