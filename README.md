# dotnet8_native_aot_example1

## 概要
.NET 8 のコンソールアプリで NativeAOT するサンプル 

## 詳細

```
dotnet new console
```

.csproj
```xml
  <PropertyGroup>
    <PublishAot>true</PublishAot>　★追加
  </PropertyGroup>
```

```
dotnet publish
```

↓ exe は約 1.5 MB
```
> dir

    Directory: dotnet8_native_aot_example1\bin\Release\net8.0\win-x64\publish

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a---          2024/01/03    15:05        1452544 dotnet8_native_aot_example1.exe
-a---          2024/01/03    15:05        8900608 dotnet8_native_aot_example1.pdb
```

ちゃんと動く
```
> .\dotnet8_native_aot_example1.exe
Hello, World!
```

## 環境

```
> dotnet --info
.NET SDK:
 Version:           8.0.100   
 Commit:            57efcf1350
 Workload version:  8.0.100-manifests.3b83835e

ランタイム環境:
 OS Name:     Windows   
 OS Version:  10.0.19045
 OS Platform: Windows   
 RID:         win-x64
 Base Path:   C:\Program Files\dotnet\sdk\8.0.100\

インストール済みの .NET ワークロード:
 Workload version: 8.0.100-manifests.3b83835e
```