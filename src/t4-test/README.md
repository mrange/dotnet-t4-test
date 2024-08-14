# How to regen a t4 file using dotnet-t4 tool

## Restore all tools

```bash
# Will install the dotnet-t4 tool in this repo
dotnet tool restore
```

## Modify the T4 template file

Change t4it.tt(line 6) from:
```csharp
<# for (var i = 0; i < 24; ++i) { #>
``

To:

```csharp
<# for (var i = 0; i < 32; ++i) { #>
```

## Run dotnet-t4 on the T4 template

```bash
# Runs the t4 tool on t4it.tt
dotnet tool run t4 .\t4it.tt
```

You should now have some code changes thanks to our change earlier