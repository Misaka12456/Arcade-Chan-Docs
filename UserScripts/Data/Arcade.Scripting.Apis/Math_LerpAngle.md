Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / Math / 方法 /
# Math.LerpAngle(float, float, float) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

返回以线性插值方式计算的两个角度之间的插值。  
插值值由参数``t``决定，t=0时返回``a``，t=1时返回``b``。  
该方法会考虑角度的周期性，即当角度值超过360度时会自动回到0度。

```csharp
public static float LerpAngle(float a, float b, float t);
```

## 参数
- ``a`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  起始角度，以角度制(Deg)表示。
- ``b`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  结束角度，以角度制(Deg)表示。
- ``t`` [float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  插值参数。取值范围为``0, 1``。超过边界值的数值会自动朝原始方向继续延伸。

## 返回
[float](https://docs.microsoft.com/zh-cn/dotnet/api/system.single)  
  计算得到的插值结果。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.3+ |

## 另请参阅
- [Math.Lerp(float, float, float)](Math_Lerp.md) 方法