### <a name="ipad-should-not-be-used-in-custom-capabilities-file-because-it-is-now-a-browser-capability"></a>不 IPad 应使用在自定义功能文件中，因为它现在是浏览器功能

|   |   |
|---|---|
|详细信息|从.NET 4.5 开始，iPad 是标识符在默认 ASP.NET 浏览器的功能文件中，因此它不应使用自定义功能文件中|
|建议|如果特定于 iPad 的功能是必需的则必须通过在预定义的网关 refID 上设置功能来修改 iPad 行为&quot;IPad&quot;而不是通过生成一个新&quot;IPad&quot;用户代理 ID匹配。|
|范围|边缘|
|版本|4.5|
|类型|运行时|

