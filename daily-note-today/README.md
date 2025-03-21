# 今日笔记

- [English README](https://github.com/frostime/siyuan-plugin-open-diary/blob/master/README-en.md)
- 提交Issue请访问[Github](https://github.com/frostime/siyuan-plugin-open-diary)
- 国内用户可访问[国内托管](https://gitcode.net/frostime/siyuan-plugin-daily-note)

本插件比较适合笔记本比较多的人，用于快速在不同笔记本创建今日的笔记，并将块在不同笔记中移动。

![日记选项](https://gitcode.net/frostime/siyuan-plugin-daily-note/-/raw/master/asset/%E6%97%A5%E8%AE%B0%E9%80%89%E9%A1%B9.png)

## 功能介绍

1. 启动插件时，自动创建/打开今天的笔记
    - 自动打开当前排位第一的笔记本中今天的笔记，如果不存在则自动创建并打开
    - 忽略「思源笔记用户指南」

2. 右上角提供下拉选项/菜单，快速创建/打开今天的笔记
    - 下拉框中按照笔记本顺序排列（见[FAQ](#q-笔记本的排序是如何确定的可以调整吗)），列出所有的笔记本
    - 「思源笔记用户指南」
    - 点击笔记本，自动打开/创建今日的笔记

3. 下拉选项框为各个笔记本提供「是否已经创建了今天的笔记」的标识
    - 若笔记本选项前有「√」标识，表示该笔记本已经创建了笔记

4. 当笔记本有更新（打开/关闭创建笔记本）的时候，请按快捷键「ctrl+alt+u」更新状态
    - 插件可自动追踪笔记的创建情况，但是不会追踪笔记本的状态
    - 因此，当打开、关闭、创建、移动笔记本的时候，请按快捷键「ctrl+alt+u」更新状态

5. 设置面板
    - 可以在设置面板中选择，是否要在开启插件的时候自动打开今天的笔记
    - 设置插件内笔记本排序方案
    - 选择使用下拉框 or 菜单图标
    - 提供「更新」按钮，功能同「Ctrl + alt + u」快捷键
    - 多语言支持

    ![](https://gitcode.net/frostime/siyuan-plugin-daily-note/-/raw/master/asset/Setting.png)

6. 移动块
    - 选中块，「Alt+右键」，可以调处一个移动块的面板
    - 选择笔记本，可以把当前块移动到对应笔记本今天的日记下

    ![](https://gitcode.net/frostime/siyuan-plugin-daily-note/-/raw/master/asset/MoveBlock.png)

## 常见问题

### Q: 插件的使用有什么限制吗？

下拉框模式在部分主题，如 Rem Craft 下无法使用，需要改成菜单模式。

### Q: 我不想每次打开笔记的时候就创建日记。

请在插件设置里关闭「自动打开 Daily Note」。

### Q: 笔记本的排序是如何确定的？可以调整吗？

#### 背景知识

在思源软件本体中，「文档树展示的排序方案」可以分为两类：

1. 自定义排序

    可以自由拖动笔记本进行排序，这个顺序会被思源记录
2. 其他排序

<img src="https://gitcode.net/frostime/siyuan-plugin-daily-note/-/raw/master/asset/%E6%96%87%E6%A1%A3%E6%A0%91%E6%8E%92%E5%BA%8F.png" alt="文档树" style="display:block;margin:auto" />


#### 插件设置

插件一共支持两种排序方案，均可在设置中配置。

![](https://gitcode.net/frostime/siyuan-plugin-daily-note/-/raw/master/asset/Sorting.png)

1. 和自定义排序一致

    此种方案下，插件展示的笔记本排序只会和在「自定义排序」模式下的顺序一致，即使后面更换了别的「文档树展示的排序方案」，插件所展示的笔记本顺序也不会改变。

2. 和文档树一致

    此种方案下，插件展示的笔记本排序和文档树中的顺序完全一致。

在更改了思源的笔记本排序之后，请按 Ctrl + Alt + U 更新状态。


###  Q: 如何更改自动生成日记的笔记本？

插件自动选择排在第一顺位的笔记本生成日记。如果希望更改，就要更改插件内笔记本的顺序。

- 对于使用「自定义排序」方案的用户，请把默认笔记本拉到最上面
- 对于使用其他方案的用户
    1. 切换到「自定义排序」下，把笔记本挪到第一位
    2. 插件设置页面，选择笔记本排序方案为「和自定义排序一致」
    3. 点击下方的 Update 按钮
    4. 如果不想让文档树的显示按照自定义排序，可在完成上面的配置后，自行换成别的排序方案，不会影响到插件内的顺序

### Q: 为什么我「Alt + 右键」有时候无法呼出移动菜单？

首先请确保点击的是块旁边的图标；如果仍然无法呼出，可以试着按快捷键「Ctrl + Alt +U」更新全局状态，然后再次尝试。

### Q: 为什么移动标题块的时候这么卡？

并不是卡，而是移动块有一个过程。

思源笔记中标题块并不是一个容器块，没有办法一次性移动完成，当前移动标题块内部的算法是插件自己实现的，需要识别哪些块属于当前标题下，所以比较慢。

## CHANGELOG

[CHANGELOG](https://github.com/frostime/siyuan-plugin-open-diary/blob/master/CHANGELOG.md)
