Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptArc 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个用于Lua脚本的脚本音符Arc。

```csharp
[MoonSharpUserData]
public sealed class ScriptArc : ScriptNote<Arcade.Gameplay.Chart.ArcArc, Arcade.Aff.RawAffArc>
```

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object?view=latest) -> [ScriptObject](ScriptObject.md) -> [ScriptEvent](ScriptEvent.md) -> [ScriptEvent&lt;TEvent, TRawEvent&gt;](ScriptEvent`2.md) -> [ScriptNote&lt;TNote, TRawNote&gt;](ScriptNote`2.md) -> **ScriptArc**

## 注解
该类用于在脚本层表示Arcaea谱面中的Arc音符。

## 属性
| 属性名 | 类型 | 说明 |
| -- | -- | -- |
| ``Timing`` | int | 该音符的起始时间。 |
| ``TimingGroupIdx`` | int | 该音符所属的时间组(TimingGroup)的索引下标。对应时间组必须已经存在于谱面中。 |
| ``EndTiming`` | int | 该音符的结束时间。 |
| ``Color`` | int | 该音符的颜色。0=蓝，1=红，2=绿，3=灰/白(持续时间0ms的3号颜色Arc会视为可变长度的ArcTap处理)。 |
| ``XStart`` | float | 该音符的起始X坐标。 |
| ``XEnd`` | float | 该音符的结束X坐标。 |
| ``YStart`` | float | 该音符的起始Y坐标。 |
| ``YEnd`` | float | 该音符的结束Y坐标。 |
| ``LineType`` | Arcade.Gameplay.ArcLineType | 该Arc音符的音弧缓动(曲线)形态。<br />可选 ``S/B/Si/So/SiSi/SiSo/SoSi/SoSo``中任意一值。 |
| ``VoidType`` | Arcade.Aff.VoidType | 该Arc音符的音轨状态类型。<br />可选 ``Solid/Void/VoidDesignant``中任意一值。 |
| ``Effect`` | string | 其上的ArcTap音符的特殊音效(Sfx)参数。<br />若值不为none，其上所有的ArcTap都会表示为SfxArcTap的样式，并且单击判定成功时播放Effect所指的音效wav文件，而非正常的点击音效(hitsound)。<br />(文件名中"."用"_"代替, 例如"kick_wav"表示音效是项目文件夹下的kick.wav) |
| ``ArcTaps`` | [ObservableCollection&lt;ScriptArcTap&gt;](https://docs.microsoft.com/zh-cn/dotnet/api/system.collections.objectmodel.observablecollection-1?view=latest) | 该Arc音符上的所有ArcTap音符。<br />只要存在附属ArcTap，若 ``VoidType`` 的值为 ``VoidType.Solid``，该Arc音符也会被视为音轨(Trace/Vold)处理【即视 ``VoidType`` 为 ``VoidType.Void``】。 |

## 方法
| 方法名 | 说明 |
| -- | -- |
| [Create(int, int, int, float, float, float, float, ArcLineType, ArcVoidType, string, int, DynValue)](ScriptArc_Create.md) | 创建一个新的Arc(音弧)脚本音符，并初始化其绑定的对象事件。 |
| [AddArcTap(int)](ScriptArc_AddArcTap.md) | 添加一个脚本音符ArcTap到该脚本音符Arc上。 |
| [RemoveArcTap(int)](ScriptArc_RemoveArcTap.md#Overload_int) | 从该脚本音符Arc上移除一个指定判定时间的ArcTap。 |
| [RemoveArcTap(ScriptArcTap)](ScriptArc_RemoveArcTap.md#Overload_ScriptArcTap) | 从该脚本音符Arc上移除一个ArcTap。 |
| [RemoveArcTaps(Predicate&lt;ScriptArcTap&gt;)](ScriptArc_RemoveArcTaps.md) | 从该脚本音符Arc上移除所有满足条件的ArcTap。 |

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |

## 另请参阅
- [ScriptArcTap](ScriptArcTap.md)
- [ScriptChart](ScriptChart.md)