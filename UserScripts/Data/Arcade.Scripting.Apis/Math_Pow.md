Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / Math / 方法 /
# Math.Pow(float, float) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

返回指定数值的幂次方。

```csharp
public static float Pow(float value, float power);
```

## 参数
- ``value`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  要计算的数值。
- ``power`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  幂次方。若为浮点值则按照泰勒级数(Taylor Series)展开的近似算法计算。

## 返回
[float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  指定数值的幂次方。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.3+ |

## 另请参阅
- [Math.Log10(float)](Math_Log10.md) 方法