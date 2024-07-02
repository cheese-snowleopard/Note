# Navigation

在Unity中，Navigation指的是用户界面（UI）元素之间的导航系统，通常用于处理游戏控制器或键盘输入时在不同UI元素之间的移动。具体来说，Navigation类允许你定义当用户按下方向键或操纵杆时，焦点应该如何从一个UI元素移动到另一个UI元素。这个功能在使用游戏手柄或键盘进行UI操作时特别有用。

```csharp
using UnityEngine;
using UnityEngine.UI;

public class NavigationExample : MonoBehaviour
{
    public Button button1;
    public Button button2;
    public Button button3;
    public Button button4;

    void Start()
    {
        // 获取 button1 的 Navigation 设置
        Navigation nav = button1.navigation;
        nav.mode = Navigation.Mode.Explicit;

        // 设置显式导航目标
        nav.selectOnUp = button4;
        nav.selectOnDown = button2;
        nav.selectOnLeft = button3;
        nav.selectOnRight = button2;

        // 应用设置
        button1.navigation = nav;
    }
}

```