### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a>阻止托管浏览器从.NET Framework 1.1 和 2.0 的宿主控件

|   |   |
|---|---|
|详细信息|Internet Explorer 中阻止对这些控件的承载。|
|建议|Internet Explorer 将无法启动使用用于承载控件的托管浏览器的应用程序。 可以通过设置注册表子项的 EnableIEHosting 值还原以前的行为<code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code>到<code>1</code>针对 x86 系统和 x64 上的 32 位进程系统，并通过设置<code>EnableIEHosting</code>值的注册表子项<code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>到<code>1</code>针对 x64 上的 64 位进程系统。|
|范围|次要|
|版本|4.5|
|类型|运行时|

