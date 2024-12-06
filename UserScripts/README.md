Arcade-Chan用户脚本(UserScript) 开发手册

``用户脚本``是一种可以在编辑器中运行的脚本，用于修改谱面。
它是一个强大的工具，可以帮助您在谱面上创建一些特定的谱面配置，或者以一些编辑器不直接支持的方式修改谱面。
要使用用户脚本，您需要确保您的Arcade-Chan是v3.3.0或更高版本。

``用户脚本``采用Lua语言，由MoonSharp提供基础支持。

请选择以下类型之一以查看详细手册：
| 类型名称 | 类型 | 描述 |
|:---|:---|:---|
|[``ScriptArc``](Data/Arcade.Scripting.Apis/Aff/ScriptArc.md)|类|表示一个用于Lua脚本的脚本音符Arc。|
|[``ScriptArcTap``](Data/Arcade.Scripting.Apis/Aff/ScriptArcTap.md)|类|表示一个用于Lua脚本的脚本音符ArcTap。该音符无法单独存在，其必须属于且仅属于一个音轨状态的Arc音符。|
|[``ScriptCamera``](Data/Arcade.Scripting.Apis/Aff/ScriptCamera.md)|类|表示一个用于Lua脚本的Camera(相机动画)脚本事件。|
|[``ScriptChart``](Data/Arcade.Scripting.Apis/Aff/ScriptChart.md)|类|表示一个用于Lua脚本的Arcaea谱面对象。|
|[``ScriptEvent``](Data/Arcade.Scripting.Apis/Aff/ScriptEvent.md)|类|表示一个用于Lua脚本的Arcaea脚本事件(Script Event)。该类为抽象类。|
|[``ScriptEvent<TEvent, TRawEvent>``](Data/Arcade.Scripting.Apis/Aff/ScriptEvent`2.md)|类|表示一个用于Lua脚本的泛型Arcaea脚本事件(Script Event)。该类为抽象类。|
|[``ScriptHold``](Data/Arcade.Scripting.Apis/Aff/ScriptHold.md)|类|表示一个用于Lua脚本的脚本音符Hold。|
|[``ScriptNote<TNote, TRawNote>``](Data/Arcade.Scripting.Apis/Aff/ScriptNote`2.md)|类|表示一个用于Lua脚本的脚本音符事件(Script Note)。该类为抽象类。|
|[``ScriptObject``](Data/Arcade.Scripting.Apis/Aff/ScriptObject.md)|类|表示用于Lua脚本的所有脚本对象的基类。|
|[``ScriptSceneControl``](Data/Arcade.Scripting.Apis/Aff/ScriptSceneControl.md)|类|表示一个用于Lua脚本的SceneControl(场景控制)脚本事件。|
|[``ScriptTap``](Data/Arcade.Scripting.Apis/Aff/ScriptTap.md)|类|表示一个用于Lua脚本的脚本音符Tap。|
|[``ScriptTiming``](Data/Arcade.Scripting.Apis/Aff/ScriptTiming.md)|类|表示一个用于Lua脚本的Timing(时间点)脚本事件。|
|[``ScriptTimingGroup``](Data/Arcade.Scripting.Apis/Aff/ScriptTimingGroup.md)|类|表示一个用于Lua脚本的TimingGroup(时间组)脚本事件。|