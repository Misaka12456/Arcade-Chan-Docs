Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptTimingGroup / 方法 /
# ScriptTimingGroup.Create 方法
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
| [Create(DynValue)](#Overload_1) | 创建一个新的时间组脚本事件。 |
| [Create(DynValue, DynValue))](#Overload_2) | 创建一个新的时间组脚本事件。 |


## ScriptTimingGroup.Create(DynValue)
<a name="Overload_1"></a>
创建一个新的时间组脚本事件。

```csharp
public static ScriptTimingGroup Create(DynValue types);
```

### 参数
- ``types`` DynValue (Lua层为``Table``，列表形态，元素为TimingGroupType枚举值)  
  时间组的类型属性列表。可以为空(不存在任何类型属性)。  
  TimingGroupType枚举允许``Normal/NoInput/FadingHolds/AngleX/AngleY/AngleAll``中的任意组合(``Normal``枚举值只能单独出现；``AngleX/AngleY``与``AngleAll``不能同时出现)。

### 返回
[ScriptTimingGroup](ScriptTimingGroup.md)  
  创建的时间组脚本事件。

### 适用于
<details>
	<summary>Arcade-Chan 3.3.0+</summary>
	<table>
		<tr><th><strong>产品</strong></th><th><strong>版本</strong></th></tr>
		<tr><td><strong>Arcade-Chan</strong></td><td>3.3.0+</td></tr>
	</table>
</details>

## ScriptTimingGroup.Create(DynValue, DynValue)
<a name="Overload_2"></a>
创建一个新的时间组脚本事件。

```csharp
public static ScriptTimingGroup Create(DynValue types, DynValue appendTypes);
```

### 参数
- ``types`` DynValue (Lua层为``Table``，列表形态，元素为TimingGroupType枚举值)  
  时间组的类型属性列表。可以为空(不存在任何类型属性)。  
  TimingGroupType枚举允许``Normal/NoInput/FadingHolds/AngleX/AngleY/AngleAll``中的任意组合(``Normal``枚举值只能单独出现；``AngleX/AngleY``与``AngleAll``不能同时出现)。
- ``appendTypes`` DynValue (Lua层为``Table``，字典形态，键值均为[string](https://docs.microsoft.com/zh-cn/dotnet/api/system.string))  
  时间组的含值类型属性列表。可以为空(不存在任何含值类型属性)。  
  对于``anglex/angley``等含值类型属性，其必须在``types``中注册对应的类型属性，并在此字典中记录其值。

### 返回
[ScriptTimingGroup](ScriptTimingGroup.md)  
  创建的时间组脚本事件。

### 适用于
<details>
	<summary>Arcade-Chan 3.3.0+</summary>
	<table>
		<tr><th><strong>产品</strong></th><th><strong>版本</strong></th></tr>
		<tr><td><strong>Arcade-Chan</strong></td><td>3.3.0+</td></tr>
	</table>
</details>