Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptChart / 方法 /
# ScriptChart.ViewBasicObjects(GettableScriptObjectType) 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

获取指定类型的基本脚本对象的只读视图。  
该方法可返回所有脚本TimingGroup(时间组)对象。

```csharp
public IReadOnlyList<ScriptObject> ViewBasicObjects(GettableScriptObjectType type = GettableScriptObjectType.All);
```

## 参数
- ``type`` GettableScriptObjectType  
  筛选的脚本对象类型。默认为 ``GettableScriptObjectType.All`` ，即所有类型。  
  GettableScriptObjectType枚举值可以是以下之一: ``Timing/Tap/Hold/Arc/Camera/SceneControl/TimingGroup/All``。

## 返回
[IReadOnlyList&lt;ScriptObject&gt;](https://docs.microsoft.com/zh-cn/dotnet/api/system.collections.generic.ireadonlylist-1)  
  指定类型的基本脚本对象的只读视图。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |