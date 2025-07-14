### 1. 介绍自己
#### Introduction 
### 2. 提升性能
#### Performance improvement - what did you implement and how did you improve the performance?
1. reduce unnecessary requests
- use lazy loading when the image enters the viewport
- merging files to avoid the multiple requests
- set proper response headers for browser caching
2. reduce resource size
- use webpack or vite to enable compression, minify JS and CSS files
- tree-shaking to remove unused code
- compress images size used in the project
3. improve rendering performance
- for React projects, use useMemo, useCallback, shouldComponentUpdate to avoid unnecessary re-renders
- use React.lazy() and Suspense and dynamic import to load components only when needed
- use SSR to improve initial page load speed and SEO
- use virtual scrolling to render only visible items in a long list
That's pretty much what I did.
### 4. How do you measure the system performance?
- use lighthouse to check performance, and SEO.
- use Chrome DevTools to check load speed and render time.
- use Performance panel focus on LCP, CLS, and INP to measure page speed and user experience.
- LCP shows first screen loading speed, CLS checks layout stability, and INP reflects UI responsiveness after user actions.
- use Rendering panel to monitor Frame Rate FPS.
- use Coverage tab check the unused code.
- use webpack-bundle-analyzer to reduce bundle size.
- That’s pretty much based on these metrics.
### 5. Lazy roading? - Can you give me an example of when you use?
- use IntersectionObserver API to detect when image enters the viewport,
- then load the image dynamically.
- or use React.lazy() and Suspense to load components only when needed.
- It’s always based on route-based code splitting.
### 6. Why did you implement lazy loading? What was the background?
- Lazy loading helps reduce initial page load time by loading only the necessary resources.
- It improves performance, especially for pages with many images or components or long lists.
### 7. What will be the negative part of using custom hooks?
- When the logic complex, custom hooks can be hard to read and maintain.
- Also, if dependencies are not handled well, they may cause unnecessary re-renders.
### 8. what is custom hooks?
- Custom hooks are reusable functions in React that always start with “use”.
- They are used to share logic between components 
- and help developers avoid  duplicate code.
### 9.How do you usually manage code quality usually?
- I use **ESLint** and **Prettier** to enforce coding standards and style.
- I also write unit tests using **Jest** and **React Testing Library** to ensure code run smoothly.
- never repeat yourself, extract common logic into custom components or functions.
- Code reviews to check performance and edge cases.
### 10. Have you suggested any new technology or strategy in your past experience
- I introduced Vite instead of Webpack to improve development experience.
- It helped the team reduce build time by 50%
### 11. How do you mentor other team members
- I give team members respect by trusting them to take ownership of their work.
- I guide them notice the repeat patterns when they write code, and encourage them thinking
- and then let them to build resuable components or functions.
- I think it's better than just let them following instructions.
### 12. How do you detect a frontend issue?
- I use browser developer tools like the Console to check errors and logs,
- and the Network tab to check API requests and responses.
- I also use debug tools to set breakpoints.
### 13.career plan
- In the short term, my goal is to let myself get used to the international environment and culture,
- In the long term, I want to become a system architect,
- helping the team and company succeed in the global market.
### 14.What was the Feedback you received in the past
- The feedback I most often received was proactive, I like led the team to solve problems.
- I also got positive feedback for helping team members through code reviews.
### 15.Have you thought about what will be challenging working in Japan
- Yes, I’ve thought about it. I think the biggest challenge will be communication,
- Especially using English and Japanese in daily work
- But I’m confident I can overcome it.
### 16.have you ever used figma?
- not really, I didn’t use Figma in my previous company in China, we used Lanhu, it's kind like Figma.
- I often used it for checking layout details, and getting CSS values
- to make sure the front-end page matched the design.
### 17.Why do you use CSS
add style to HTML elements to make the page look good.
create a better user experience,
### 18. Can you use a function for CSS?
### 19. Could you tell me the team structure?
- We had a team of four front-end developers.
- Each person was responsible for a different project, and we worked independently but also shared knowledge when - needed.
### How did you optimize the time
### What was the advantage of finding a code base and functional components
A clear code base makes the project easier to read and maintain.
Using functional components with React Hooks helps us write more reusable code.
### How do you handle the component in your project
- We separate component to common components, business components
- and also use custom hooks for shared logic.
### Where do you use paginations
- I use pagination on pages with large data lists
- to improve performance and user experience.
- the backend provides pagination APIs,
- so we can request data page by page instead of loading everything at once.
### Where do you use suspense?
load components only when needed
route-based code splitting
it helps improve initial page load speed.
### first request
The first request is usually the main HTML document,
like index.html, which contains the basic structure of the page.
After that, 
the browser loads CSS, JavaScript, and API requests based on the content.
### Could you tell me the weakness in client-side rendering
- CSR is use JavaScript to render the content, so the initial page load can be slower
- may also have a bad SEO
### What should be rendered in client side and server side
I use server-side rendering for SEO-friendly and static pages to improve first load speed.
I use client-side rendering for dynamic pages like dashboards that rely on user interactions.
### how do you set redux 
I set up Redux by creating a store using configureStore() from Redux Toolkit,
 and wrapping the app with the <Provider> component.
I organize slices for each feature using createSlice(), which helps manage state, actions, and reducers in a cleaner way.
### What is the trouble handling flow?
My troubleshooting flow is: 
find the issue,
reproduce it locally, 
location the bug in the code,
fix the code, and then deploy the fix.