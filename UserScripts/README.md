Arcade-Chan用户脚本(UserScript) 开发手册

``用户脚本``是一种可以在编辑器中运行的脚本，用于修改谱面。
它是一个强大的工具，可以帮助您在谱面上创建一些特定的谱面配置，或者以一些编辑器不直接支持的方式修改谱面。
要使用用户脚本，您需要确保您的Arcade-Chan是v3.3.0或更高版本。

``用户脚本``采用Lua语言，由MoonSharp提供基础支持。

每个用户脚本需要包含如下格式的内容：
```lua
ScriptInfo = {
	id = "脚本ID，用于唯一标识脚本",
	title = "脚本标题",
	desc = "脚本描述",
	author = "脚本作者",
	version = "脚本版本",
	compatibility = "兼容性检查代码",
	arguments = { 脚本入口点方法ScriptMain的形参列表 }
}

function ScriptMain()
	-- 脚本主体
end
```

例如：
```lua
ScriptInfo = {
	id = "moe.misakacastle.adechan.script.example",
	title = "用户脚本示例",
	desc = "这是一个用户脚本示例。它会在给定的时间点在给定轨道上添加一个Tap音符。",
	author = "Misaka Castle",
	version = "0.1.0",
	compatibility = "Arcade-Chan>=3.3.0",
	arguments = {
		{
			type = "number", -- 支持number/string/boolean
			name = "时间点",
			required = true
		},
		{
			type = "number",
			name = "轨道",
			required = false,
			default = 1
		}
	}
}

function ScriptMain(...)
	local args = {...}
	local timing = args[1]
	local track = args[2] or 1

	local chart = ChartInstance
	local tap = ScriptTap.Create(timing, track)
	chart:AddTap(tap)
end
```


请选择一个命名空间查看详细手册：
| 命名空间 | 说明 |
|:--|:--|
| [Arcade.Scripting.Apis](Data/Arcade.Scripting.Apis/README.md) | 提供所有用于Lua脚本的API类。 |
| [Arcade.Scripting.Apis.Aff](Data/Arcade.Scripting.Apis/Aff/README.md) | 包含所有可在Lua层使用的Arcade-Chan谱面数据的API类。这些类允许脚本开发者从Lua层读写已加载的Arcaea谱面(.aff)的各种信息。 |