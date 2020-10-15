## 框架入口
Gameframework框架入口脚本 GameEntry.cs，代码如下：
```
/// <summary>  
/// 游戏入口。  
/// </summary>  
public partial class GameEntry : MonoBehaviour  
{  
  private void Start()  
    {  
	    //初始化框架内部的组件
        InitBuiltinComponents();  
        //初始化自定义组件
		InitCustomComponents(); 
  }  
}
```
入口函数只做了两件事
1. 初始化框架内部的组件，框架自带18大组件，用于支持快速开发游戏
2. 初始化自定义组件，各自业务相关逻辑

18大组件中有一个流程组件 ProcedureComponent，该组件用于绑定启动流程。如下图：
![图片](https://github.com/xujinping/Test/blob/master/Lark20201015-093543.png)
