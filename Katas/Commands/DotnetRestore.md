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
