### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>不再能够 EnableViewStateMac 设置为 false

|   |   |
|---|---|
|详细信息|ASP.NET 不再允许开发者指定 <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> 或 <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>。 现在，针对所有带嵌入视图状态的请求强制执行视图状态消息身份验证代码 (MAC)。 只有应用程序显式将 EnableViewStateMac 属性设置为<code>false</code>会受到影响。|
|建议|必须假定 EnableViewStateMac 为 true，而产生的任何 MAC 错误必须先解决 (中所述[本指南](https://support.microsoft.com/kb/2915218)，其中包含具体什么原因导致 MAC 错误的多个解决方案)。|
|范围|主要|
|版本|4.5.2|
|类型|运行时|

