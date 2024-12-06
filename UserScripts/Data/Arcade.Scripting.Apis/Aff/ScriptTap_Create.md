Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptTap / 方法 /
# ScriptTap.Create(int, int, int) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

创建一个新的Tap脚本音符，并初始化其绑定的对象事件。

```csharp
public static ScriptTap Create(int timing, int track, int timingGroup = 0);
```

## 参数
- ``timing`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Tap的判定时间。
- ``track`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Tap的所属整数轨道。
- ``timingGroup`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Tap所属的时间组(TimingGroup)的索引下标。默认为0(默认时间组)。

## 返回
[ScriptTap](ScriptTap.md)  
  创建的Tap脚本音符。

## 注解
该方法创建的 [ScriptTap](ScriptTap.md) 对象并不会自动添加并应用到谱面中，如需添加到谱面中请参考 [ScriptChart.AddTap(ScriptTap)](ScriptChart_AddTap.md) 方法。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |