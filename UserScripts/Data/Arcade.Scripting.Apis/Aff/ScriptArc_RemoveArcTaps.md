Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptArc / 方法 /
# ScriptArc.RemoveArcTaps(Predicate&lt;ScriptArcTap&gt;) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

从该脚本音符Arc上移除所有满足条件的ArcTap。

```csharp
public int RemoveArcTaps(Predicate<ScriptArcTap> match);
```

### 参数
- ``match`` [Predicate&lt;ScriptArcTap&gt;](https://docs.microsoft.com/zh-cn/dotnet/api/system.predicate-1)  
  要移除的ArcTap的条件。

### 返回
[int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  成功移除的ArcTap的数量。若移除操作灾难性失败(Failed Fatally)，则返回0 (不存在成功移除的ArcTap)。

### 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |