Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / Math / 方法 /
# Math.Clamp01(float) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

将指定的值限制在``[0, 1]``的范围内。

```csharp
public static float Clamp01(float value);
```

## 参数
- ``value`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  要限制的值。

## 返回
[float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  如果值超过了``[0, 1]``所表示的范围，则返回最接近的边界值；否则返回原始值。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.3+ |

## 另请参阅
- [Math.Clamp(float, float, float)](Math_Clamp.md) 方法