Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptTiming / 方法 /
# ScriptTiming.Create(int, float, float, int) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

创建一个新的Timing(时间点)脚本事件。

```csharp
public static ScriptTiming Create(int timing, float bpm, float beats = 4f, int timingGroup = 0);
```

## 参数
- ``timing`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  时间点的时间(Time)参数。
- ``bpm`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  时间点的BPM(Beats Per Minute)。
- ``beats`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  时间点的每小节拍数。默认为4。
- ``timingGroup`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  时间点所属的时间组(TimingGroup)的索引下标。默认为0(默认时间组)。

## 返回
[ScriptTiming](ScriptTiming.md)
  创建的Timing(时间点)脚本事件。

## 注解
该方法创建的 [ScriptTiming](ScriptTiming.md) 对象并不会自动添加并应用到谱面中，如需添加到谱面中请参考 [ScriptChart.AddTiming(ScriptTiming)](ScriptChart_AddTiming.md) 方法。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |