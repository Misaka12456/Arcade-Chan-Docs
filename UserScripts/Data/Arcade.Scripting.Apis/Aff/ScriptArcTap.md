Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptArcTap 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个用于Lua脚本的脚本音符ArcTap。  
该音符无法单独存在，其必须属于且仅属于一个音轨状态的Arc音符。  
(若其属于了一个音弧状态的Arc音符，则对应Arc音符会直接视为音轨状态处理)

```csharp
[MoonSharpUserData]
public sealed class ScriptArcTap : ScriptEvent
```

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object) -> [ScriptObject](ScriptObject.md) -> [ScriptEvent](ScriptEvent.md) -> **ScriptArcTap**

## 注解
该类用于在脚本层表示Arcaea谱面中的ArcTap音符。

## 属性
| 属性名 | 类型 | 说明 |
| -- | -- | -- |
| ``Timing`` | int | 该音符的判定时间。 |

## 方法
| 方法名 | 说明 |
| -- | -- |
| [Create(ScriptArc, int)](ScriptArcTap_Create.md) | 使用指定的父脚本音符Arc和判定时间创建一个新的ArcTap脚本音符。 |

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |

## 另请参阅
- [ScriptArc](ScriptArc.md)
- [ScriptChart](ScriptChart.md)