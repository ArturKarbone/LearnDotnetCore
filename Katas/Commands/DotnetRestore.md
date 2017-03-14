https://docs.microsoft.com/en-us/dotnet/articles/core/tools/dotnet-restore

- run dotnet restore in empty folder, at project level at solution level
- see output. pay attention to nuget configs


```
MSBUILD : error MSB1003: Specify a project or solution file. The current working directory does not contain a project or solution file.
```

```
  Restoring packages for C:\Artur\aspnetcore_basketservice\src\BasketService\BasketService.csproj...
  Lock file has not changed. Skipping lock file write. Path: C:\Artur\aspnetcore_basketservice\src\BasketService\obj\project.assets.json
  Restore completed in 1,3 sec for C:\Artur\aspnetcore_basketservice\src\BasketService\BasketService.csproj.

  NuGet Config files used:
      C:\Users\artur\AppData\Roaming\NuGet\NuGet.Config
      C:\Program Files (x86)\NuGet\Config\Microsoft.VisualStudio.Offline.config

  Feeds used:
      https://api.nuget.org/v3/index.json
      https://www.myget.org/F/aspnetvnext/api/v3/index.json
      C:\Program Files (x86)\Microsoft SDKs\NuGetPackages\
```


nuget.config at root level is going to be used:

```
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <add key="AkkaDotNetCore" value="https://www.myget.org/F/akka-netcore/api/v3/index.json" />
    <add key="NuGet" value="https://api.nuget.org/v3/index.json" />
  </packageSources>
</configuration>

```
- clean packages http://stackoverflow.com/questions/30933277/how-to-clear-nuget-package-cache-using-command-line
- where packages are stored http://stackoverflow.com/questions/35205092/net-core-and-nuget
- nuget locals global-packages -list

Errors when myget feed is commented out:

C:\Program Files\dotnet\sdk\1.0.0-rc4-004771\NuGet.targets(97,5): error : Unable to resolve 'Akka (>= 1.2.0-alpha1)' for '.NETCoreApp,Version=v1.0'. [C:\Artur\aspnetcore_basketservice\src\BasketService\BasketService.sln]
