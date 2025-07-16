## 一自我介绍与职业规划

### 1. 请介绍一下你自己

### 2. 你为什么想来日本

### 3. 你觉得在日本工作挑战是什么

### 4. 你了解乐天么？

### 5. 你为什么选择乐天

### 6. 你觉得你的优势是什么

### 7. 你遇到最大的挑战

### 8. 你未来的职业规划是什么

## 二项目介绍

### 9. 介绍一下你最近的项目

### 10. 你在项目中负责什么

### 11. 你有主导项目的经验么

## 三性能优化

### 12.你如何衡量前端性能

use Chrome DevTools to check load speed and render time.  
use Performance panel, focus on LCP【Largest Contentful Paint】 to check how fast first screen shows,  
CLS【Cumulative Layout Shift】 to check if layout shifts.  
INP【Interaction to Next Paint】 to check how fast page reacts after click.  
use Rendering panel, check FPS【Frames Per Second】 to check smoothness.  
use Network panel → check request size, time, and waterfall.  
use Coverage tab, check unused code size.  
use Lighthouse to check score, SEO.  
use webpack-bundle-analyzer to check bundle size. 
I usally use this tool to check performance.

### 13.你在项目中做过哪些性能优化
I want to talk about this in three parts:  
- reduce unnecessary requests  
use lazy loading just when the image enters the viewport  
merging files to avoid the multiple small requests  
use browser caching by setting proper response headers to avoid re-fetching  
- reduce resource size  
use webpack or vite to enable compression, minify JS and CSS files  
tree-shaking to remove unused code  
compress images size used in the project  
- improve rendering performance  
use useMemo, useCallback, shouldComponentUpdate to avoid re-renders  
I use React.lazy() and Suspense with React Router to do code splitting.  
The page only loads the component when visits the route.  
That's pretty much what I did.  

### 14.为什么用 LazyLoading 懒加载，背景是什么，懒加载用在了哪里
I want to talk about lazyloading in three parts:  
1. lazy load the image when it enters the viewport  
I always use IntersectionObserver API to do that.  
2. In React project, I use React.lazy() and Suspense with React Router to do code splitting.  
only load the component when visits the route.  
3. use es module dynamic import to load the component only when needed.  
In my project, I dynamically import a chart library component.  
so it doesn't load the component until the user clicks the button to show the chart.  
4. with lazy loading, can improve initial page load speed, this three parts are what I think about lazy loading.  

### 15.性能调优经验
In our rewards points admin system, the ops team needed to download user order data as Excel files.  
For 30,000 rows, it's a big list  
At first, the page would freeze during export.  
Then I use Web Worker to create a separate thread for the export logic.  
I moved the export logic to a Web Worker.  
Inside the worker, I did  
Batch API requests for all pages.  
Merging all order data.  
Generate Excel Blob inside the worker.  
After the worker finished, it sent the Blob back to the main thread, which triggered the file download.  
After doing this, the UI keep smooth and have a better user experience.  

## 前端架构

### 16. 你拿到一个项目后，你如何推进
I usually follow three steps:  

1. Understand the requirements before starting  
I first have a meeting with product managers/ designers/ backend engineers/ to check the requirements.
kepp everyone on the same page before starting the project.
with product clarify the business 
talk with designers to check the design and user experience.
work with backend to understand the API and data structure.

2. Plan the project structure and timeline
for example seperate the stable and frequently changing parts,  
do a technical selection, base on the requirements and team background,
then set a timeline and Key milestones.

3. then I Focus on quality and delivery
use tools like ESLint and Prettier to ensure code quality,
review code with team members to catch issues early
and ensure everyone follows the same standards.

I think do this three steps well, we can deliver a high-quality project on time.

### 18. 你有过组件设计的经验么？你如何进行组件设计
Yes, I'v always built a resuable component in my daily work.  
I always design a components in three step.
one is notice the repeat patterns during development.
two think and research the best practices solutions.
three design the component API like props, events.
then coding and test.
always add unit tests and provide clear documentation for the component.
When I design our reward points admin systems, I noticed the table logic was always repeated.
Every page required:
fetching data,managing loading state,and then updating table state, and rendering the table.
so I decided to extract these common logic into a reusable table component.developers only need to provide an API endpoint, and then the table component would handle everything else. it's pretty easy to use.
that's how I designed the reusable table component in my admin system.

### 19. 你如何进行项目迁移或者重构

### 20. 你如何管理版本，你们上线的流程是怎样的

### 21. CI/CD 的流程是怎样的

### 22. 你如何进行敏捷管理,

### 23. 设计产品后端沟通的工具是什么，如何沟通 Swagger 如何生成类型定义

### 24.你遇到过哪些后端接口设计不合理的情况，怎么处理？

## 四技术栈

### 25. 前端安全 csrf xss

### 26. 你用过哪些 css 预处理器

### 27. 函数式组件和类组件的区别

### 28. 你做过响应式设计吗？你如何处理不同屏幕尺寸的适配

### 29. 你的项目是如何处理组件的？

### 30.Webpack 和 Vite 的差异和选择理由

### 31. 客户端渲染的缺点

### 32. TypeScript 的优点和缺点

### 33. TypeScript 中的 interface 和 type 的区别

### 34. 你如何设计 Redux，如何设计 store，redux 运行的流程

### 35. 你使用过 zustand 吗？它和 redux 的区别

### 36. react hooks,自定义 hooks 的使用场景

### 37. useState 和 useReducer 的区别

### 38. useRef 的使用场景

### 39. useMemo 和 useCallback 的区别

### 40. 你如何处理跨域问题

### 41. 你如何处理浏览器兼容性问题

### 42. 你如何处理浏览器缓存

### 43. 前端路由的原理，使用什么前端路由

### 44.虚拟 DOM 的原理和实现

### 45. 你用过 SSR 吗？有什么优点

### 46.SSR 页面“水合”（hydration）是什么？浏览器中发生了什么？

### 47.Babel 是做什么的

### 48.浏览器渲染流程（Critical Rendering Path）

### 49.什么是 Repaint 和 Reflow（Layout thrashing 如何优化）

### 50.浏览器输入 URL 后发生了什么？

### 51.HTTP2, HTTP3 有哪些优势

### 52.什么时候选择 Context API，什么时候选择 Redux，什么时候用 Zustand？

## 五代码质量

### 53. 你如何保证代码质量

### 54. 你如何做 review code

### 55. 你有提出什么技术建议么给团队提升开发效率的么

### 56.Git Hooks, Lint Staged, Commitlint 是否使用过

### 57.ESLint, Prettier 配置细节

## 团队管理

### 58. 你有带过团队成员吗？你如何激励他们

### 59. 你如何进行质量管理

### 60. 如何进行代码 review

### 61. 如何确保代码质量

## 测试

### 62.单元测试、集成测试、端到端测试（E2E）的区别和实际应用

### 63.Jest + React Testing Library 的实际使用经验

### 64.如何测试 React hooks 和异步逻辑

## 六故障排查

### 65.你有监控系统的经验吗

### 66.你前端故障处理流程是怎样的，你如何处理

### 67.解决一次故障大概多久

## 学习与成长

### 68. 你是如何学习新技术的

### 69. 你平时关注哪些技术社区或博客

### 70. 你如何保持自己的技术更新

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

In JavaScript, each object has a double underscore**proto**.
When we access a property, JavaScript first checks the object itself.
If not found, it follows the double underscore **proto** chain.
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
