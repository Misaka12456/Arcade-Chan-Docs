Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptCamera 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个用户Lua脚本的Camera(相机动画)脚本事件。

```csharp
[MoonSharpUserData]
public sealed class ScriptCamera : ScriptEvent<Arcade.Gameplay.Chart.ArcCamera, Arcade.Aff.RawAffCamera>
```

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object) -> [ScriptObject](ScriptObject.md) -> [ScriptEvent](ScriptEvent.md) -> [ScriptEvent&lt;TEvent, TRawEvent&gt;](ScriptEvent`2.md) -> **ScriptCamera**

## 注解
该类用于在脚本层表示Arcaea谱面中的Camera事件。  
**该类仅用于只读谱面中已有的Camera事件，暂不支持创建新的或修改现有的Camera事件。**

## 属性
| 属性名 | 类型 | 说明 |
| -- | -- | -- |
| ``MoveX`` | float | 相机动画的X轴移动量(相对于世界坐标系)。 |
| ``MoveY`` | float | 相机动画的Y轴移动量(相对于世界坐标系)。 |
| ``MoveZ`` | float | 相机动画的Z轴移动量(相对于世界坐标系)。 |
| ``RotateX`` | float | 相机动画的X轴旋转量(相对于世界坐标系)。 |
| ``RotateY`` | float | 相机动画的Y轴旋转量(相对于世界坐标系)。 |
| ``RotateZ`` | float | 相机动画的Z轴旋转量(相对于世界坐标系)。 |
| ``EaseType`` | string | 相机动画的缓动类型。<br />可选``l/s/qi/qo/reset``中任意一值。 |
| ``Duration`` | int | 相机动画的持续时间，以毫秒(ms)为单位。 |
| ``TimingGroupIdx`` | int | 相机动画所属的时间组(TimingGroup)的索引下标。对应时间组必须已经存在于谱面中。 |

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.3+ |

## 另请参阅
- [ScriptChart](ScriptChart.md)