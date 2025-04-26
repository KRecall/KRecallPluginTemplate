# Plugin Development Guide

## Create Plugin Class
as CaptureScreenByKDESpectaclePlugin class

must extend AbsCaptureScreenPlugin, other AbsPlugin or PluginBasic

must has a constructor with need metadata parameter

remember to add pluginClass to the pluginMetadata

remember changed your package name
```kotlin
package io.github.octestx.krecall.plugins.captureScreen.kdespectacle

class CaptureScreenByKDESpectaclePlugin(metadata: PluginMetadata): AbsCaptureScreenPlugin(metadata)
```

## Register Plugin
in the build.gradle file
add pluginMetadata to the plugin list
```kotlin
val plugins = listOf(
    PluginMetadata(
        pluginId = "CaptureScreenByKDESpectaclePlugin",
        supportPlatform = setOf(OS.LINUX),
        supportUI = true,
        pluginClass = "CaptureScreenByKDESpectaclePlugin"
    ),
)
```