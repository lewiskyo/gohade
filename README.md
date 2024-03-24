# gohade
a web framework

# 01讲
基于net/http, 实现一个简单的http服务器, 无任何处理和响应

# 02讲
## add framework/context.go, 为框架添加上下文Context, 支持以下能力
  1. 判断是否超时
  2. 传递变量
  3. 从request,form表单读取变量, 并转成特定类型, 例如int,string,[]string,json
  4. 封装按照text,html,json这三种常用格式返回数据的函数

## add framework/context.go, 定义了controller接口, 后续业务controller都要实现该接口

## modify framework/core.go
   1. 为Core添加静态路由


## add controller.go, 继承framework/controller, 实现一个处理器 FooControllerHandler
   1. 支持捕捉panic;

## add route.go, 将foo路由绑定到 FooControllerHandler

ps: 代码运行需要先go build