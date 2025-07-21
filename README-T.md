## 技术面试
- 技术相关的面试题
### 1. 你怎么优化前端性能
- what did you implement and how did you improve the performance?
```txt
I want to talk about this in three parts:
1. reduce unnecessary requests to improve performance
- the most used method is lazy loading,
when the image enters the viewport and then load the image dynamically.
use React.lazy() and Suspense to do route-based code splitting, we user
visit the route and then load the component  when needed.
use dynamic import to load components only when needed.
- use browser caching by setting proper response headers also can reduce requests.
2. reduce resource size to improve performance
- use webpack or vite to enable compression, minify JS and CSS files
- do tree-shaking to remove unused code
3. improve rendering performance
- for React projects, use useMemo, useCallback, shouldComponentUpdate to avoid unnecessary re-renders
- use virtual scrolling if you need render a long list
That's pretty much what I did at previous company.
```
### 2. 怎么测量前端性能
- how do you measure the system performance?
```txt
- use lighthouse to check performance, and SEO.
- use Chrome DevTools to check load speed and render time.
- use Performance panel focus on LCP, CLS, and INP to check page speed and user experience.
- LCP shows first screen loading speed, CLS checks layout stability, and INP reflects UI responsiveness after user actions.
- use Rendering panel to monitor Frame Rate FPS.
- use Coverage tab check the unused code.
- use network panel to check API requests and responses.
- use webpack-bundle-analyzer to check bundle size.
- That’s pretty much based on these metrics.
```
### 3. 怎么管理代码质量
- how do you usually manage code quality?
```txt
we do this in three ways:
1. use tools like ESLint and Prettier to enforce standards code style.
2. by testing, we write unit tests and integration tests to ensure code run smoothly
3. by code reviews, we check performance and edge cases to make sure the project easy to maintain in the long term.
```
### 4. 过去有没有推荐过技术或者策略
- have you suggested any new technology or strategy in your past experience?
```txt
I introduced Vite instead of Webpack to improve development experience.
It helped the team reduce build time by 50%
```
### 5. 你是如何发现和定位前端问题的
- For trouble shooting, how do you handle it
```txt
- I use browser developer tools like the Console panel to console logs
- and the Network tab panel to check API requests and responses.
- I also use debug tools to set breakpoints.
with these tools, I can easily locate the issues.
```
### 6. 你处理问题的步骤是什么
- What is the trouble handling flow
```txt
My flow is: 
confirm and understand the issue before starting,
reproduce in local environment,
locate the bug in the code
use chrome dev tools to console logs or debug.
create a fix branch and fix the bug and test
if everything is ok, then commit the code and deploy test environment to QA team.
```
### 7 你遇到问题的时候怎么处理和解决
```txt
My flow is: 
confirm and understand the issue before starting,
reproduce in local environment,
locate the bug in the code
use chrome dev tools to console logs or debug.
create a fix branch and fix the bug and test
if everything is ok, then commit the code and deploy test environment to QA team.
```
### 8. 你处理问题一般需要多久
- How long does it take to fix a bug?
```txt
It depends on the situation.
If it's a simple bug, I can fix it in a few minutes.
I remember the longest time is 2 hours, we use a UI library, I need to check the source code and find the issue.
```

### 9. 你项目中用过figma么？
- Have you used Figma in your project?
```txt
not really, we didn’t use Figma in my previous company in China, we used Lanhu, it's kind like Figma.
I often used it for checking design and getting CSS values
```
### 10. 你用CSS做什么
- Why do you use CSS?
```txt
I use CSS to add style to HTML elements 
make the page beautiful and have a good user experience.
```
### 11. 在CSS中用过函数么
- Can you use a function for CSS?
```txt
Yes, I can use CSS functions like calc() to calculate values like width and height,
use var() to define and reuse css variables
```
### 12. 你们实施过什么测试
- What kind of tests have you implemented?
```txt
- we use Jest to do unit test for components and functions
- we use React Testing Library to do Integration testing make sure different parts can work together.
For example: to simulate user actions like clicks, trigger API calls, and check if the UI updates properly
we do the Performance testing use chrome DevTools to check load speed and render time.
also we use Lighthouse to check performance and SEO.
In my previous company, the QA team had many mobile devices, so we do real device testing to check the browser compatibility.
```
### 13. 你有监控系统的经验么
- Do you have experience in monitoring systems?
```txt
Yes, I have experience in monitoring systems.
In my previous company, we had an internal monitoring system to check frontend errors.
We tracked JavaScript errors, API request fail, and performance everyday.
When an issue happened, we flowed a process:
```
### 14. 性能调优
- How do you tunning performance?
```txt
In my previous company we have a rewards points admin system,
the ops team needed to download user order data as Excel files.
For 30,000 rows, it's a big list
Then I use Web Worker to create a separate thread for the export logic.  
I moved the export logic to a Web Worker.  
// Inside the worker, I did
// Batch API requests for all pages.  
// Merging all order data.  
// Generate Excel Blob inside the worker.  
After the worker finished, it call back to the main thread, which triggered the file download.
After doing this, we imporve the user experience a lot
and the page run smoothly without blocking.
```

### 15. 从零开始的系统设计的经验
- Do you have experience in designing a system from scratch?
```txt
Yes, I have experience.
In my previous company, I design the banking rewards points system.
I think the first important thing is talk to stakeholders to understand the business requirements berfore starting.
Then plan the project structure, and seperate the stable and frequently update parts, to avoid side effects.
Then do the technical selection base on the requirements and user experience.
Then the rest is to develop the system step by step.
```

### 16.从零开始的组件设计经验
- Do you have experience in designing components from scratch?
```txt
- Yes, I'v always built a resuable component in my daily work.
- I always design a components in three step.
- one is notice the repeat patterns during development.
- two think and design a best practices solutions to avoid code duplication.
- three design the component API like props, events.
- then coding and add unit tests.
- In the end always provide clear documentation for the component.
- When I develop our reward points admin systems, I noticed the table logic was always repeated.
Every page required:
- fetching data, set loading status, set table state, and rendering the table.
- so I decided to extract these common logic into a reusable table component. developers only need to provide an API endpoint, and then the resuable table component would handle everything else.
with this resuable table component, impove the development efficiency and reduce code duplication.
that's how I designed the reusable table component in my admin system.
```
### Lazy loading 怎么做，什么背景
- How do you implement lazy loading and what is the background?
```txt
I think if have a long image list can use the lazy loading.
- I use IntersectionObserver API create an observer to detect when an image enters the viewport.
It can reduce the unnecessary image loading. imporve the page load time.
```
### 17.怎么设置redux
- How do you set up Redux?
```txt
I set up Redux by creating a store using createStore from redux.
Then I define actions and reducers to manage the state.
I use combineReducers from redux to combine multiple reducers.
I wrap the react root component with Provider from react-redux.

In class components, I use connect from react-redux to pass state and dispatch as props.
In function components, I use useSelector and useDispatch from react-redux to access state and dispatch actions.
```
### 18. react和Redux的区别
- What is the difference between React and Redux?
```txt
React is a JavaScript library build UI.
Redux is a global state management library, it helps manage the state in a predictable way. also need to use React-Redux to connect Redux with React.
```
### 19. 有server-side rendering的经验么
- Do you have experience with server-side rendering?
```txt
Yes, I’ve worked with server-side rendering in my first company,
At that time we upgrate official website to version 2.0 from jQuery to Vue.
we use frameworks like Nuxt.js to do SSR
it can build the HTML page on the server side and return to browser.
And the browser to render the page right away.
By doing this, we improve the initial page load speed and get a better SEO.
```
### 水合
- What is hydration?
```txt
with SSR, the server sends a static HTML page to the browser, 
and the browser can render the html right away.
Then, React runs on the client to attach event listeners and make the page interactive
this step is called hydration.
So hydration connects the HTML to JavaScript logic, can enable full React features after the initial load.
```
### 20. 类组件和函数组件的区别
- What is the difference between class components and function components?
```txt
Function components use useState hook to manage state.
Class components use this.state and this.setState to manage state.

Function components use useEffect to handle side effects like data fetching.
Class components use lifecycle methods like componentDidMount, componentDidUpdate, and componentWillUnmount.
```
### 21. 虚拟DOM
- What is virtual DOM?
```txt
1. Virtual DOM is a JavaScript object that represents the real DOM in memory.
it can reduce direct DOM operations and update the real DOM efficiently.
2. When state changes, Virtual DOM compares state with the previous one, this is called diffing.
and only updates the real DOM nodes that changed 
this process is called patching.
```
### 有用过TS么?
- Have you used TypeScript?
```txt
Yes, I have used TypeScript in my daily development.
1. TypeScript provides static type checking, which helps catch errors early in development.
2. It has better IDE support like auto-completion and type checking.
```
### TS不好的地方
- What are the nagatives of TypeScript?
```txt
3. write type may be time-consuming, especially for complex logic.
4. Third-party libraries may not have type definitions, which can lead to type errors, or require developers to write type files by themselves.
```