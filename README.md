# Xamarin NativeReferences Bug

Run the build:

```
msbuild /restore /t:pack /bl
```

Observe the error:

```
"/Users/matthew/Projects/Testing/XamarinNativeReferences/XamarinNativeReferences.sln" (pack target) (1:2) ->
"/Users/matthew/Projects/Testing/XamarinNativeReferences/source/Square.CoreAardvark/Square.CoreAardvark.csproj" (pack target) (2:15) ->
(GenerateNuspec target) -> 
  /usr/local/share/dotnet/sdk/3.0.100-preview6-012264/Sdks/NuGet.Build.Tasks.Pack/buildCrossTargeting/NuGet.Build.Tasks.Pack.targets(198,5): error : The file '/Users/matthew/Projects/Testing/XamarinNativeReferences/source/Square.CoreAardvark/bin/Debug/xamarinios1.0/Native.Square.CoreAardvark.manifest' to be packed was not found on disk. [/Users/matthew/Projects/Testing/XamarinNativeReferences/source/Square.CoreAardvark/Square.CoreAardvark.csproj]

"/Users/matthew/Projects/Testing/XamarinNativeReferences/XamarinNativeReferences.sln" (pack target) (1:2) ->
"/Users/matthew/Projects/Testing/XamarinNativeReferences/source/Square.Aardvark/Square.Aardvark.csproj" (pack target) (3:11) ->
  /usr/local/share/dotnet/sdk/3.0.100-preview6-012264/Sdks/NuGet.Build.Tasks.Pack/buildCrossTargeting/NuGet.Build.Tasks.Pack.targets(198,5): error : The file '/Users/matthew/Projects/Testing/XamarinNativeReferences/source/Square.Aardvark/bin/Debug/xamarinios1.0/Native.Square.Aardvark.manifest' to be packed was not found on disk. [/Users/matthew/Projects/Testing/XamarinNativeReferences/source/Square.Aardvark/Square.Aardvark.csproj]
```

See also: https://github.com/onovotny/MSBuildSdkExtras/issues/176
