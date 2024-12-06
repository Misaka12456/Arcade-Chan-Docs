Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptTimingGroup / 方法 /
# ScriptTimingGroup.RemoveType 方法
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
| [RemoveType(TimingGroupType)](#Overload_Normal) | 从该时间组中移除一个类型属性。 |
| [RemoveType(string)](#Overload_Append) | 从该时间组中移除一个包含值的类型属性(AppendType)。 |


## ScriptTimingGroup.RemoveType(TimingGroupType)
<a name="Overload_Normal"></a>
从该时间组中移除一个类型属性。

```csharp
public bool RemoveType(TimingGroupType type);
```

### 参数
- ``type`` TimingGroupType  
  要移除的类型属性。

### 返回
[bool](https://docs.microsoft.com/zh-cn/dotnet/api/system.boolean)  
  如果成功移除了指定的类型属性，则返回``true``；否则返回``false``。

### 适用于
<details>
	<summary>Arcade-Chan 3.3.0+</summary>
	<table>
		<tr><th><strong>产品</strong></th><th><strong>版本</strong></th></tr>
		<tr><td><strong>Arcade-Chan</strong></td><td>3.3.0+</td></tr>
	</table>
</details>

## ScriptTimingGroup.RemoveType(string)
<a name="Overload_Append"></a>
从该时间组中移除一个包含值的类型属性(AppendType)。

```csharp
public bool RemoveType(string key);
```

### 参数
- ``key`` [string](https://docs.microsoft.com/zh-cn/dotnet/api/system.string)  
  要移除的类型属性的键。

### 返回
[bool](https://docs.microsoft.com/zh-cn/dotnet/api/system.boolean)  
  如果成功移除了指定的类型属性，则返回``true``；否则返回``false``。

### 适用于
<details>
	<summary>Arcade-Chan 3.3.0+</summary>
	<table>
		<tr><th><strong>产品</strong></th><th><strong>版本</strong></th></tr>
		<tr><td><strong>Arcade-Chan</strong></td><td>3.3.0+</td></tr>
	</table>
</details>