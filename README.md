## SpaceWarp PluginInfo generator

Generates `MyPluginInfo.cs` based on MSBuild properties.

This is a version of
[BepInEx.PluginInfoProps](https://github.com/BepInEx/BepInEx.Templates/blob/master/BepInEx.PluginInfoProps/README.md)
specifically modified for use with SpaceWarp.Template, and all credit goes to the original authors.

## Basic usage

Define the following properties in your project:

```xml
<AssemblyName>Example.Plugin</AssemblyName>
<Product>My first plugin</Product>
<Version>1.0.0</Version>
```

this will generate the following class:

```cs
using System;

internal static class MyPluginInfo
{
    /// <summary>
    /// The GUID of the plugin.
    /// </summary>
    public const string PLUGIN_GUID = "Example.Plugin";
    /// <summary>
    /// The name of the plugin.
    /// </summary>
    public const string PLUGIN_NAME = "My first plugin";
    /// <summary>
    /// The version of the plugin.
    /// </summary>
    public const string PLUGIN_VERSION = "1.0.0";
}
```