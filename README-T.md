## 技术面试
- 技术相关的面试题
### 1. 你怎么优化前端性能
- what did you implement and how did you improve the performance?
```txt
In my previous company, I foucs on three part to do performance optimization.
I want to talk about this in three parts:
1. reduce unnecessary requests to improve load speed
the most used method is lazy loading,
when have a long image list,
watch the images and only render when image enters the viewport
use React.lazy() and Suspense to do route-based code splitting,
load the component only when the user navigates to that route.
use dynamic import to load components only when needed.
2. reduce resource size to improve load speed
use webpack or vite to enable compression,
minify JS and CSS files
do tree-shaking to remove unused code
3. improve render performance
for React projects,
use useMemo,
useCallback,
shouldComponentUpdate to avoid unnecessary re-renders
if you need render a long list use virtual scrolling.
That's pretty much what I did at previous company.
```

```txt
In my previous company, I use lazy loading to improve the performance.
we build a points mall, it has a long product image list.
At first, if we render all images at once, the load speed was very slow.
Then I use IntersectionObserver API create an observer to watch an image enters the viewport.
When the image enter the viewport, and then load the image.
it can reduce the unnecessary image loading, imporve the page load time.
by doing this, we imporve the user experience a lot.
```

### 2. 怎么测量前端性能
- how do you measure the system performance?
```txt
- I always use Chrome DevTools to check load speed and render time in my previous company.
I always use Performance panel focus on the following metrics:
LCP, CLS, and INP
to check the load speed and user experience.
// LCP shows first screen loading speed, CLS checks layout stable, and INP reflects user interaction speed.
- use Rendering panel to monitor FPS to check rendering performance. frame per second should be 60 FPS.
- use Coverage tab panel check the unused code.
- use network panel to check API requests and responses time.
- use lighthouse to check performance, and SEO.
- use webpack-bundle-analyzer to check bundle size then do some optimization.
- That’s pretty much based on these metrics.
```
### 3. 怎么管理代码质量
- how do you usually manage code quality?
```txt
we do this in three ways:
1. use tools like ESLint and Prettier to make sure everyone follows the same coding standards.
2. write unit tests and integration tests to ensure code run smoothly.
3. by code reviews, we check
performance
edge cases
good naming
clear comments
extract common logic 
make sure the project easy to maintain in the long term.
That's what I usually do.
```
### 4. 你如何进行质量管理
- How do you ensure quality management?
```txt
1.I think first important thing is
to clarify the requirements with stakeholders before starting,
make sure do the right thing.
2. use tools like ESLint and Prettier
to make sure everyone follows the same coding standards.
3. write unit tests and do integration tests,
to ensure code run smoothly.
4. always do code reviews to check the 
performance
edge cases
good naming
clear comments
extract common logic
make sure the project easy to maintain in the long term.
That's what I usually do.
```
### 5. 你如何进行代码审查
- How do you conduct code reviews?
```txt
First, We built a standard code style make sure everyone follows the same coding standards.
I focus on writing clear, easy-to-read code, with good naming and comments.
I also foucs on to extract common logic into components or functions to avoid duplicate code. 
make sure the project easy to maintain in the long term.
and also pay attention to performance and edge cases to ensure the code runs smoothly.
That's how I do code reviews.
```
### 6.从零开始的组件设计经验
- Do you have experience in designing components from scratch?
```txt
- Yes, I'v always built resuable component in my previous company.
- I always design a components in three step.
- one is notice the repeat patterns during development.
- two do some research design a best practices solutions to avoid duplicate code.
- three design the component API make the component configuration-driven.
- then coding and add unit tests.
- In the end always provide clear document.
- When I develop our reward points admin systems, I noticed the table logic was always repeated.
Every page required:
- fetching data, loading, set table state.
- so I extract these common logic into a reusable table component.
developers only need to provide an API endpoint,
and then the resuable table component handle everything.
By doing this, it can improve the development efficiency and reduce duplicate code.
I can summarize this as following steps:
1. notice the repeat patterns during development.
2. do some research and design a best practices solutions to avoid duplicate development.
3. design the component API make the component configuration-driven.
4. then coding and add unit tests.
5. In the end always provide clear document.
that's how I designed the reusable table component in my previous company.
```
### 7. 从零开始的系统设计的经验
第一确定需求，
- Do you have experience in designing a system from scratch?
```txt
Yes, I have experience.
In my previous company, I design the banking rewards points system.
I think the first important thing is talk to stakeholders
to understand the business requirements berfore starting.
make suer we do the right thing and everyone is on the same page.
Then plan the project structure, and seperate the stable 
business and frequently update business, to avoid side effects.
like I sperate admin system to three sub-systems:
- product management
- rewards points management
- order management
Then do the technical selection base on the requirements and user experience.
then design the system architecture, like api design, routs, and codebase.
then set a standard code style in the beginning,
use tools like ESLint and Prettier to ensure code quality.
and add CI/CD to automate the build and deployment process.
```
### 8. 你是怎么设计推进这个项目的
- How did you design and promote this project?
```txt
I can give you an example of how I manage development progress in my previous company.
First, we separate the task into small steps.
and set a priority for each task.
Then I set a timeline for each task based on the priority.
Then we use tools like Jira to track the progress.
Every morning, we have a quick standup meeting
to check the progress and confirm today's plan.
In the end of each day, I report the progress to stakeholders.
make sure everyone is on the same page during the development.
So I think with
planning ahead,
setting priorities,
keep communication,
we can make sure run the project smoothly.
```
### 9. 你们实施过什么测试
- What kind of tests have you implemented?
```txt
- we use Jest to do unit test for components and functions
- we use React Testing Library to do Integration testing make sure different parts can work together.
For example: to simulate user actions like clicks, trigger API calls, and check if the UI updates properly
we do the Performance testing use chrome DevTools to check load speed and render time.
also we use Lighthouse to check performance and SEO.
In my previous company, the QA team had many mobile devices, so we do real device testing to check the browser compatibility.
```

### 10. 过去有没有推荐过技术或者策略
- have you suggested any new technology or strategy in your past experience?
```txt
Yes, In my previous company, I suggested to use Vite instead of Webpack.
Vite can improve development experience a lot.
with the faster hot module replacement HMR,
But I do this gradually,
first I set up a Vite project for a new project,
This project is not emergency, so we can try new technology.
After we completed a full process from development to production,
we confirmed the business run stale
Then we gradually migrate the project to Vite.
I think sometimes we need to balance new technology risk and benefit.
if the benefit is big enough, we can try new technology.
```
### 11. 你是如何发现和定位前端问题的
- For trouble shooting, how do you handle it
```txt
About handle trouble shooting, I want to share my experience in my previous company.
I think the first important thing is confirm and understand the issue before starting.
make sure I understand what happend, and what the expected behavior is.
Then I will reproduce the issue in my local environment.
Then I use chrome dev tools to locate the bug,
check the console panel to console logs
use network panel to check API requests and responses.
sometimes set breakpoints to debug the code.
After I locate the bug,
I will fix the bug and add unit tests cases to make sure code run smoothly.
Then do code reviews with team to check the edge cases make sure code quality.
If everything is ok, then commit the code and deploy test environment to stakeholders confirm.
After the confirm the fix, I will deploy to production.
```

### 14. 你处理问题一般需要多久
- How long does it take to fix a bug?
```txt
It depends on the situation.
If it's a simple bug, I can fix it in a few minutes.
I remember the longest time is 2 hours,
In my previous company
we use a open source UI library ant design mobile,
I need to check the source code and find the issue.
Although it was a big chanllenge But with my effort and patience, I finally fixed it.
```

### 15. 你项目中用过figma么？
- Have you used Figma in your project?
```txt
not really, we didn’t use Figma in my previous company in China, we used Lanhu, it's kind like Figma.
I often used it for checking design and getting CSS values
```
### 16. 你用CSS做什么
- Why do you use CSS?
```txt
I use CSS to add style to HTML elements 
make the page beautiful and have a good user experience.
```
### 17. 在CSS中用过函数么
- Can you use a function for CSS?
```txt
Yes, I can use CSS functions 
like function calc() to calculate values like width and height,
use function var() to define and reuse css variables
```
### 18. 你有监控系统的经验么
- Do you have experience in monitoring systems?
```txt
Yes, I have experience in monitoring systems.
In my previous company, we had an internal monitoring system to check frontend errors.
We tracked JavaScript errors, API request fail errors, and performance everyday.
we always need to use this monitoring system to check the production errors.
```
### 19. 性能调优
- How do you tunning performance?
```txt
In my previous company we have a rewards points admin system,
the ops team needed to download user order data as Excel files.
For 30,000 rows data, it's a long list
Then I use Web Worker to create a separate thread for the export logic.  
I moved the export logic to a Web Worker created thread.
// Inside the worker, I did
// Batch API requests for all pages.  
// Merging all order data.  
// Generate Excel Blob inside the worker.  
After the worker finished, it call back to the main thread, and then triggered the file download.
After doing this, the page run smoothly without blocking
improve the user experience a lot.
```


### 20 Lazy loading 怎么做，什么背景
- How do you implement lazy loading and what is the background?
```txt
I think if have a long image list can use the lazy loading.
- I use IntersectionObserver API create an observer to detect when an image enters the viewport.
It can reduce the unnecessary image loading. improve the page load time.
```
### 虚拟滚动
- What is virtual scrolling and how does it work?
```txt
Virtual scrolling used when you need render a long lists.
it's will be slow if you render all list items at once.
Virtual scrolling only renders the visible items in the viewport.
When you scroll, it loads more new items and removes the previous items
This makes the page faster, even with lots of data.
we also use libraries like react-window or react-virtualized in my previous company
to improve the performance of long lists.
```

### 21.怎么设置redux
- How do you set up Redux?
```txt
I set up Redux by creating a store using createStore from redux.
Then I define actions and reducers to manage the state.
I use combineReducers from redux to combine multiple reducers.
I wrap the react root component with Provider from react-redux.

In class components, I use connect from react-redux to pass state and dispatch as props.
In function components, I use useSelector and useDispatch from react-redux to access state and dispatch actions.
```
### 22. react和Redux的区别
- What is the difference between React and Redux?
```txt
React is a JavaScript library build UI.
Redux is a global state management library, it helps manage the state in a predictable way.
also need to use React-Redux to connect Redux with React.
```
### 23. 有server-side rendering的经验么
- Do you have experience with server-side rendering?
```txt
Yes, I’ve worked with server-side rendering in my first company,
At that time we upgrate official website to version 2.0 from jQuery to Vue.
we use frameworks like Nuxt.js to do SSR
it can build the HTML page on the server side and return to browser.
And the browser to render the page right away.
By doing this, we improve the initial page load speed and get a better SEO.
it's very helpful for the business.
```
### 24 什么时候用客户端渲染，什么时候用服务端渲染
- When do you use client-side rendering and when do you use server-side rendering?
```txt

```
### 25 客户端渲染的缺点
- What are the weakness of client-side rendering?
```txt
CSR is use JavaScript to render the content,
may cause the blank screen before the JavaScript load.
so the initial page load speed can be slow.
may also have a bad SEO
```

### 26 水合
- What is hydration?
```txt
with SSR, the server sends a static HTML page to the browser, 
and the browser can render the html right away.
Then, React runs on the client to attach event listeners and make the page interactive
this step is called hydration.
So hydration connects the HTML to JavaScript logic, can enable full React features after the initial load.
```
### 27. 类组件和函数组件的区别
- What is the difference between class components and function components?
```txt
Function components use useState hook to manage state.
Class components use this.state and this.setState to manage state.

Function components use useEffect to handle side effects like data fetching.
Class components use lifecycle methods like componentDidMount, componentDidUpdate, and componentWillUnmount.
and the fuction doesn't have this, so we can extract many logic into custom hooks. 
```
### 28 Custom hooks 的缺点
- What are the disadvantages of custom hooks?
```txt
- When the logic complex, custom hooks can be hard to read and maintain.
- Also, if dependencies are not handled well, they may cause unnecessary re-renders.
must be careful when using custom hooks.
```

### 29. 虚拟DOM
- What is virtual DOM?
```txt
1. Virtual DOM is a JavaScript object that stands for the real DOM in memory.
I think it has two steps:
2. When state changes, Virtual DOM compares with the previous state, this process called diffing.
and then updates only the real DOM  changed 
this process is called patching.
it can reduce direct DOM operations and update the real DOM efficiently.
```
### 30 有用过TS么?
- Have you used TypeScript?
```txt
Yes, I have used TypeScript in my daily development.
1. TypeScript provides static type checking, which helps catch errors early in development.
2. It has better IDE support like auto-completion and type checking.
```
### 31 TS不好的地方
- What are the nagatives of TypeScript?
```txt
3. write type may be time-consuming, especially for complex logic.
4. Third-party libraries may not have type definitions, which can lead to type errors, or require developers to write type files by themselves.
```