# <center>Java面试题</center>
## Object类有哪些方法
### 获取代表类的Class对象
   `public final native Class<?> getClass()`
### 对象比较
   * `public native int hashCode()`
   * `public boolean equals(Object obj) {return (this == obj)}`
### 对象复制
   `protected native Object clone() throws CloneNotSupportedException`
### 获取对象字符串
   `public String toString() {return getClass().getName + "@" + Integer.toHexString(hashCode())}`
### 多线程相关
   * `public final native void notify()`
   * `public final native void notifyAll()`
   * `public final native void wait(long timeout) throws InterruptedException`
   * ```java
     public final void wait(long timeout, int nanos) thorws InterruptedException {
         if (timeout < 0) {
             throw new IllegalArgumentExcption("timeout value is negative")
         }
         if (nanos < 0 || nanos > 999999) {
             thow new IllegalArugumentionException("nanosecond timeout value out of range")
         }
         if (nanos > 0 ) {
             timeout++
         }
         wait(timeout)
     }
     ```
   * `public final void wait thows InterruptedException {wait(0)}`  
### 清理
   `protected void fianlize() throws Throwable {}`

