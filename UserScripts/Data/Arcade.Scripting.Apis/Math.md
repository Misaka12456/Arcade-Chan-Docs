Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# Math 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个能从脚本层调用的数学计算类。

```csharp
[MoonSharpUserData]
public static class Math
```

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object?view=latest) -> **Math**

## 注解
该类提供可在脚本层调用的数学计算方法。  
其可以平替Arcade-Chan用户脚本环境下已被禁用的Lua标准库 ``math``。  
其底层由[UnityEngine.Mathf](https://docs.unity3d.com/Documentation/ScriptReference/Mathf.html)提供支持。

## 属性
该类没有向脚本层公开的属性。

## 方法
| 方法名 | 说明 |
| -- | -- |
| [Abs(float)](Math_Abs.md) | 返回指定数值的绝对值。 |
| [Ceil(float)](Math_Ceil.md) | 返回大于或等于指定数值的最小整数。 |
| [CeilToInt(float)](Math_CeilToInt.md) | 返回大于或等于指定数值的最小整数。 |
| [Clamp(float, float, float)](Math_Clamp.md) | 将指定的值限制在一定的范围内。 |
| [Clamp01(float)](Math_Clamp01.md) | 将指定的值限制在``[0, 1]``的范围内。 |
| [Cos(float)](Math_Cos.md) | 返回指定角度的余弦(Cos/Cosine)值。<br />传入的角度为弧度制(Rad)的角度值。 |
| [Cot(float)](Math_Cot.md) | 返回指定角度的余切(Cot/Cotangent)值。<br />传入的角度为弧度制(Rad)的角度值。 |
| [Exp(float)](Math_Exp.md) | 返回自然对数底e的指定次幂的值。 |
| [Floor(float)](Math_Floor.md) | 返回小于或等于指定数值的最大整数。 |
| [FloorToInt(float)](Math_FloorToInt.md) | 返回小于或等于指定数值的最大整数。 |
| [Lerp(float, float, float)](Math_Lerp.md) | 返回以线性插值方式计算的两个数值之间的插值。 |
| [LerpAngle(float, float, float)](Math_LerpAngle.md) | 返回以线性插值方式计算的两个角度之间的插值。 |
| [Log(float)](Math_Log.md) | 返回指定数值的自然对数(ln)值。 |
| [Log10(float)](Math_Log10.md) | 返回指定数值的以10为底的对数(lg)值。 |
| [Max(float, float)](Math_Max.md) | 返回两个数值中较大的一个。 |
| [Min(float, float)](Math_Min.md) | 返回两个数值中较小的一个。 |
| [Pow(float, float)](Math_Pow.md) | 返回指定数值的幂次方。 |
| [Round(float)](Math_Round.md) | 返回指定数值的最近整数值(四舍五入)。 |
| [RoundToInt(float)](Math_RoundToInt.md) | 返回指定数值的最近整数值(四舍五入)。 |
| [Sign(float)](Math_Sign.md) | 返回指定数值的正负符号(即符号函数 ``sgn(x)`` 的值)。 |
| [Sin(float)](Math_Sin.md) | 返回指定角度的正弦(Sin/Sine)值。<br />传入的角度为弧度制(Rad)的角度值。 |
| [Tan(float)](Math_Tan.md) | 返回指定角度的正切(Tan/Tangent)值。<br />传入的角度为弧度制(Rad)的角度值。 |
| [Rand()](Math_Rand.md) | 返回在``[0, 1]``范围内的随机浮点数。 |
| [RandInt(int, int)](Math_RandInt.md) | 返回在给定范围内的随机整数。 |
## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.3+ |