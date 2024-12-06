Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptArcTap / 方法 /
# ScriptArcTap.Create(ScriptArc, int) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

使用指定的父脚本音符Arc和判定时间创建一个新的ArcTap脚本音符。  
**ArcTap所属的时间组将与其父Arc所属的时间组一致。**  

```csharp
public static ScriptArcTap Create(ScriptArc arc, int timing);
```

## 参数
- ``arc`` [ScriptArc](ScriptArc.md)  
  ArcTap所属的父脚本音符Arc。
- ``timing`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  ArcTap的判定时间。

## 返回
[ScriptArcTap](ScriptArcTap.md)  
  创建的ArcTap脚本音符。

## 注解
该方法创建的 [ScriptArcTap](ScriptArcTap.md) 对象无法添加到父Arc中。  
如需添加到父Arc中请直接使用 [ScriptArc.AddArcTap(int)](ScriptArc_AddArcTap.md) 方法。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |