Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptChart / 方法 /
# ScriptChart.RemoveTimingGroup(ScriptTimingGroup) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

从谱面中移除一个TimingGroup(时间组)。

```csharp
public bool RemoveTimingGroup(ScriptTimingGroup timingGroup);
```

## 参数
- ``timingGroup`` [ScriptTimingGroup](ScriptTimingGroup.md)  
  要移除的TimingGroup脚本事件。

## 返回
[bool](https://learn.microsoft.com/zh-cn/dotnet/api/system.boolean)  
  如果成功移除了指定的TimingGroup(时间组)脚本事件，则为``true``；否则为``false``。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |