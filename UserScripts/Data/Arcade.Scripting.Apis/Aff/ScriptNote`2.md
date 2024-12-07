Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptNote&lt;TNote, TRawNote&gt; 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个用于Lua脚本的脚本音符事件(Script Note)。  
该类为抽象类。

```csharp
[MoonSharpUserData]
public abstract class ScriptNote<TNote, TRawNote> : ScriptEvent<TNote, TRawNote> where TNote : Arcade.Gameplay.Chart.ArcNote, new() where TRawNote : Arcade.Aff.IRawAffItem, new()
```

## 类型参数
- ``TNote``  
  其对应的Arc音符(对象事件)类型。

- ``TRawNote``  
  其对应的Arc音符(原始Aff事件)类型。

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object) -> [ScriptObject](ScriptObject.md) -> [ScriptEvent](ScriptEvent.md) -> [ScriptEvent&lt;TEvent, TRawEvent&gt;](ScriptEvent`2.md) -> **ScriptNote&lt;TNote, TRawNote&gt;**

## 属性
| 属性名 | 类型 | 说明 |
| -- | -- | -- |
| ``TimingGroupIdx`` | int | 该音符所属的时间组(TimingGroup)的索引下标。对应时间组必须已经存在于谱面中。 |

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |

## 另请参阅
- [ScriptTap](ScriptTap.md)
- [ScriptHold](ScriptHold.md)
- [ScriptArc](ScriptArc.md)