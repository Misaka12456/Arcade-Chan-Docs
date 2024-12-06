Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptChart / 方法 /
# ScriptChart.RemoveTap(ScriptTap) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

从谱面中移除一个Tap音符。

```csharp
public bool RemoveTap(ScriptTap tap);
```

## 参数
- ``tap`` [ScriptTap](ScriptTap.md)  
  要移除的Tap脚本音符。

## 返回
[bool](https://learn.microsoft.com/zh-cn/dotnet/api/system.boolean)  
  如果成功移除了指定的Tap音符，则为``true``；否则为``false``。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |