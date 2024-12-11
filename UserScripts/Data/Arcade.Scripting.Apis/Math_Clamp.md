Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / Math / 方法 /
# Math.Clamp(float, float, float) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

将指定的值限制在一定的范围内。

```csharp
public static float Clamp(float value, float min, float max);
```

## 参数
- ``value`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  要限制的值。
- ``min`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  限制的最小值。
- ``max`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  限制的最大值。

## 返回
[float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  如果值超过了指定的范围，则返回最接近的边界值；否则返回原始值。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.3+ |

## 另请参阅
- [Math.Clamp01(float)](Math_Clamp01.md) 方法