Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptHold / 方法 /
# ScriptHold.Create(int, int, int, int) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

创建一个新的Hold脚本音符，并初始化其绑定的对象事件。

```csharp
public static ScriptHold Create(int timing, int endTiming, int track, int timingGroup = 0);
```

## 参数
- ``timing`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Hold的判定起始时间。
- ``endTiming`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Hold的判定结束时间。
- ``track`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Hold的所属整数轨道。
- ``timingGroup`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Hold所属的时间组(TimingGroup)的索引下标。默认为0(默认时间组)。

## 返回
[ScriptHold](ScriptHold.md)  
  创建的Hold脚本音符。

## 注解
该方法创建的 [ScriptHold](ScriptHold.md) 对象并不会自动添加并应用到谱面中，如需添加到谱面中请参考 [ScriptChart.AddHold(ScriptHold)](ScriptChart_AddHold.md) 方法。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |