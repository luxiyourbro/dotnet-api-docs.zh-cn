### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a>在注册表中注册自身时，.NET Framework 4.6 不使用 4.5.x.x 版本

|   |   |
|---|---|
|详细信息|如您所料，在注册表中设置版本键 (在<code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) 的.NET Framework 4.6 开始"4.6"，而不"4.5"。 应更新依赖于这些注册表项来了解在计算机上安装了哪些.NET Framework 版本的应用，以了解 4.6 是新的可能版本中，和一个与以前 4.5.x 兼容释放。|
|建议|通过查找 4.5 的注册表项来还接受 4.6 来安装更新应用探测的.NET Framework 4.5。|
|范围|边缘|
|版本|4.6|
|类型|运行时|

