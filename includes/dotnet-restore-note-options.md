> [!NOTE]
> 从.NET 核心 2.0 开始，你不需要运行[ `dotnet restore` ](~/docs/core/tools/dotnet-restore.md)因为它是隐式运行的所有命令，如`dotnet build`和`dotnet run`，需要进行还原。 它仍是一个有效的命令，在某些情况下，其中执行操作的显式还原功能很有用，如[持续集成生成在 Visual Studio Team Services](/vsts/build-release/apps/aspnet/build-aspnet-core)或需要显式控制的时间的生成系统中进行恢复。
>
> 此命令还支持`dotnet restore`选项传入的长格式 (例如， `--source`)。 缩写形式选项，如`-s`，不支持。