Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptChart / 方法 /
# ScriptChart.RemoveTiming(ScriptTiming) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

从谱面中移除一个Timing(时间点)脚本事件。

```csharp
public bool RemoveTiming(ScriptTiming timing);
```

## 参数
- ``timing`` [ScriptTiming](ScriptTiming.md)  
  要移除的Timing脚本事件。

## 返回
[bool](https://learn.microsoft.com/zh-cn/dotnet/api/system.boolean)  
  如果成功移除了指定的Timing脚本事件，则返回``true``；否则返回``false``。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |