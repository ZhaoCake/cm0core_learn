# 搭建进度

*参考知乎上的《SOC设计》专栏进行学习*

## 2024-11-3

今天开始。先使用工具搭建总线。之前也使用过。
搭建完成，需要阅读生成的总线代码，理解总线结构。

arm design start 实在是提供了很多的工具，这样一来就可以快速将注意力集中到SOC的搭建上了。

我先将需要的东西复制过来，对于arm design中加密的`core`,我写入了`.gitignore`中，需要自行下载到对应位置。

即使是这样，观察这个被继承之后的核，也还是具备很多接口

连着看了四篇文章，应该说对于要做的事情有认识了。我应该启动我的IDE，并且创建工程，添加上一块ram,并且将其通过cmsdk提供的sram2ahb接口连接到总线上。

工程准备完成，现在我应该把核、itcm、dtcm都挂载到总线上去。

挂完了，可是gowin怎么把我的信号都优化掉了？按照文档里添加了keep注释也还是没用啊，疑惑，看来是时候收手了。