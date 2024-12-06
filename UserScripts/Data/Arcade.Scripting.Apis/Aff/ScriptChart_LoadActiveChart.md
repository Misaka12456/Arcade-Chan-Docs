Arcade-Chan 用户脚本 / 开发手册 / Arcade.Scripting / ScriptChart / 方法 /
# ScriptChart.LoadActiveChart() 方法
参考

## 定义
<div style="font-size: 90%;">
命名空间: <a href="README.md">Arcade.Scripting.Apis.Aff</a><br />
Lua层级: &lt;Global&gt;<br />
程序集: Arcade.Scripting.dll
</div><br />

从当前正在编辑的谱面文件对象创建用于脚本的谱面对象 [ScriptChart](ScriptChart.md)。

```csharp
public static ScriptChart LoadActiveChart();
```

## 返回
[ScriptChart](ScriptChart.md)  
  创建的用于脚本的谱面对象 [ScriptChart](ScriptChart.md)。

## 异常
[InvalidOperationException](https://docs.microsoft.com/zh-cn/dotnet/api/system.invalidoperationexception)
  当没有任何已加载的谱面文件时引发。

## 适用于
| 产品 | 版本 |
|:----|:----|
| **Arcade-Chan** | 3.3.0+ |