# panic

panic意味着挂了，通常是不可恢复的。

## 原则

- 不要像 try catch 那样用 panic recover。

- 只在main和init时进行主动panic。

- kit库最好先编写Recover中间件，记录panic防止程序终止。

- 野生goroutine可能导致内存泄漏，而且一旦发生panic，会导致整个程序挂掉。最好使用类似于下面的代码开启goroutine:

```go
func Go(f func()) {
    wg.Add(1)
    go func() {
        defer func() {
	    if err := recover(); err != nil {
	        debug.PrintStack()
	    }
	    wg.Done()
  	}()

  	f()
     }()
    
    wg.Wait()
}
```
