## 一自我介绍与职业规划

### 1. 请介绍一下你自己
Hi, My name is Damon Young.
I've been working as a front-end engineer for over 7 years.
I've built many web apps using React.
I'm especially skilled at mobile web development
and creating user-friendly interactions.

I started my career during my internship at ZBJ,
the largest internet company in ChongQing, China.
At that time, I helped upgrade their official website to version 2.0 from jQuery to Vue.
Since then, I've worked in different industries like e-commerce platform and banking systems.

At my last company, I was in charge of banking rewards systems.
I also built a shared admin system template,
to help unify the user experience across all our internal systems.

I'm also a top 20 contributor to the open-source project Ant Design Mobile,
which has 10,000 stars on github.
I helped fix UI bugs and improve test coverage.

I'm looking forward to contributing to your team and projects. Thanks.
### 2. 你为什么想来日本

### 3. 你觉得在日本工作挑战是什么
I think One of my challenges is communication.
In a international environment, I need to communicate with people from different backgrounds and cultures.
I must to make sure my communication is clear and efficient
But I have confidence in my English skills, Also, I'm working on my Japanese language
So I can overcome this challenge.

### 4. 你了解乐天么？
Yes, I know that Rakuten is one of the major tech companies in Japan.
It started as an e-commerce platform,
now it offers many services like mobile networks, payments, and a points system.
I often use Rakuten Points across different services,
which I think creates strong user loyalty.
I think Rakuten's business is very broad and deeply connected to people's daily lives.

### 5. 你为什么选择乐天
I’ve actually wanted to apply for a job at Rakuten for a long time.
I also have many friends working there, and they all speak very highly of Rakuten.
I really like Rakuten's international environment
and enjoy working with people from different backgrounds.
I have experience in the e-commerce and banking industries.
I believe my skills and experience make me a great match for this job.

### 6. 你觉得你的优势是什么
I think my strengths are:
1. I am a proactive person so I always face challenges with a positive attitude.
2. I have strong problem-solving skills so I can make sure projects run smoothly.
3. I have experience in building resuable components and ensure code quality in the long term.
I have confidence contribute to the team and keep everything run smoothly.

### 7. 你工作中遇到的最大的挑战

### 8. 你未来的职业规划是什么
In the short term, my goal is to let myself get used to the international environment and culture,
In the long term, I want to become a system architect,
helping the team and company succeed in the global market.

## 二项目介绍

### 9. 介绍一下你最近的项目
Fumin Bank provides financial services like:
- savings
- loan services
- wealth products
- reward points system
I was in charge of the banking reward points system.
When Users saving their money in bank or buying wealth products,
they could earn points.
and then use those points in a points mall to get products or services.

This system had two parts:
- A mobile web page points mall inside the Fumin Bank app.(WebView-based page inside the app)
Users can check and use their points to get products or services.
- An admin management project to manage merchants and products things like that.

### 10. 你在项目中负责什么
My responsibility:
Led the team to develop the system make sure we delivered high-quality features on time.
worked closely with the product and backend teams to confirm requirements
reviewed code, make sure code quality in the long term.

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
use tools like ESLint and Prettier and git hooks to ensure code quality, build a standard code style make sure everyone follows it.
use CI/CD to automate testing and deployment,
and always do code reviews before merging code.
and deliver the project on time.
I think do this three steps well, we can deliver a high-quality project on time.

### 18. 你有过组件设计的经验么？你如何进行组件设计
- Yes, I'v always built a resuable component in my daily work.  
- I always design a components in three step.
- one is notice the repeat patterns during development.
- two think and research the best practices solutions.
- three design the component API like props, events.
then coding and test.
always add unit tests and provide clear documentation for the component.
- When I develop our reward points admin systems, I noticed the table logic was always repeated.  
Every page required:
- fetching data,managing loading state,and then updating table state, and rendering the table.
- so I decided to extract these common logic into a reusable table component. developers only need to provide an API endpoint, and then the table component would handle everything else. it's pretty easy to use.
that's how I designed the reusable table component in my admin system.

### 19. 你如何进行项目迁移或者重构

### 20. 你如何管理版本，你们上线的流程是怎样的
we use Git for version control. and flow the trunk-based development model. 
the process is like this:
1. Development stage: Features are developed and tested on the develop branch.
2. Integration testing stage: After development, features are merged into the test branch
run a full integration testing.
3. Code review stage: when finish the testing, we create a pull request with code review to ensure code quality.
4. Pre-release stage: After code review, the code is merged into the master branch. and deployed to a staging environment, and stakeholders check the release.
5. Production release: After stakeholder check complete,
 the release is promoted to production, We check the production environment to ensure everything works as expected. and submit a final validation report to stakeholders.

### 21. CI/CD 的流程是怎样的
we use GitLab CI/CD to automate the entire process from development to release.

CI pipeline runs automatically to check code quality, run tests, and build the project.

CD pipeline deploys the code to staging for testing, and after validation, it is deployed to production automatically.

### 22. 你如何进行敏捷管理,

### 23. 设计产品后端沟通的工具是什么，如何沟通 Swagger 如何生成类型定义
we use Swagger to document our API endpoints.
Swagger generates API documentation and provides a UI for testing endpoints.
We use Swagger Codegen to generate TypeScript type definitions
it really helps us keep the frontend and backend in sync.

### 24.你遇到过哪些后端接口设计不合理的情况，怎么处理？

## 四技术栈

### 25. 前端安全 csrf xss
CSRF: CSRF happens because browsers trust cookies, not pages, and attackers abuse this behavior to forge cross-site requests.
This allows attackers to use HTML tags like <img> or <form> to trigger fake requests to another site where you are already logged in.
For example, when I am logged in on Site A, visiting a malicious Site B. In site B can trigger fake requests to Site A using simple HTML tags without my intention.
I prevent it by using CSRF tokens, SameSite cookies, and double confirm on sensitive actions.

### 26. 你用过哪些 css 预处理器
I have used Sass and Less in my projects.
Sass is a powerful CSS preprocessor that allows nesting, variables, mixins, and functions.
It helps write cleaner and more maintainable CSS code.

### 27. 函数式组件和类组件的区别

Function components use useState hook to manage state.
Class components use this.state and this.setState to manage state.

Function components use useEffect to handle side effects like data fetching.
Class components use lifecycle methods like componentDidMount, componentDidUpdate, and componentWillUnmount.

### 28. 你做过响应式设计吗？你如何处理不同屏幕尺寸的适配
Yes, I have worked on responsive projects.
1. I use CSS media to adjust font sizes, padding, layouts, and component visibile or not for different breakpoints
2. I use CSS Flexbox and Grid to create flexible layouts can handle different screen sizes.

### 29. 你的项目是如何处理组件的？
I follow three key principles for component design:
1. I split component by responsibility, some handle UI, some handle  data and logic. keep components small resuable and easy to test.
2. build components use configuration driven props, make them easy to use and flixible to support different use cases.
3.I use a clear folder structure: like pages, layouts, common and good naming conventions to make it easy to read and maintain.

### 30.Webpack 和 Vite 的差异和选择理由
1.Vite is faster in development because it uses native ES modules and does on-demand loading. Webpack needs to bundle first, so dev server is slower.
2.Vite uses Rollup for production builds, and webpack uses its own bundler. In most cases Vite's production build is faster and smaller.
3. Vite has a simple configuration setting while Webpack has more complex settings, but Webpack has more plugins and loaders available.

so I choose Vite for new projects because it is faster and easier to use.
if I need complex custom config or specific plugins, I might choose Webpack.
### 31. 客户端渲染的缺点
1. user will see a blank page until the JavaScript loads and renders the content.
2. SEO is not good.

### 32. TypeScript 的优点和缺点
1. TypeScript provides static type checking, which helps catch errors early in development.
2. It has better IDE support like auto-completion and type checking.
3. write type may be time-consuming, especially for complex logic.
4. Third-party libraries may not have type definitions, which can lead to type errors, or require developers to write type files by themselves.

### 33. TypeScript 中的 interface 和 type 的区别
interface is for object shapes, it can extend and merge.
type supports unions, primitives, but cannot merge.

### 34. 你如何设计 Redux，如何设计 store，redux 运行的流程

### 35. 你使用过 zustand 吗？它和 redux 的区别

### 36. react hooks,自定义 hooks 的使用场景

### 37. useState 和 useReducer 的区别

### 38. useRef 的使用场景

### 39. useMemo 和 useCallback 的区别
useMemo returns a memoized value.
useCallback returns a memoized function.
use useMemo to avoid expensive recalculations, like sorting data. use it to recalculate only when dependencies change.
use useCallback to prevent unnecessary function re-creations, useful when passing callbacks function to child components. with useCallback, the function will recreate only when its dependencies change.

### 40. 你如何处理跨域问题
Cross-origin happens when the protocol, domain, or port is different between frontend and backend.
base the same-origin policy, browsers block cross-origin requests for security reasons.
In development, I use proxy like Vite proxy or Webpack proxy to forward requests and avoid CORS issues.
In peoject, set CORS headers on the backend to allow specific origins.
Sometimes use JSONP for GET requests.

### 41. 你如何处理浏览器兼容性问题
1.use Can I use website to check feature support.
2. use polyfills like core-js for missing features
3. use auto-prefixer to add prefixes for CSS properties.
4. if the browser doesn't support a feature, I use a fallback solution.

### 42. 你如何处理浏览器缓存
1. use HTTP cache headers, like Cache-Control and ETag, to control how browsers cache static files.
2. use hash in file names to ensure when files change, browsers will load the new version.
### 43. 前端路由的原理，使用什么前端路由
Front-end routing uses browser history or hash to change the URL without refreshing the page.
It listens for URL changes and renders different components based on the current route.
I use React Router for SPA routing,
BrowserRouter has a clean URL without hash, and search engines can index it well.
and HashRouter uses hash in the URL, and search engines may ignore it.
If use HashRouter, it doesn't need server-side support,
if use BrowserRouter need server-side support, it need to return the main HTML document for all routes.

### 44.虚拟 DOM 的原理和使用场景
1. Virtual DOM is a JavaScript object that represents the real DOM in memory.
2. When state changes, React creates a new virtual DOM, compares it with the previous one (diffing), and only updates the real DOM nodes that changed (patching).
3. this can faster updates by reducing direct DOM operations,
### 45. 你用过 SSR 吗？有什么优点
Yes, I have used SSR with frameworks like Nuxt.js. At my first company, we needed to improve initial page load speed and a better SEO, so we 
upgrated the website to use SSR.
1. SSR generates the HTML on the server side, so the browser can render the page right away. so it improves initial page load speed and SEO.

### 46.SSR 页面“水合”（hydration）是什么？浏览器中发生了什么？
First, with SSR, the server sends a static HTML page to the browser.
Then, React runs on the client to attach event listeners and make the page interactive
— this step is called hydration.
So hydration connects the HTML to JavaScript logic, enable full React features after the initial load.
### 47.Babel 是做什么的
1. converts modern JavaScript code into older versions so it can run on more browsers.
2. compiles JSX syntax into JavaScript functions.

### 48.浏览器渲染流程（Critical Rendering Path）
1. The browser load HTML and builds the DOM tree.
2. It loads CSS and builds the CSSOM tree.
3. It combines the DOM and CSSOM to create the Render Tree.
1. Layout: calculates each element’s position and size.
2. Paint: fills in colors, borders, text.
3. Composite: draws everything on the screen.

### 49.什么是 Repaint 和 Reflow（Layout thrashing 如何优化）
Reflow happens when layout or size changes.The browser recalculates positions and sizes of elements. like changing width, margin, adding or removing elements.
Repaint happens when only styles change, but layout stays the same.
Example: changing color, background, visibility.
I think reducing reflow improves performance.
### 50.浏览器输入 URL 后发生了什么？
1. The browser resolves the domain to an IP address via DNS.
2. opens a TCP connection with Three-way Handshake and sends an request to the server.
3. The server responds with HTML, CSS, JS, and the browser starts building the DOM and CSSOM, combining them into a Render Tree.
and then draws everything on the screen.
### 51.HTTP2, HTTP3 有哪些优势

### 52.什么时候选择 Context API，什么时候选择 Redux，什么时候用 Zustand？
Context API is built-in React, good for simple global state like theme or user info. but it can cause the whole component tree to re-render, even if only part changes.
Redux is a separate library, better for complex state and business logic across large apps. it only updates components that use the changed state.
but it requires more setup and boilerplate code.

## 五代码质量

### 53. 你如何保证代码质量
I want to talk about this in three parts:
1. In development stage, I use tools to enforce coding standards and style.
For example, use ESLint to check code quality.
Use prettier to ensure consistent code style.
use Git Hooks with Husky to run checks before commits.
2. In coding stage, write unit tests using Jest and use React Testing Library to do integration tests. and always extract common logic into components or functions to avoid duplication code.
3. In review stage, to check performance and edge cases.
In this way, I can ensure code quality in the long term.

### 54. 你如何做 review code
We follow a consistent coding style — I foucs on everyone to follow our coding standards.
I focus on writing clear, easy-to-read code, with good naming and comments.
I also make sure to extract common logic into components or functions to avoid duplication code. make the project easy to maintain in the long term.
We also pay attention to performance issues and edge cases during reviews.

### 55. 你有提出什么技术建议么给团队提升开发效率的么
I introduced Vite instead of Webpack to improve development experience.
we first tried vite in a less ungent project, we test the full development process, and it worked well. with this experience, we decided to use Vite in all new projects.
It really helped the team improve development experience.

### 56.Git Hooks, Lint Staged, Commitlint 是否使用过
Yes, I have used Git Hooks with Husky to automate checks during commits.
I use lint-staged to run lint and format only on staged files, keeping code clean without slowing down the commit process.
I also use commitlint to enforce commit message standards based on conventional commits.
### 57.ESLint, Prettier 配置细节

## 团队管理

### 58. 你有带过团队成员吗？你如何激励他们
- I give team members respect by trusting them to take ownership of their work.
- I guide them notice the repeat patterns when they write code, and encourage them thinking
- and then let them to build resuable components or functions.
- I think it's better than just let them following instructions.
### 59. 你如何进行质量管理
I think we can do three things to ensure quality:
1. make sure we konw the requirements well before starting the project.
2. use tools like ESLint and Prettier to enforce coding standards and style.
3. write unit tests using Jest and React Testing Library to do integration tests, to ensure code run smoothly.
4. do code reviews to make sure code quality and performance.
## 测试

### 62.单元测试、集成测试、端到端测试（E2E）的区别和实际应用

### 63.Jest + React Testing Library 的实际使用经验

### 64.如何测试 React hooks 和异步逻辑

## 六故障排查

### 65.你有监控系统的经验吗

### 66.你前端故障处理流程是怎样的，你如何处理
First, we had a internal monitoring system to check frontend errors and sometimes we get bug reports from users.
Then, I reproduce the issue in a local environment to location the problem.
I always use browser developer tools like the Console to check errors and logs,
and the Network tab to check API requests and responses is correct.
and I also use debug tools to set breakpoints.
After I location the problem, I fix it and test it in local environment.
### 67.解决一次故障大概多久
it depends on the issue complexity, but usually I can fix it within a few hours.

## 学习与成长

### 68. 你是如何学习新技术的
First, i start with read official documentation to understand the basics.
Then, I try to build small projects to practice or use the new technology to build a side project.
I share my knowledge with the team and sometimes I recommend new technologies to improve our workflow.

### 69. 你平时关注哪些技术社区或博客
I follow several tech blogs and communities:
- I follow the official React blog for updates and best practices.
- I read CSS Tricks for CSS tips and tricks.
- I follow JavaScript Weekly for the latest JavaScript news.

### 70. 你如何保持自己的技术更新
I keep my skills up to date in two ways:
Practice with side projects
I often use new technologies in my side projects to quickly get experience.
In my job, I always try to introduce new tools or techniques, as long as it make sure it doesn't affect code quality or deadlines.
I think it’s important to leave the comfort zone.

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

Webpack 或 Vite 如何做代码分包？说明 manualChunks 或 chunk 名称生成机制。

你在项目中做过哪些包体积优化？请举例说明。

Browser 的 HTTP 缓存机制如何工作？你会怎么配置 headers？

如何实现 React 组件库的自动样式加载？CSS Modules 或 styled-components 工作原理？

算法题：请实现一个求数组中最长递增子序列（LIS）的方法，并说明时间复杂度。
