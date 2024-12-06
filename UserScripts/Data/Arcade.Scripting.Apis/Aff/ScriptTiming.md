Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptTiming 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个用于Lua脚本的Timing(时间点)脚本事件。

```csharp
[MoonSharpUserData]
public sealed class ScriptTiming : ScriptEvent<Arcade.Gameplay.Chart.ArcTiming, Arcade.Aff.RawAffTiming>
```

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object) -> [ScriptObject](ScriptObject.md) -> [ScriptEvent](ScriptEvent.md) -> [ScriptEvent&lt;TEvent, TRawEvent&gt;](ScriptEvent`2.md) -> **ScriptTiming**

## 注解
该类用于在脚本层表示Arcaea谱面中的Timing事件。

## 属性
| 属性名 | 类型 | 说明 |
| -- | -- | -- |
| ``Timing`` | int | 该事件的触发时间。 |
| ``BPM`` | float | 从该时间点开始的BPM(Beats Per Minute)。 |
| ``Beats`` | float | 从该时间点开始的每小节拍数。 |
| ``TimingGroupIdx`` | int | 该时间点所属的时间组(TimingGroup)的索引下标。对应时间组必须已经存在于谱面中。 |

## 方法
| 方法名 | 说明 |
| -- | -- |
| [Create(int, float, float, int)](ScriptTiming_Create.md) | 创建一个新的Timing(时间点)脚本事件。 |

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |

## 另请参阅
- [ScriptTimingGroup](ScriptTimingGroup.md)
- [ScriptChart](ScriptChart.md)