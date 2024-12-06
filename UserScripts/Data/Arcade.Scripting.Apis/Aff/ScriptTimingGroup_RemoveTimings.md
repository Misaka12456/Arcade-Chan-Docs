Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptTimingGroup / 方法 /
# ScriptTimingGroup.RemoveTimings 方法
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
| [RemoveTimings(Predicate&lt;ScriptTiming&gt;)](#Overload_Predicate) | 从该时间组中移除所有满足条件的Timing(时间点)脚本事件。 |
| [RemoveTiming(params ScriptTiming[]))](#Overload_Array) | 从该时间组中移除指定的Timing(时间点)脚本事件。 |


## ScriptTimingGroup.RemoveTimings(Predicate&lt;ScriptTiming&gt;)
<a name="Overload_Predicate"></a>
从该时间组中移除所有满足条件的Timing(时间点)脚本事件。

```csharp
public int RemoveTimings(Predicate<ScriptTiming> match);
```

### 参数
- ``match`` [Predicate&lt;ScriptTiming&gt;](https://docs.microsoft.com/zh-cn/dotnet/api/system.predicate-1)  
  要移除的Timing(时间点)脚本事件的条件。

### 返回
[int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  如果成功移除了至少一个满足条件的Timing(时间点)脚本事件，则返回移除的数量；否则返回0。

### 适用于
<details>
	<summary>Arcade-Chan 3.3.0+</summary>
	<table>
		<tr><th><strong>产品</strong></th><th><strong>版本</strong></th></tr>
		<tr><td><strong>Arcade-Chan</strong></td><td>3.3.0+</td></tr>
	</table>
</details>

## ScriptTimingGroup.RemoveTimings(params ScriptTiming[])
<a name="Overload_Array"></a>
从该时间组中移除指定的Timing(时间点)脚本事件。

```csharp
public int RemoveTimings(params ScriptTiming[] timings);
```

### 参数
- ``timings`` [ScriptTiming](ScriptTiming.md)&#91;&#93;  
  要移除的Timing(时间点)脚本事件。

### 返回
[int](https://docs.microsoft.com/zh-cn/dotnet/api/system.int32)  
  成功移除的Timing(时间点)脚本事件的数量。

### 适用于
<details>
	<summary>Arcade-Chan 3.3.0+</summary>
	<table>
		<tr><th><strong>产品</strong></th><th><strong>版本</strong></th></tr>
		<tr><td><strong>Arcade-Chan</strong></td><td>3.3.0+</td></tr>
	</table>
</details>