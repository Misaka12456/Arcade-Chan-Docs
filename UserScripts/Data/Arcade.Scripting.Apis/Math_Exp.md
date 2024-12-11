Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / Math / 方法 /
# Math.Exp(float) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

返回自然对数底e的指定次幂的值。

```csharp
public static float Exp(float power);
```

## 参数
- ``power`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  e的幂次方。若为浮点值则按照泰勒级数(Taylor Series)展开的近似算法计算。

## 返回
[float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  e的``power``次幂的值。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.3+ |

## 另请参阅
- [Math.Log(float)](Math_Log.md) 方法