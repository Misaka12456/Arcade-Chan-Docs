Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptTap 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个用于Lua脚本的脚本音符Tap。

```csharp
[MoonSharpUserData]
public sealed class ScriptTap : ScriptNote<Arcade.Gameplay.Chart.ArcTap, Arcade.Aff.RawAffTap>
```

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object) -> [ScriptObject](ScriptObject.md) -> [ScriptEvent](ScriptEvent.md) -> [ScriptEvent&lt;TEvent, TRawEvent&gt;](ScriptEvent`2.md) -> [ScriptNote&lt;TNote, TRawNote&gt;](ScriptNote`2.md) -> **ScriptTap**

## 注解
该类用于在脚本层表示Arcaea谱面中的Tap音符。

## 属性
| 属性名 | 类型 | 说明 |
| -- | -- | -- |
| ``Timing`` | int | 该音符的判定时间。 |
| ``Track`` | int | 该音符的轨道编号。默认范围1-4；6k环境下为0-5。 |
| ``TimingGroupIdx`` | int | 该音符所属的时间组(TimingGroup)的索引下标。对应时间组必须已经存在于谱面中。 |

## 方法
| 方法名 | 说明 |
| -- | -- |
| [Create(int, int, int)](ScriptTap_Create.md) |创建一个新的Tap脚本音符，并初始化其绑定的对象事件。 |

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |

## 另请参阅
- [ScriptChart](ScriptChart.md)