Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptSceneControl 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个用于Lua脚本的SceneControl(场景控制)脚本事件。

```csharp
[MoonSharpUserData]
public sealed class ScriptSceneControl : ScriptEvent<Arcade.Gameplay.Chart.ArcSceneControl, Arcade.Aff.RawAffSceneControl>
```

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object) -> [ScriptObject](ScriptObject.md) -> [ScriptEvent](ScriptEvent.md) -> [ScriptEvent&lt;TEvent, TRawEvent&gt;](ScriptEvent`2.md) -> **ScriptSceneControl**

## 注解
该类用于在脚本层表示Arcaea谱面中的SceneControl事件。  
**该类仅用于只读谱面中已有的SceneControl事件，暂不支持创建新的或修改现有的SceneControl事件。**

## 属性
| 属性名 | 类型 | 说明 |
| -- | -- | -- |
| ``SCType`` | Arcade.Gameplay.Chart.SceneControlType | 场景控制事件的类型。<br />可选``TrackHide/TrackShow/HideGroup/TrackDisplay/EnwidenCamera/EnwidenLanes``中任意一值。 |
| ``FloatArg`` | float | 场景控制的浮点参数(参数1)。 |
| ``IntArg`` | int | 场景控制的整数参数(参数2)。 |
| ``TimingGroupIdx`` | int | 场景控制所属的时间组(TimingGroup)的索引下标。对应时间组必须已经存在于谱面中。 |

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |

## 另请参阅
- [ScriptChart](ScriptChart.md)