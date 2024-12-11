Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptChart / 方法 /
# ScriptChart.ViewEvents 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

获取所有脚本事件(不包括[ScriptTimingGroup](ScriptTimingGroup.md))的只读视图。  
若需要修改现有脚本事件，请通过该方法获取单个脚本事件后修改其属性即可。

```csharp
public IReadOnlyList<ScriptEvent> ViewEvents();
```

## 返回
[IReadOnlyList&lt;ScriptEvent&gt;](https://learn.microsoft.com/zh-cn/dotnet/api/system.collections.generic.ireadonlylist-1)  
  所有脚本事件的只读视图。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |