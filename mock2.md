1. 请解释 JavaScript 的闭包机制，它是如何工作的？
- What is a closure in JavaScript？
A closure is when a function remembers the variables from where it was defined.
Even if we run the function later, it still knows those values.
For example:
I define a function called outer. Inside outer function, I create a variable A.
Then I return another function that just returns A.
Even after function outer is done, the returned function still remembers variable A.


2. 原型链如何实现 JS 对象的继承？有哪些底层执行顺序？
- How does prototype-based inheritance work in JavaScript
- Can you explain the prototype chain

In JavaScript, each object has a double underscore__proto__.
When we access a property, JavaScript first checks the object itself.
If not found, it follows the double underscore __proto__ chain.
It goes up until Object.prototype.
If the property is still not found, it returns undefined.

3. 事件循环是如何调度宏任务和微任务的？请举例说明。
- How does the JavaScript event loop work
- What’s the difference between macro tasks and micro tasks
- Can you give an example with setTimeout and Promise

JavaScript uses an event loop to manage tasks.
Tasks are split into macro tasks and micro tasks.
The event loop runs macro tasks one by one.
After each macro task, JavaScript runs all the micro tasks.
then it moves to the next macro task.

4. Promise 的 .then() 为什么是异步的？底层机制是多少？
.then() is asynchronous because the ECMAScript standard defines it that way.
Even if the Promise is resolved, the callback runs later.
It goes into the microtask queue.
JavaScript runs all sync code first, then clears microtasks.

5. React 中 useEffect、useMemo、useCallback 有什么区别和使用场景？
- What’s the difference between useEffect, useMemo, and useCallback
useEffect runs side effects like data fetch or DOM changes.
useMemo caches expensive calculations to avoid re-running them.
useCallback returns a memoized function to avoid re-renders when passing functions as props.
I use useEffect for lifecycle logic,
useMemo for performance when computing heavy values,
and useCallback to keep stable function references.


如何实现可按需加载组件？请结合 React.lazy 和 import() 说明。

SSR 页面“水合”（hydration）是什么？浏览器中发生了什么？

Webpack 或 Vite 如何做代码分包？说明 manualChunks 或 chunk 名称生成机制。

你在项目中做过哪些包体积优化？请举例说明。

Browser 的 HTTP 缓存机制如何工作？你会怎么配置 headers？

如何实现 React 组件库的自动样式加载？CSS Modules 或 styled-components 工作原理？

算法题：请实现一个求数组中最长递增子序列（LIS）的方法，并说明时间复杂度。