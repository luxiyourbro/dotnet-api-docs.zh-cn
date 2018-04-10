### <a name="null-coalescer-values-are-not-visible-in-debugger-until-one-step-later"></a>Null 接合器值直至更高版本的一个步骤不在调试器中可见

|   |   |
|---|---|
|详细信息|.NET Framework 4.5 中的 bug 导致不能在调试器中可见的 framework 的 64 位版本上运行时执行赋值运算后立即通过 null 合并操作设置的值。|
|建议|单步执行在调试器中的一个额外的时间将会导致本地/字段的值正确更新。 此外，在.NET Framework 4.6 中; 中解决此问题升级到该版本的 Framework 应该可以解决此问题。|
|范围|边缘|
|版本|4.5|
|类型|运行时|

