Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptArc / 方法 /
# ScriptArc.AddArcTap(int) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

添加一个脚本音符ArcTap到该脚本音符Arc上。

```csharp
public ScriptArcTap AddArcTap(int timing);
```

## 参数
- ``timing`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  ArcTap的判定时间。

## 返回
[ScriptArcTap](ScriptArcTap.md)  
  创建的ArcTap脚本音符。

## 异常
[InvalidOperationException](https://docs.microsoft.com/zh-cn/dotnet/api/system.invalidoperationexception)  
  在当前Arc可判定(不属于启用NoInput的时间组)的情况下，新ArcTap的判定时间与既有至少一个ArcTap的判定时间重叠(TimeOverlap)——这在谱面制作规范中是不被允许的。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |