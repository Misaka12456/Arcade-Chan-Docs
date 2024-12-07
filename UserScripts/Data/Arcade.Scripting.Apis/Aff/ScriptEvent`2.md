Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptEvent&lt;TEvent, TRawEvent&gt; 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个用于Lua脚本的泛型Arc脚本事件(Script Event)。  
该类为抽象类。

```csharp
[MoonSharpUserData]
public abstract class ScriptEvent<TEvent, TRawEvent> : ScriptEvent where TEvent : Arcade.Gameplay.Chart.ArcEvent, new() where TRawEvent : Arcade.Aff.IRawAffItem, new()
```

## 类型参数
- ``TEvent``  
  其对应的Arc对象事件类型。

- ``TRawEvent``  
  其对应的原始Aff事件类型。

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object) -> [ScriptObject](ScriptObject.md) -> [ScriptEvent](ScriptEvent.md) -> **ScriptEvent&lt;TEvent, TRawEvent&gt;**

## 属性
| 属性名 | 类型 | 说明 |
| -- | -- | -- |
| ``Timing`` | int | 该事件的触发(对于标准事件)/判定(对于音符类事件)时间。 |

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |

## 另请参阅
- [ScriptEvent](ScriptEvent.md)