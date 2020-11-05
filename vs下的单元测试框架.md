# vs下的单元测试框架

## 1. 新建项目

打开vs2013，新建一个控制台项目，取名为“UnitTestDemo”，打开Program类，创建一个Add方法：

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace UnitTestDemo
{
    public class Program
    {
        static void Main(string[] args)
        {
        }
        public static int Add(int num1, int num2)
        {
            return num1 + num2;
        }
    }
}
```
## 2. 添加单元测试项目

在右侧“解决方案资源管理器”下的“解决方案‘UnitTestDemo’”处右键，选择“添加”-->“新建项目”：

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/1ee9086843a6cdf30a1c78a380ddc69b.png)

在弹出的选项框中选择“测试”中的“单元测试项目”，命名为“UnitTestDemoTest”，点击“确定”添加项目：

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/5d4183cdadc6afc9207acc0c6c528923.png)

为了方便理解，这边可以把UnitTestDemoTest项目下的类重命名为“ProgramTest.cs”，表示这是测试Program类。此时项目结构如下：

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/7ef6114033e47f5db70cad664cc6380c.png)

在单元测试项目中引用控制台项目：右键“引用”，选择“添加引用”：

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/2b58b00452b8d2dee61ae3785c98963d.png)

在弹出的引用管理器界面选择UnitTestDemo项目，点击“确定”添加引用的项目：

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/dd09d46fb219416de53a8fdbd7c2cc4b.png)

引用完毕后项目结构如下：

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/79d1734cd4f7358a4ad58a490b74c54c.png)

## 3. 编写单元测试方法

在单元测试项目中的ProgramTest.cs中填写以下代码：

```
using System;
using Microsoft.VisualStudio.TestTools.UnitTesting;
using UnitTestDemo;

namespace UnitTestDemoTest
{
    [TestClass]
    public class ProgramTest
    {
        [TestMethod]
        public void AddTest()
        {
            int num1 = 100;
            int num2 = 200;

            Assert.AreEqual(Program.Add(num1, num2), 300);
        }
    }
}
```

其中`Assert.AreEqual(Program.Add(num1, num2), 300);`这句表示期望结果为300，如果结果相等，则通过，类似的还有以下几种：
> `Assert.AreEqual()` 测试指定的值是否相等，如果相等，则测试通过；
`Assert.Inconclusive()` 表示一个未验证的测试；
`Assert.IsTrue()` 测试指定的条件是否为True，如果为True，则测试通过；
`Assert.IsFalse()` 测试指定的条件是否为False，如果为False，则测试通过；
`Assert.IsNull()` 测试指定的对象是否为空引用，如果为空，则测试通过；
`Assert.IsNotNull()` 测试指定的对象是否为非空，如果不为空，则测试通过。

## 4. 进行单元测试

依次点击菜单栏的“测试”-->“窗口”-->“测试资源管理器”，可以打开测试资源管理器：

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/17d188b021a5584f6935d12ad8e2ad6e.png)

生成解决方案后，能在左边的“测试资源管理器”中看到全部的测试项目，这边显示为“AddTest”。右击这个测试，选择“运行选定的测试”，即可开始测试：

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/2a35fb7dadc888aa696e4db60756f33d.png)

测试完成后会显示结果，如下图：

![](https://wojiayun.ztywyj.top:18443/lychee/uploads/big/566f95202463374da9fbd7d291b9c280.png)

