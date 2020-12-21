# context

context是级连上下文，可以做级连取消、传送数据等。

## 原则

- 尽量不要在context中传递业务参数。业务参数应在函数签名中显式传递。

- 应将context作为函数的第一个参数。
- 要为操作设置超时时间。
- 使用context做超时取消时需要做收敛。如context到达服务A时还剩3秒，A调用下游服务B时超过1秒就要取消。此时A传递给B的context应该设置为较小者（即1秒的超时）。反之，如果到达A时还剩1秒，A调用B要3秒的超时，此时A传给B的同样是较小者，也就是1秒的超时。
- 如果参数是context，不要传递空值进去。如果不知道传递什么，请传context.TODO()进去。context.TODO()与context.Background()底层结构其实是相同的。

