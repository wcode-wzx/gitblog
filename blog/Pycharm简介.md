<!--
author: thyme
date: 2019-12-17
title: Pycharm简介
tags:  
category: python
status: publish   
summary: 
-->

Pycharm简介
PyCharm是用于Python脚本语言的最流行的IDE。 本章将向您介绍PyCharm并解释其功能。PyCharm为用户和开发人员在以下方面提供了一些最好的功能 -

- 代码完成和检查
- 高级调试
- 支持Web编程和框架，如[Django](http://www.yiibai.com/django/)和[Flask](http://www.yiibai.com/flask/)

## **PyCharm的特点**

此外，由于下面提到的功能，开发人员会发现PyCharm很适合使用 -

**代码完成**

无论是内置还是外置软件包，PyCharm均可实现更流畅的代码完成。

**SQLAlchemy作为调试器**

可以设置断点，在调试器中暂停，并可以查看用于SQL语言代码的用户表达式的SQL表示。

**编辑器中的Git可视化**

在Python中编码时，对于开发人员来说查询是正常的。 您可以在PyCharm中轻松检查上次提交，因为它具有可以定义上次提交与当前提交之间的区别的蓝色部分。

**代码覆盖编辑器**

您可以在PyCharm编辑器外部运行.py文件，并将其标记为项目树中其他位置的代码覆盖细节，摘要部分等。

**包管理**

所有安装的软件包都以适当的视觉表示显示。 这包括已安装软件包的列表以及搜索和添加新软件包的功能。

**本地历史**

本地历史始终以像Git这样的补充方式跟踪更改。 PyCharm中的本地历史记录提供了回滚和添加内容所需的完整细节。

**重构**

重构是一次重命名一个或多个文件的过程，PyCharm包含用于平滑重构过程的各种快捷方式。

**PyCharm编辑器的用户界面**

PyCharm编辑器的用户界面显示在下面的屏幕截图中。 请注意，编辑器包含用于创建新项目或从现有项目导入的各种功能。



![img](http://www.thyme.org.cn\blog\img\874090615_35681.jpg)



从上面的屏幕截图中，可以看到新创建的项目Demo和用于包管理的site-packages文件夹以及其他各种文件夹。

可以下载PyCharm编辑器并在此链接阅读其官方文档 -

https://www.jetbrains.com/pycharm/

Measure

Measure

# Pycharm基础知识

本章将讨论PyCharm的基本知识，并让您感觉很舒服，开始在PyCharm编辑器中工作。

当第一次启动PyCharm时，您可以看到一个带有IDE入口点的欢迎屏幕，例如 -

- 创建或打开项目
- 从版本控制中检出项目
- 查看文档
- 配置IDE



![img](http://www.thyme.org.cn\blog\img\665090627_11571.jpg)



回想一下，在上一章中，我们创建了一个名为`demo1`的项目，将在本教程中引用同一个项目。 现在将开始在同一个项目中创建新文件，以了解PyCharm Editor的基本知识。



![img](http://www.thyme.org.cn\blog\img\118090628_52785.jpg)



以上快照描述了**demo1** 的项目概述和创建新文件的选项。例如创建一个名为`main.py`的新文件。

包含在`main.py`中的代码如下所示 -

```
y = 3
def print_stuff():
print ("Calling print_stuff")
print (y)
z = 4
print (z)
print("exiting print_stuff")
print_stuff() # we call print_stuff and the program execution goes to (***)
print(y) # works fine
print (z) # NameError!!!
```

Python

使用PyCharm编辑器在`main.py`文件中创建的代码显示如下 -



![img](http://www.thyme.org.cn\blog\img\312090630_43622.jpg)



此代码可以在IDE环境中运行。下面讨论运行程序的基本演示 -



![img](http://www.thyme.org.cn\blog\img\263090630_87438.jpg)



请注意，我们在指定的代码中包含了一些错误，以便控制台可以按照预期的方式执行代码并显示输出。



![img](http://www.thyme.org.cn\blog\img\871090633_56020.jpg)



Measure

Measure

# Pycharm安装

在本章中，您将详细了解PyCharm在本地计算机上的安装过程。

## **安装步骤**

必须按照以下步骤在系统上安装PyCharm。 这些步骤显示了从将PyCharm软件包从其官方网站下载到创建新项目的安装过程。

**第1步**

从PyCharm的官方网站下载所需的软件包或可执行文件 https://www.jetbrains.com/pycharm/download/#section=windows 在这里您会看到两个Windows版本的软件包，如下面的屏幕截图所示 -



![img](http://www.thyme.org.cn\blog\img\870090617_98109.jpg)



**请注意**，该专业套件包含所有高级功能，并在几天内免费试用，用户必须在试用期之后购买授权密钥才能激活。 社区版是免费的，可以根据需要进行下载和安装。 它包含安装所需的所有基本功能。 请注意，我们将在本教程中使用社区版本。

**第2步**

将社区软件包(可执行文件)下载到您的系统中，双击:*pycharm-community-2018.1.4.exe*，如下所示 -



![img](http://www.thyme.org.cn\blog\img\264090621_73141.png)



**第3步**

现在，安装程序类似于任何其他软件包。点击下一步:



![img](http://www.thyme.org.cn\blog\img\887090623_25429.png)





![img](http://www.thyme.org.cn\blog\img\483090624_18779.png)



**第4步**

安装成功以后，PyCharm会要求您导入现有软件包的设置(如果有的话)。



![img](http://www.thyme.org.cn\blog\img\372090625_30600.png)





![img](http://www.thyme.org.cn\blog\img\564090625_38367.png)



这有助于创建一个新的Python项目，可以从头开始工作。 请注意，与其他IDE不同，PyCharm只专注于使用Python脚本语言的项目。

Measure

Measure

# Pycharm键盘映射

PyCharm包含各种键盘映射，以显示编辑器中最常用的命令。 本章详细讨论Pycharm键盘映射。

可以在文件菜单:**帮助** -> **键盘映射参考** 中找到可用键盘列表，如下面的屏幕截图所示 -



![img](http://www.thyme.org.cn\blog\img\305090639_33134.jpg)



可以找到Pycharm键盘映射列表和可用的PDF格式快捷方式，如下所示 -



![img](http://www.thyme.org.cn\blog\img\550090641_83907.png)



> *注 - Windows和Linux操作系统的默认键盘映射是默认键盘映射，而在Mac OS中，默认键盘映射是OSX 10.5。*

还可以使用Windows和Linux操作系统中的设置选项(Mac OS中的首选项)查看可用Keymaps列表，如下面的屏幕截图所示 -



![img](http://www.thyme.org.cn\blog\img\120090642_90332.jpg)



默认的键盘映射包括编辑器操作，主菜单，工具窗口，外部工具，版本控制系统，宏，快速列表，插件和其他选项的各个部分。

Measure

Measure

# Pycharm快捷键

快捷键是用于执行一组活动的键的组合。可以在Keymaps指南参考中找到PyCharm快捷键列表。

## **查看快捷键**

快捷键列表可在以下选项:**帮助** -> **查找操作** 菜单中使用快捷窗口弹出。



![img](http://www.thyme.org.cn\blog\img\596090651_34840.jpg)



可以看到这里显示的快捷窗口 -

![img](http://www.thyme.org.cn\blog\img\258090651_35130.jpg)



该快捷方式包括标识符列表，包含功能和选项菜单栏的快捷方式。例如，查看导航栏包含切换ON和OFF，根据设置的值(ON和OFF)显示导航栏。

Measure

Measure

# Pycharm Omni

Omni是PyCharm的一部分，可以从任何地方进入任何地方。 它包括用于从一个地方移动到另一个地方的各种工具。 它有助于在这种情况下您需要快速从一个项目目录移动到另一个目录。 本章将使您熟悉Omni的功能。

**功能**

导航菜单描述了Omni中涉及的功能。 本节详细讨论这些 -

**类**

这有助于在一个提到的项目中从一个类导航到另一个类。 这对浏览类的列表非常有帮助。

![img](http://www.thyme.org.cn\blog\img\562090656_99435.jpg)



**后退**

该选项有助于从现有状态向后移动。 快捷键是:**Ctrl + Alt + Left**。



![img](http://www.thyme.org.cn\blog\img\255090658_74057.jpg)



**前进**

它的作用类似于**后退**选项。 但是，功能完全相反。



![img](http://www.thyme.org.cn\blog\img\932090658_17698.jpg)



# Pycharm宏

PyCharm编辑器中的宏和Omni之间的区别很微妙。 Omni允许您访问编辑器的确切位置或指定的代码位置，但没有特别的意义。 宏另一方面允许用户浏览函数和类或特定的类方法。

## **导航宏**

观察以下屏幕截图，以更好地了解导航宏 -



![img](http://www.thyme.org.cn\blog\img\956140611_51921.jpg)



**Navigate** -> **Declaration** 打开显示声明，类型声明和定义超级方法。 类型声明中包含的各种属性如下所示 -



![img](http://www.thyme.org.cn\blog\img\843140613_44693.jpg)



但是，如果用户尝试访问.so对象的声明(例如，从datetime模块导航到选择模块)，则每次遇到存根文件时都会出现此宏的问题。

**到处搜索**

它有助于搜索类和相关的方法。它还包括与Google一起搜索的选项。



![img](http://www.thyme.org.cn\blog\img\522140615_56855.jpg)



每个部分在其部分名称旁边都包含一个快捷键组合。 “随处搜索”是PyCharm中可用的其他搜索操作的入口。

Measure

Measure

# Pycharm微指令

Micros处理获取指定文件中的位置。这些工具最终使用了大部分的开发过程。 在本章中，您将详细学习微指令(Micro)。

考虑结构面板的例子，它被用作微观的表示。

## **从源滚动**

它有助于从提到的源滚动，如指定文件的完整文件夹位置。



![img](http://www.thyme.org.cn\blog\img\316140617_67566.jpg)



**全部收缩**

考虑下面显示的屏幕截图，其中显示了打开指定位置的文件。为了折叠文件夹结构，您可以使用图像中显示的快捷键。



![img](http://www.thyme.org.cn\blog\img\374140618_37286.jpg)



此快捷键有助于折叠指定代码的文件夹位置，如下所示。

![img](http://www.thyme.org.cn\blog\img\103140618_73734.jpg)



**显示选项菜单**

项目结构面板的“显示选项”菜单显示可用于创建项目的选项列表。 观察下面的截图以便更好地理解 -



![img](http://www.thyme.org.cn\blog\img\164140618_67405.jpg)



选项列表显示如下 -



![img](http://www.thyme.org.cn\blog\img\887140619_29803.jpg)



**隐藏**

该选项有助于隐藏项目窗口的结构面板。 折叠后的结构面板的用户界面如下所示 -



![img](http://www.thyme.org.cn\blog\img\475140619_42538.jpg)





![img](http://www.thyme.org.cn\blog\img\646140620_65082.jpg)



可以按照此处所示重新打开结构面板 -



![img](http://www.thyme.org.cn\blog\img\597140620_92278.jpg)



Measure

Measure

# Pycharm改进和编写代码

PyCharm包含用于编写代码的各种标准，其中包含适用于Python的适当缩进。 这有助于提高代码标准并在PyCharm编辑器中编写完整的代码。

## **改进代码完成**

PyCharm中的代码完成非常独特。 您可以使用许多其他功能进一步增强它。 请注意，编辑器提供了代码块的开始和结束。 以下代码编写一个名为demo.py的文件中 -

message = 'GIEWIVrGMTLIVrHIQS' #encrypted message

LETTERS = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'

for key in range(len(LETTERS)):

translated = ''

for symbol in message:

if symbol in LETTERS:

num = LETTERS.find(symbol)

num = num - key

if num < 0:

num = num + len(LETTERS)

translated = translated + LETTERS[num]

else:

translated = translated + symbol

print('Hacking key #%s: %s' % (key, translated))

Python

代码使用以下构造完成 -



![img](http://www.thyme.org.cn\blog\img\724140633_72739.jpg)



如果在屏幕上显示此弹出窗口时按下Ctrl + 空格键，则可以看到更多代码完成选项 -

![img](http://www.thyme.org.cn\blog\img\715140633_85076.jpg)



## **意图操作**

PyCharm包含意图特定的操作，并且快捷键是**Alt + Enter**。 工作中意图最重要的例子是在字符串中使用语言注入。下面给出的屏幕截图显示了意图操作的工作 -



![img](http://www.thyme.org.cn\blog\img\755140634_20999.jpg)



请注意，可以在PyCharm编辑器中插入许多意图操作的其它语言。

Measure

Measure

# Pycharm控制台

PyCharm有一个完整的代码完整的Python控制台，可以在选项菜单:工具(*Tools*) - >运行Python控制台(*Run Python Console*)中找到。



![img](http://www.thyme.org.cn\blog\img\933140637_49933.jpg)



使用上一章中的代码，如下所示 -

message = 'GIEWIVrGMTLIVrHIQS' #encrypted message

LETTERS = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ'

for key in range(len(LETTERS)):

translated = ''

for symbol in message:

if symbol in LETTERS:

num = LETTERS.find(symbol)

num = num - key

if num < 0:

num = num + len(LETTERS)

translated = translated + LETTERS[num]

else:

translated = translated + symbol

print('Hacking key #%s: %s' % (key, translated))

Python

现在，在控制台下运行代码来执行脚本以获取所需的输出，如下所示。



![img](http://www.thyme.org.cn\blog\img\130140638_26953.jpg)



您可以在控制台中，观察到输出如下所示 -

![img](http://www.thyme.org.cn\blog\img\385140638_36828.jpg)



Measure

Measure

# Pycharm解释器

PyCharm包括解释器，以便根据需要创建具有新功能的新项目。 您可以根据需要在系统中创建虚拟环境。也可以在对话框中继承全局网站包。解释器可在Python Package Index(PyPI)上找到，并且可以使用pip install轻松安装和访问。

## **解释器的创建**

要创建一个解释器，总是建议在管理所需配置的情况下创建一个新项目。 看看下面的截图以便更好地理解 -



![img](http://www.thyme.org.cn\blog\img\962140651_45327.jpg)



这些参数包括 -

- 位置 - 它描述了创建虚拟环境的参数，它是系统的具体位置。
- 基本解释器 - 它定义解释器的属性。

该对话框还引用了现有虚拟解释器将被视为属性的参数。 当用户添加了新的本地解释器，PyCharm将会向用户询问解释器的二进制文件。 在大多数情况下，它总是被视为一个.exe文件。 在Jython的情况下，它是一个.bat文件。



![img](http://www.thyme.org.cn\blog\img\377140652_23172.jpg)



项目解释器的详细信息和现有项目demo1的基本配置参考如下所示 -

![img](http://www.thyme.org.cn\blog\img\569140653_61618.jpg)



请记住，解释器还包括项目工作顺利进行所必需的基本软件包。

Measure

Measure

# Pycharm调试和断点

运行Python代码包含两种模式:运行脚本和调试脚本。 本章重点介绍如何使用PyCharm来调试Python脚本。

## **涉及的步骤**

调试Python项目的步骤如下所述 -

**第1步**

从下面的屏幕截图所示开始调试Python项目 -



![img](http://www.thyme.org.cn\blog\img\651080653_73792.jpg)



**第2步**

现在，Windows防火墙要求调试Python项目的权限，因为该过程涉及逐行编译。



![img](http://www.thyme.org.cn\blog\img\378080654_95155.jpg)



**第3步**

调试控制台在PyCharm编辑器中创建，如下所示，它逐行执行输出。



![img](http://www.thyme.org.cn\blog\img\806080654_18207.jpg)



运行按钮从一行移动到另一行，以按照我们想要的方式执行输出。



![img](http://www.thyme.org.cn\blog\img\378080655_86471.jpg)



## **了解断点**

在调试特定的脚本时，有意创建一个断点。 断点是故意停止的地方或代码暂停的地方，以便在特定阶段识别输出。



![img](http://www.thyme.org.cn\blog\img\728080655_54697.jpg)



在PyCharm中，使用指定编辑器中的单独对话框可以看到断点。 它包括各种属性来评估定义的断点和跟踪日志的主要动机，以实现更好的编程实践。

Measure

Measure

# Pycharm版本控制的集成

PyCharm支持各种版本控制系统。 此功能有助于改进管理各种版本的代码库。 本章详细讨论了这个概念。

## **涉及的步骤**

您将通过以下步骤来初始化和管理版本控制系统 -

**初始化Subversion控制系统**

要以系统的方式启动版本控制系统，初始化它非常重要。 PyCharm提供了各种版本控制系统的选项。



![img](http://www.thyme.org.cn\blog\img\136090600_61181.jpg)





![img](http://www.thyme.org.cn\blog\img\618090600_21498.jpg)



**忽略文件**

在PyCharm的任何一个项目中，我们都要建立默认项目和虚拟环境，也应该使用版本控制系统来创建它的管理。 例如，Git包含在提交操作期间被忽略的.gitignore文件，但是，其中包含一些配置。 现在，转到设置菜单并检查以下内容 -



![img](http://www.thyme.org.cn\blog\img\104090601_41980.jpg)



它包括用于检查Git可执行文件路径的各种配置，并验证是否忽略任何文件。



![img](http://www.thyme.org.cn\blog\img\567090601_11478.jpg)



**GitHub的配置**

PyCharm包括设置以包括GitHub存储库的配置，其中用户可以包括用户名，密码和其他凭证(如果有的话)。



![img](http://www.thyme.org.cn\blog\img\231090604_32603.jpg)



# Pycharm HTML和CSS集成

PyCharm编辑器很好地支持HTML和CSS。 PyCharm编辑器包含一个特殊的简写，并为HTML提供标记完成。

## **Emmet**

Emmet是PyCharm编辑器中使用的速写。 它包括HTML和CSS文件的缩写预览，自动URL识别和编辑点等各种功能。设置部分的用户界面显示在下面的屏幕截图中 -



![img](http://www.thyme.org.cn\blog\img\838090608_26099.jpg)



## **创建HTML和CSS文件**

PyCharm包含一个用于创建HTML和CSS文件的内置功能。 创建新的HTML和CSS文件的基本步骤如下所示 -



![img](http://www.thyme.org.cn\blog\img\978090615_60532.jpg)



现在，在项目中创建HTML文件时提及文件的名称，如下所示 -

![img](http://www.thyme.org.cn\blog\img\287090627_31229.jpg)

这将创建sample-file.html文件，如下所示 -

![img](http://www.thyme.org.cn\blog\img\621090627_22753.jpg)



## **创建CSS文件**

这里演示如何创建CSS文件的步骤:

从菜单**New**中，选择**File**选项，如下所示 -



![img](http://www.thyme.org.cn\blog\img\178090628_56487.jpg)



在创建过程中指定CSS的名称，如此处所示 -



![img](http://www.thyme.org.cn\blog\img\893090632_58209.jpg)



可以看到具有不同颜色组合的各种文件的完整项目结构，如下所示 -



![img](http://www.thyme.org.cn\blog\img\961090632_84075.jpg)



Measure

Measure

# Pycharm Javascript支持

在本章中，我们将重点介绍在PyCharm编辑器中使用JavaScript的主要功能。 当用户通过URL实现JavaScript库时，PyCharm打算下载本地副本，以便用于完成和代码分析。

参考以下HTML文件的示例代码，如下所示，这是在前一章中创建的HTML代码 -



![img](http://www.thyme.org.cn\blog\img\731090634_50965.jpg)



对于每个HTML文件或JavaScript文件，可以检查通过PyCharm编辑器的设置配置加载的外部库。 观察下面的截图以便更好地理解 -



![img](http://www.thyme.org.cn\blog\img\402090635_93874.jpg)



请注意，除非下载并实现它，否则无法看到任何库。 PyCharm还通过一个名为**JS Toolbox**的工具箱支持各种库的JavaScript支持。 下面的截图显示了这一点。



![img](http://www.thyme.org.cn\blog\img\251090636_45927.jpg)



它还包含JavaScript文件配置所需的各种属性。 属性和配置列表如下所示 -

![img](http://www.thyme.org.cn\blog\img\311090639_84130.jpg)



注意它包括各种参数，如单元测试后缀，文件后缀，查看后缀，搜索URL和特定的根目录。

Measure

Measure

# Pycharm提示

PyCharm在启动过程中提供了各种提示，帮助用户了解其功能和操作。 它还包含一些强制理解的捷径。

在本章中，您将看到一些重要的PyCharm技巧。

## **将文件更改为特定的更改列表**

本技巧演示了如何根据用户的选择将文件更改为特定更改列表。 这有助于根据版本控制系统设置管理存储库。 观察下面的截图以便更好地理解 -



![img](http://www.thyme.org.cn\blog\img\596090641_81270.jpg)



## **显示一个类中所有用法的列表**

此功能显示项目中特定类别，方法或变量中包含的所有用法的列表。 它可以让用户快速跳到特定区域。 观察下面的截图以便更好地理解 -



![img](http://www.thyme.org.cn\blog\img\642090641_81868.jpg)



## **查找操作的菜单命令**

这个提示有助于查找特定动作的菜单命令，而且快捷键也是**Ctrl + Shift + A**。 用户可以从提到的建议列表中选择所需的操作。



![img](http://www.thyme.org.cn\blog\img\259090642_80762.jpg)



## **通过代码运行检查**

此提示有助于通过代码运行特定的检查。 同样的快捷键组合是**Ctrl + Alt + Shift + I**。



![img](http://www.thyme.org.cn\blog\img\687090642_86052.jpg)



## **指定设置列表**

此提示用于指定所需设置的列表。 它包括特定编辑器的智能键。 智能键是一些操作的快捷键。



![img](http://www.thyme.org.cn\blog\img\499090646_19107.jpg)



## **运行/调试脚本文件**

此提示对于运行或调试可通过主工具栏访问的脚本文件非常有用。 同样的快捷键组合是**Alt + Shift + F10**。



![img](http://www.thyme.org.cn\blog\img\287090647_23245.jpg)



Measure

Measure

# Pycharm数据库工具

PyCharm支持各种类型数据库的接口支持。 当用户授予对创建的数据库的访问权限，它就会使用提供代码完成的SQL编写工具提供数据库的模式图。 在本章中，我们将重点介绍MySQL数据库连接，其中涉及以下步骤。

## **添加数据源**

请注意PyCharm支持各种数据库连接，这一点很重要。

**第1步**

打开数据库工具窗口:**View** -> **Tool Windows** -> **Database**，并打开名为数据源和对话框的对话框(**Data Sources and Dialog**)。

![img](http://www.thyme.org.cn\blog\img\507120609_88658.jpg)



现在，选择MySQL数据库来添加新的数据源。

**第2步**

用户应该下载缺少的驱动程序文件以获得与MySQL数据库的正确连接。

![img](http://www.thyme.org.cn\blog\img\964120609_31358.jpg)

**第3步**

现在，指定要实现连接的配置设置。

- **主机(Host )** - 如果您的数据库服务器位于不同的计算机上，请使用服务器主机的IP地址替换localhost，例如172.20.210.168。

  **端口(Port)** - 默认的MySQL服务器端口是3306。如果您的服务器使用不同的端口，请指定该端口。

- **用户和密码** - 这些是必需的凭据。

**第4步**

通过测试连接(*Test Connection*)功能始终确保数据库连接成功。

![img](http://www.thyme.org.cn\blog\img\240120611_64092.jpg)



测试连接还涉及通过查询创建测试表并执行它们。 一旦执行成功，可以操作数据库。



![img](http://www.thyme.org.cn\blog\img\164120618_77671.jpg)

Measure

Measure

# Pycharm导出数据

PyCharm IDE包含将现有代码文件转换为HTML格式或CSV格式的各种功能。 在本章中，您将学习使用PyCharm IDE导出数据。

PyCharm编辑器的输出设置如下图所示 -



![img](http://www.thyme.org.cn\blog\img\316140604_30256.jpg)



## **导出为HTML功能**

此功能有助于导出HTML格式的特定文件。 这样做是为了改善给定模块的安全性。 下面的截图提供了一个更好的理解 -



![img](http://www.thyme.org.cn\blog\img\758140604_82134.jpg)



导出操作成功后，生成的HTML文件将显示在浏览器输出中，如下所示 -



![img](http://www.thyme.org.cn\blog\img\393140605_64193.jpg)



现在，如果查看导出操作后生成的HTML代码，可以观察到也包含行号以实现此操作。



![img](http://www.thyme.org.cn\blog\img\274140606_32505.jpg)

Measure

Measure

# Pycharm Web框架

本章重点介绍Web框架及其部署。 PyCharm具有部署代码和文件的简单功能。 要使用PyCharm部署代码，我们需要添加一个带有菜单选项:**Settings** -> **Build, Execution** -> **Deployment** 来部署Web服务器。



![img](http://www.thyme.org.cn\blog\img\894140610_21326.jpg)



现在，包含部署项目所需的各种配置的所有设置。



![img](http://www.thyme.org.cn\blog\img\634140610_44764.jpg)



在**Mappings** 选项卡中，用户可以指定本地代码的位置以及它应该远程复制到的位置。



![img](http://www.thyme.org.cn\blog\img\927140611_42957.jpg)



代码可以使用工具菜单栏下的:**Tools** -> **Deployment** 选项进行部署。

PyCharm中的部署非常细化:用户可以部署单个文件或整个源代码。



![img](http://www.thyme.org.cn\blog\img\197140611_97654.jpg)



PyCharm还包含各种操作来比较远程和本地版本。 编辑器使用自动部署和版本控制系统比较本地和远程版本更可靠。

Measure

Measure

# Pycharm Django框架

PyCharm的一个特点是它包含了对Django的支持。 通过在PyCharm中包含JavaScript特性，它可以被认为是Django的最佳IDE。

下面给出了在PyCharm IDE中创建Django项目的基本步骤 -



![img](http://www.thyme.org.cn\blog\img\286140616_74802.jpg)



如果启用**EnableDjangoadmin** 选项，PyCharm将为您设置管理网站。



![img](http://www.thyme.org.cn\blog\img\782140617_47343.jpg)



**模板调试**

调试适用于Django和Jinja模板。 我们可以检查变量，逐步执行代码，并在调试器中执行所期望的操作。



![img](http://www.thyme.org.cn\blog\img\578140618_60390.jpg)

Measure

Measure

# Pycharm Pyramid框架

可以使用其欢迎窗口在PyCharm编辑器中创建一个Pyramid Framework项目。

用户可以默认设置项目的解释器和Python位置，选择脚手架和模板语言。 Pyramid框架中的脚手架使用URL调度来映射URL并查看代码和SQLAlchemy以获得持久性属性。



![img](http://www.thyme.org.cn\blog\img\307140620_60550.jpg)



PyCharm编辑器会向用户询问setup.py文件中所需软件包的列表，并提示用户下载所需的软件包。

![img](http://www.thyme.org.cn/gitblog/blog/Pycharm%E7%AE%80%E4%BB%8B%20-%20Pycharm%E6%95%99%E7%A8%8B%E2%84%A2_files/519140620_64747.jpg)

以开发模式安装项目(有关更多详细信息，请参阅 **Pyramid** 的官方文档)。 用户应该通过菜单:**Tools** -> **Run setup.py** 选项来运行。



![img](http://www.thyme.org.cn/gitblog/blog/Pycharm%E7%AE%80%E4%BB%8B%20-%20Pycharm%E6%95%99%E7%A8%8B%E2%84%A2_files/339140622_76586.jpg)



用户应在运行.py文件时选择开发任务，如下面窗口中所述 -



![img](http://www.thyme.org.cn/gitblog/blog/Pycharm%E7%AE%80%E4%BB%8B%20-%20Pycharm%E6%95%99%E7%A8%8B%E2%84%A2_files/180140622_14824.jpg)



使用以下命令使用名为initialize <project_name>的控制台脚本初始化数据库非常重要 -

initialize_pyramiddemo_db development.ini

Shell

用户可以通过运行项目来启动服务器，该项目将显示如下所示的结果 -

![img](http://www.thyme.org.cn/gitblog/blog/Pycharm%E7%AE%80%E4%BB%8B%20-%20Pycharm%E6%95%99%E7%A8%8B%E2%84%A2_files/338140623_14779.jpg)

Measure

Measure

# Pycharm Flask框架

PyCharm支持Flask框架开发。 通过欢迎屏幕创建新项目，您可以轻松创建新的Flask项目。 可以设置项目的位置和虚拟环境，并选择模板语言以及模板的位置。



![img](http://www.thyme.org.cn/gitblog/blog/Pycharm%E7%AE%80%E4%BB%8B%20-%20Pycharm%E6%95%99%E7%A8%8B%E2%84%A2_files/824140626_97545.jpg)



可以使用 **Run - > Run’‘** 来运行项目。

也可以用这个框架添加一个新的数据源。创建一个名为squema.sql的文件并添加SQL代码来创建一些表。 PyCharm编辑器会识别这些文件并要求您配置数据源并设置为数据库方言。



![img](http://www.thyme.org.cn/gitblog/blog/Pycharm%E7%AE%80%E4%BB%8B%20-%20Pycharm%E6%95%99%E7%A8%8B%E2%84%A2_files/310140627_19982.jpg)



PyCharm会要求您选择想要使用的方言。 可以更改SQL的属性:**Settings** -> **Language and Frameworks** -> **SQL Dialects**，如下图所示 -



![img](http://www.thyme.org.cn/gitblog/blog/Pycharm%E7%AE%80%E4%BB%8B%20-%20Pycharm%E6%95%99%E7%A8%8B%E2%84%A2_files/970140628_21011.jpg)



对于 Flask 编辑器，运行SQL查询的最简单方法是单击查询中的某处，然后单击检查窗口并单击**“Run Query into console”**。

![img](http://www.thyme.org.cn/gitblog/blog/Pycharm%E7%AE%80%E4%BB%8B%20-%20Pycharm%E6%95%99%E7%A8%8B%E2%84%A2_files/328140629_74025.jpg)

Flask框架的用户界面如下所示 -



![img](http://www.thyme.org.cn/gitblog/blog/Pycharm%E7%AE%80%E4%BB%8B%20-%20Pycharm%E6%95%99%E7%A8%8B%E2%84%A2_files/635140629_65665.jpg)

Measure

Measure


