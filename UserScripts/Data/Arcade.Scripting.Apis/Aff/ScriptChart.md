Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptChart 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个用于Lua脚本的Arcaea谱面对象。

```csharp
[MoonSharpUserData]
public sealed class ScriptChart : IDisposable
```

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object) -> **ScriptChart**

实现 [IDisposable](https://learn.microsoft.com/zh-cn/dotnet/api/system.idisposable)

## 注解
该类是所有通过Lua层对已加载的谱面进行CRUD(增删改查)操作的入口类，其为一个单例类，且在Lua层中无法直接创建新的实例（构造函数不对Lua层公开）。  
Lua层获取该类实例需要通过``ChartInstance``全局变量或[LoadActiveChart()](ScriptChart_LoadActiveChart.md)工厂方法进行。  
该类可看作是谱面对象 Arcade.Gameplay.Chart.ArcChart 的「脚本」封装，提供了对谱面中的所有事件进行操作的方法。  
若需要修改现有谱面元素，可先获取元素的脚本对象，然后修改其属性即可（修改会自动触发一个内部的通知事件，因此会自动更新到谱面对象中）。

## 属性
该类没有向脚本层公开的属性。

## 方法
| 方法名 | 说明 |
| -- | -- |
| [LoadActiveChart()](ScriptChart_LoadActiveChart.md) | 从当前已加载的谱面文件 ArcChart 对象创建用于脚本的谱面对象 ScriptChart。 |
| [Refresh()](ScriptChart_Refresh.md) | 刷新当前脚本谱面对象，将其与当前已加载的谱面文件对象同步。其作用等价于[Sync()](ScriptChart_Sync.md)。 |
| [Sync()](ScriptChart_Sync.md) | 将当前脚本谱面对象(ScriptChart)与已加载的最新谱面对象(ArcChart)同步。其作用等价于[Refresh()](ScriptChart_Refresh.md)。 |
| [Save()](ScriptChart_Save.md) | 保存谱面到文件。其作用等价于编辑器中单击保存按钮或按默认为``Ctrl+S``的快捷键。 |
| [SaveWithoutNotify()](ScriptChart_SaveWithoutNotify.md) | 保存谱面到文件，但不触发保存通知。 |
| [AddTiming(ScriptTiming)](ScriptChart_AddTiming.md) | 添加一个Timing(时间点)脚本事件到谱面中。 |
| [AddTap(ScriptTap)](ScriptChart_AddTap.md) | 添加一个Tap音符到谱面中。 |
| [AddHold(ScriptHold)](ScriptChart_AddHold.md) | 添加一个Hold音符到谱面中。 |
| [AddArc(ScriptArc)](ScriptChart_AddArc.md) | 添加一个Arc音符到谱面中。 |
| [AddTimingGroup(ScriptTimingGroup)](ScriptChart_AddTimingGroup.md) | 添加一个TimingGroup(时间组)到谱面中。 |
| [RemoveTiming(ScriptTiming)](ScriptChart_RemoveTiming.md) | 从谱面中移除一个Timing(时间点)脚本事件。 |
| [RemoveTap(ScriptTap)](ScriptChart_RemoveTap.md) | 从谱面中移除一个Tap音符。 |
| [RemoveHold(ScriptHold)](ScriptChart_RemoveHold.md) | 从谱面中移除一个Hold音符。 |
| [RemoveArc(ScriptArc)](ScriptChart_RemoveArc.md) | 从谱面中移除一个Arc音符。 |
| [RemoveTimingGroup(ScriptTimingGroup)](ScriptChart_RemoveTimingGroup.md) | 从谱面中移除一个TimingGroup(时间组)。 |
| [ViewEvents()](ScriptChart_ViewEvents.md) | 获取所有脚本事件(不包括[ScriptTimingGroup](ScriptTimingGroup.md))的只读视图。 |
| [ViewTimings()](ScriptChart_ViewTimings.md) | 获取所有脚本Timing(时间点)事件的只读视图。 |
| [ViewTaps()](ScriptChart_ViewTaps.md) | 获取所有脚本Tap音符的只读视图。 |
| [ViewHolds()](ScriptChart_ViewHolds.md) | 获取所有脚本Hold音符的只读视图。 |
| [ViewArcs()](ScriptChart_ViewArcs.md) | 获取所有脚本Arc音符的只读视图。 |
| [ViewCameras()](ScriptChart_ViewCameras.md) | 获取所有脚本Camera(相机动画)事件的只读视图。 |
| [ViewSceneControls()](ScriptChart_ViewSceneControls.md) | 获取所有脚本SceneControl(场景控制)事件的只读视图。 |
| [ViewTimingGroups()](ScriptChart_ViewTimingGroups.md) | 获取所有脚本TimingGroup(时间组)的只读视图。 |
| [ViewBasicObjects(GettableScriptObjectType)](ScriptChart_ViewBasicObjects.md) | 获取指定类型的基本脚本对象的只读视图。<br />GettableScriptObjectType枚举值可以是以下之一: ``Timing/Tap/Hold/Arc/Camera/SceneControl/TimingGroup/All``。 |

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |

## 另请参阅
- [ScriptTiming](ScriptTiming.md)
- [ScriptTap](ScriptTap.md)
- [ScriptHold](ScriptHold.md)
- [ScriptArc](ScriptArc.md)
- [ScriptCamera](ScriptCamera.md)
- [ScriptSceneControl](ScriptSceneControl.md)
- [ScriptTimingGroup](ScriptTimingGroup.md)