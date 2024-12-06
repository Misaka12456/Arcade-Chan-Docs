Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptArc / 方法 /
# ScriptArc.Create(int, int, int, float, float, float, float, ArcLineType, ArcVoidType, string, int, DynValue) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

创建一个新的Arc(音弧)脚本音符，并初始化其绑定的对象事件。

```csharp
public static ScriptArc Create(int timing, int endtiming, int color, float xStart, float xEnd, float yStart, float yEnd, ArcLineType lineType, ArcVoidType voidType, string effect = "none", int timingGroup = 0, DynValue arctaps = null);
```

## 参数
- ``timing`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Arc的起始时间。
- ``endtiming`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Arc的结束时间。
- ``color`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Arc的颜色。可选值为0=蓝，1=红，2=绿，3=灰/白(持续时间0ms的3号颜色Arc会视为可变长度的ArcTap处理)。
- ``xStart`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  Arc的起始X坐标。
- ``xEnd`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  Arc的结束X坐标。
- ``yStart`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  Arc的起始Y坐标。
- ``yEnd`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  Arc的结束Y坐标。
- ``lineType`` ArcLineType  
  Arc的音弧缓动(曲线)形态。可选值为【基础】S/B/Si/So和【高级】SiSi/SiSo/SoSi/SoSo八种缓动形态之一。
- ``voidType`` ArcVoidType  
  Arc音符的音轨状态类型。可选值为Solid/Void和VoidDesignant三种状态之一。
- ``effect`` [string](https://docs.microsoft.com/zh-cn/dotnet/api/system.string)  
  其上的ArcTap音符的特殊音效(Sfx)参数。默认为"none"(即无特殊音效)。
- ``timingGroup`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  Arc所属的时间组(TimingGroup)的索引下标。默认为0(默认时间组)。
- ``arctaps`` DynValue (Lua层为``Table``，列表形态，元素为[ScriptArcTap](ScriptArcTap.md))  
  其上的所有ArcTap音符。可选参数。默认为空列表(即该Arc音符不存在任何附属ArcTap)。

## 返回
[ScriptArc](ScriptArc.md)  
  创建的Arc(音弧)脚本音符。

## 异常
[ArgumentOutOfRangeException](https://docs.microsoft.com/zh-cn/dotnet/api/system.argumentoutofrangeexception)  
  时间组索引下标超出现有时间组列表的范围。

## 注解
该方法创建的 [ScriptArc](ScriptArc.md) 对象并不会自动添加并应用到谱面中，如需添加到谱面中请参考 [ScriptChart.AddArc(ScriptArc)](ScriptChart_AddArc.md) 方法。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |