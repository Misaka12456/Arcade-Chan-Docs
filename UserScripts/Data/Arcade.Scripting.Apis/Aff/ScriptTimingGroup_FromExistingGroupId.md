Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptTimingGroup / 方法 /
# ScriptTimingGroup.FromExistingGroupId(int) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

从谱面中已存在的时间组中根据其索引下标获取其的脚本事件对象。

```csharp
public static ScriptTimingGroup FromExistingGroupId(int id);
```

## 参数
- ``id`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  时间组的索引下标。0表示默认时间组。

## 返回
[ScriptTimingGroup](ScriptTimingGroup.md)  
  获取到的时间组的脚本事件对象。

## 异常
[ArgumentOutOfRangeException](https://docs.microsoft.com/zh-cn/dotnet/api/system.argumentoutofrangeexception)
  当给定的时间组索引下标超出范围时引发。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |