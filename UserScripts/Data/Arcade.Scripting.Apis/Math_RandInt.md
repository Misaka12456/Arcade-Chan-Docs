Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / Math / 方法 /
# Math.RandInt(int, int) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

返回在给定范围内的随机整数。

```csharp
public static int RandInt(int minInclusive, int maxExclusive);
```

## 参数
- ``minInclusive`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  随机数的最小值(包含)。
- ``maxExclusive`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  随机数的最大值(不包含)。

## 返回
[int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  返回在 ``[minInclusive, maxExclusive)`` 范围内的随机整数。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.3+ |

## 另请参阅
- [Math.Rand()](Math_Rand.md) 方法