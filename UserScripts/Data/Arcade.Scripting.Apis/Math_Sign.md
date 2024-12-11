Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / Math / 方法 /
# Math.Sign(float) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

返回指定数值的正负符号(即符号函数 ``sgn(x)`` 的值)。

```csharp
public static float Sign(float value);
```

## 参数
- ``value`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  要计算的数值。

## 返回
[float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  - 如果 ``value`` &gt; 0，则返回 1。
  - 如果 ``value`` = 0，则返回 0。
  - 如果 ``value`` &lt; 0，则返回 -1。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.3+ |