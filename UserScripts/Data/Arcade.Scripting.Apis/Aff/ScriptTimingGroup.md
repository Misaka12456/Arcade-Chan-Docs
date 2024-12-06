Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting
# ScriptTimingGroup 类
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

表示一个用于Lua脚本的TimingGroup(时间组)脚本事件。

```csharp
[MoonSharpUserData]
public sealed class ScriptTimingGroup : ScriptObject
```

继承 [Object](https://learn.microsoft.com/zh-cn/dotnet/api/system.object) -> [ScriptObject](ScriptObject.md) -> **ScriptTimingGroup**

## 注解
该类用于在脚本层表示Arcaea谱面中的TimingGroup(时间组)事件。  
除时间组的参数列表及属于该时间组的[ScriptTiming](ScriptTiming.md)外，该类**不包含属于该时间组的其它任何事件信息（包括物件/音符事件）**。  
若获取事件请使用对应事件在[ScriptChart](ScriptChart.md)中的获取方法。

## 属性
| 属性名 | 类型 | 说明 |
| -- | -- | -- |
| ``Id`` | int | 时间组的唯一标识符。通常为时间组在谱面中的索引下标。 |
| ``Types`` | [ObservableCollection&lt;TimingGroupType&gt;](https://docs.microsoft.com/zh-cn/dotnet/api/system.collections.objectmodel.observablecollection-1) | 时间组的类型属性。列表可以为空(时间组无类型属性)。<br />TimingGroupType枚举允许``Normal/NoInput/FadingHolds/AngleX/AngleY/AngleAll``中的任意组合(``Normal``枚举值只能单独出现；``AngleX/AngleY``与``AngleAll``不能同时出现)。 |
| ``AppendTypes`` | System.Enhance.ObservableDictionary<string, string> | 时间组的含值类型属性(AppendTypes)。字典可以为空(时间组无含值类型属性)。<br />对于``anglex/angley``等含值类型属性，其必须在``Types``中注册对应的类型属性，并在此字典中记录其值。 |
| ``Timings`` | [ObservableCollection&lt;ScriptTiming&gt;](https://docs.microsoft.com/zh-cn/dotnet/api/system.collections.objectmodel.observablecollection-1) | 时间组中的所有Timing(时间点)脚本事件。 |

## 方法
| 方法名 | 说明 |
| -- | -- |
| [Create(DynValue)](ScriptTimingGroup_Create.md#Overload_1) | 创建一个新的时间组脚本事件。 |
| [Create(DynValue, DynValue)](ScriptTimingGroup_Create.md#Overload_2) | 创建一个新的时间组脚本事件。 |
| [FromExistingGroupId(int)](ScriptTimingGroup_FromExistingGroupId.md) | 从谱面中已存在的时间组中根据其索引下标获取其的脚本事件对象。 |
| [AddTiming(ScriptTiming)](ScriptTimingGroup_AddTiming.md) | 添加一个Timing(时间点)脚本事件到该时间组中。 |
| [RemoveTiming(ScriptTiming)](ScriptTimingGroup_RemoveTiming.md#Overload_ScriptTiming) | 从该时间组中移除一个Timing(时间点)脚本事件。 |
| [RemoveTiming(int)](ScriptTimingGroup_RemoveTiming.md#Overload_int) | 从该时间组中移除一个指定时间的Timing(时间点)脚本事件。 |
| [RemoveTimings(Predicate&lt;ScriptTiming&gt;)](ScriptTimingGroup_RemoveTimings.md#Overload_Predicate) | 从该时间组中移除所有满足条件的Timing(时间点)脚本事件。 |
| [RemoveTimings(params ScriptTiming&#91;&#93;)](ScriptTimingGroup_RemoveTimings.md#Overload_Array) | 从该时间组中移除指定的Timing(时间点)脚本事件。 |
| [AddType(TimingGroupType)](ScriptTimingGroup_AddType.md#Overload_Normal) | 添加一个类型属性到该时间组中。 |
| [AddType(string, string)](ScriptTimingGroup_AddType.md#Overload_Append) | 添加一个包含值的类型属性(AppendType)到该时间组中。 |
| [RemoveType(TimingGroupType)](ScriptTimingGroup_RemoveType.md#Overload_Normal) | 从该时间组中移除一个类型属性。 |
| [RemoveType(string)](ScriptTimingGroup_RemoveType.md#Overload_Append) | 从该时间组中移除一个包含值的类型属性(AppendType)。 |

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |

## 另请参阅
- [ScriptTiming](ScriptTiming.md)
- [ScriptChart](ScriptChart.md)