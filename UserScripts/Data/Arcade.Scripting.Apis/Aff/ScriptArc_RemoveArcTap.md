Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptArc / 方法 /
# ScriptArc.RemoveArcTap 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

## 重载
| 方法名 | 说明 |
| -- | -- |
| [RemoveArcTap(int)](#Overload_int) | 从该脚本音符Arc上移除一个指定判定时间的ArcTap。 |
| [RemoveArcTap(ScriptArcTap)](#Overload_ScriptArcTap) | 从该脚本音符Arc上移除一个ArcTap。 |


## ScriptArc.RemoveArcTap(int)
<a name="Overload_int"></a>
从该脚本音符Arc上移除一个指定判定时间的ArcTap。

```csharp
public bool RemoveArcTap(int timing);
```

### 参数
- ``timing`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  要移除的ArcTap的判定时间。

### 返回
[bool](https://docs.microsoft.com/zh-cn/dotnet/api/system.boolean)  
  如果找到并成功移除了指定判定时间的ArcTap，则返回``true``；否则返回``false``。

### 适用于
<details>
	<summary>Arcade-Chan 3.3.0+</summary>
	<table>
		<tr><th><strong>产品</strong></th><th><strong>版本</strong></th></tr>
		<tr><td><strong>Arcade-Chan</strong></td><td>3.3.0+</td></tr>
	</table>
</details>

## ScriptArc.RemoveArcTap(ScriptArcTap)
<a name="Overload_ScriptArcTap"></a>
从该脚本音符Arc上移除一个ArcTap。

```csharp
public bool RemoveArcTap(ScriptArcTap arcTap);
```

### 参数
- ``arcTap`` [ScriptArcTap](ScriptArcTap.md)  
  要移除的ArcTap。

### 返回
[bool](https://docs.microsoft.com/zh-cn/dotnet/api/system.boolean)  
  如果找到并成功移除了指定的ArcTap，则返回``true``；否则返回``false``。

### 适用于
<details>
	<summary>Arcade-Chan 3.3.0+</summary>
	<table>
		<tr><th><strong>产品</strong></th><th><strong>版本</strong></th></tr>
		<tr><td><strong>Arcade-Chan</strong></td><td>3.3.0+</td></tr>
	</table>
</details>