### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a>SqlBulkCopy 使用目标列编码为字符串

|   |   |
|---|---|
|详细信息|将数据插入列中时，<xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> 使用目标列的编码而不是 <code>VARCHAR</code> 和 <code>CHAR</code> 类型的默认编码。 在目标列未使用默认编码时，此更改会消除使用此默认编码所引起的数据损坏的可能性。 在极少数情况下，现有的应用程序可能会引发 SqlException 异常，如果在编码的更改所生成太大，无法适应目标列的数据。|
|建议|预计<xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name>将不再损坏数据，由于编码的差异。 如果要将复制接近目标列的大小限制的字符串，可能需要也预编码 （要复制数据以检查数据将适应目标列中） 或通过捕获由于<xref:System.Data.SqlClient.SqlException?displayProperty=name>s。|
|范围|边缘|
|版本|4.5|
|类型|运行时|
|受影响的 API|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|

