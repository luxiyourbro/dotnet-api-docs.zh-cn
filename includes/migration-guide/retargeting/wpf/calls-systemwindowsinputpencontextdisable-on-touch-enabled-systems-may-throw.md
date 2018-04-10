### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>对 System.Windows.Input.PenContext.Disable 触控的系统上的调用可能会引发 ArgumentException

|   |   |
|---|---|
|详细信息|在某些情况下，调用到内部<strong>System.Windows.Intput.PenContext.Disable</strong>触控的系统上的方法可能会引发未处理<code>T:System.ArgumentException</code>由于重新进入。|
|建议|在.NET Framework 4.7 中已得到解决此问题。 若要避免此异常，升级到.NET Framework 4.7 从.NET Framework 的版本。|
|范围|边缘|
|版本|4.6.1|
|类型|重定目标|

