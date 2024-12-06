Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptTimingGroup / 方法 /
# ScriptTimingGroup.RemoveTiming 方法
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
| [RemoveTiming(ScriptTiming)](#Overload_ScriptTiming) | 从该时间组中移除一个Timing(时间点)脚本事件。 |
| [RemoveTiming(int))](#Overload_int) | 从该时间组中移除一个指定时间的Timing(时间点)脚本事件。 |


## ScriptTimingGroup.RemoveTiming(ScriptTiming)
<a name="Overload_ScriptTiming"></a>
从该时间组中移除一个Timing(时间点)脚本事件。

```csharp
public bool RemoveTiming(ScriptTiming timing);
```

### 参数
- ``timing`` [ScriptTiming](ScriptTiming.md)  
  要移除的Timing(时间点)脚本事件。

### 返回
[bool](https://docs.microsoft.com/zh-cn/dotnet/api/system.boolean)  
  如果找到并成功移除了指定判定时间的Timing(时间点)脚本事件，则返回``true``；否则返回``false``。

### 适用于
<details>
	<summary>Arcade-Chan 3.3.0+</summary>
	<table>
		<tr><th><strong>产品</strong></th><th><strong>版本</strong></th></tr>
		<tr><td><strong>Arcade-Chan</strong></td><td>3.3.0+</td></tr>
	</table>
</details>

## ScriptTimingGroup.RemoveTiming(int)
<a name="Overload_int"></a>
从该时间组中移除一个指定时间的Timing(时间点)脚本事件。

```csharp
public bool RemoveTiming(int time);
```

### 参数
- ``time`` [int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  要移除的Timing(时间点)脚本事件的时间。

### 返回
[bool](https://docs.microsoft.com/zh-cn/dotnet/api/system.boolean)  
  如果找到并成功移除了指定判定时间的Timing(时间点)脚本事件，则返回``true``；否则返回``false``。

### 适用于
<details>
	<summary>Arcade-Chan 3.3.0+</summary>
	<table>
		<tr><th><strong>产品</strong></th><th><strong>版本</strong></th></tr>
		<tr><td><strong>Arcade-Chan</strong></td><td>3.3.0+</td></tr>
	</table>
</details>