## shell + python 有什么优点:
  **参数input的问题**:python中我要如何获取输入？手动修改源代码很费眼睛，因为变量初始化待可能都不在同一个脚本中，另外碰到长度三百行以上甚至一千多行的代码，找到变量并且修改更是感到绝望。为了改一个变量调试半小时。<br>
  比较优雅的可以用config来读取，但对读代码的人来说不是很友好，总得开一个config来看一下是一个什么样的变量，是一个str还是一个什么东西。不利于整体阅读。<br>
  但用bash的话，首先你可以直接知道这个python脚本需要哪些参数，什么input,什么是output。而且终于不必再每次都打开那个该死的编辑器然后再open folder。因为如果不打开folder就无法读到正确的工作目录，import都是个问题。 <br>
  **多脚本协作的问题**：经常的，一个任务会被一次次拆分，然后再一次次合并，那么在python中就会产生这样的问题，我要实现一个跟据txt文件的时间线来剪辑视频的脚本，我要有基础的utils。就是读取txt并且解析成字典的函数，然后要有读取视频并且按照字典来剪辑的函数。以及把它们汇集到一起的函数。以及再到实际任务中可能需要应对批处理的函数。这是一个三级封装。 <br>
  那么当我修改了解析txt的函数，就可能牵一发而动全身。我的每一级都得修改来适配。但这实际上每一级都是一次重复工作。有多少级就重复多少次。<br>
  而使用bash的情况是，我们想要直接用bash把这些底层的函数直接整合到一起。如果有需要修改底层，也只需要修改与它交互待部分。这会比自己写一个main.py然后把所有东西炖在一起优雅得多。 <br>
  关键是，我不用再打开那个该死的编辑器来运行了。我可以直接双击.sh或者.bat.
