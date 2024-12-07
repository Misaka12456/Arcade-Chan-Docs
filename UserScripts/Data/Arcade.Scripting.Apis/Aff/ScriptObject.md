Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptObject 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

支持用于Lua脚本的所有脚本对象类。这是所有用户脚本对象类的最终基类；它是用户脚本类型层次结构的根。  
**注意：该类对Lua层并不可见，此处仅作为继承链的上游类型参考。**

```csharp
public abstract class ScriptObject
```

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object) -> **ScriptObject**

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |

## 另请参阅
- [ScriptEvent](ScriptEvent.md)
- [ScriptEvent&lt;TEvent, TRawEvent&gt;](ScriptEvent`2.md)
- [ScriptNote&lt;TNote, TRawNote&gt;](ScriptNote`2.md)