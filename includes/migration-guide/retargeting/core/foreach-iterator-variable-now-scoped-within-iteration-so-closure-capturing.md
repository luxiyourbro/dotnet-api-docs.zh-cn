### <a name="foreach-iterator-variable-is-now-scoped-within-the-iteration-so-closure-capturing-semantics-are-different-in-c5"></a>Foreach 迭代器变量的作用域现在在迭代中，因此闭包捕获语义不同 （在 C# 5)

|   |   |
|---|---|
|详细信息|从 C# 5 (Visual Studio 2012)，开始<code>foreach</code>迭代器变量的作用域在迭代期内。 如果代码以前根据变量不包括在中，这可能会导致中断<code>foreach</code>的闭包。 此更改的症状是传递给委托的迭代器变量被视为创建它时具有委托的值，而不是它在调用委托时具有的值。|
|建议|理想情况下，应更新代码以使用新的编译器行为。 如果需要旧语义，迭代器变量可替换为显式置于循环范围外的单独变量。|
|范围|主要|
|版本|4.5|
|类型|重定目标|

