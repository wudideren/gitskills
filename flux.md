# <center>Flux</center>
## Flux是什么
  Flux是一种架构思想，专门解决软件的结构问题。它跟MVC架构是同一类东西，但是更加简单和清晰。Flux存在多种实现
## Flux基本概念
  1. View 视图层
  2. Action 动作，视图层发出的消息（比如mouseClick）
  3. Dispatcher 派发器，用来接收Actions、执行回调函数
  4. Store 数据层，用来存放应用的状态，一点发生变动，就提醒Views要更新页面
    ![flux组成图](D:\local\notes\images\flux.png)
  
  flux最大的特点，是数据的“单向流动”
  1. 用户访问View
  2. View发出用户的Action
  3. Dispatcher收到Action，要求Store进行相应的更新（Dispather只能有一个，并且是全局的）
  4. Store更新后，发出一个“change”事件
  5. View收到“change”事件后，更新页面
  上面过程中，数据总是“单向流动”，任何相邻的部分都不会发生数据的“双向流动”。保证了流程的清晰