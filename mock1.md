## 第一次模拟面试的总结
### 2025年7月11号

面试者: anqi 和 shogo

1. slef introduction

3. only a chill talk with my friends.

2. tell me more about this company, and what kind of product and business are they launching. what's your responsibility in there.

Fumin bank provided financial services like 
savings, wealth products,
loan services,
and reward points system.

I was in charge of the banking reward points system.
Users could earn points by saving money or buying wealth products,
and then use those points in a points mall.      // e-commerce coupons, streaming memberships, and mobile top-ups.
This project had two parts:
a mobile web page in the Fumin Bank app for users to check and use their points,   // WebView-based page inside the app
and a admin system to manage merchants and products.  
I also built a admin system template based on our work,
which improved the user experience across different teams in the company.

 it's a modular,component-based resuable admin system template
 it can ready to use out of the box,
 it includes:
// 1.a ready-to-use login page with permission control
// 2.a layout module with a sidebar menu where developers could pass in their own routes
// 3.reusable business components like tables and forms, all following our design standards

My responsibily was led the team to develop the system, reviewed code, and managed progress and quality.
I worked closely with the product and backend teams to confirm requirements
and deliver high-quality features on time.

3. how many members in the team
four of us on the team, including me.
All of us were front-end engineers.

Around 40% time was discussing requirements with product and backend teams.
About 30% was for code review and manage progress.
Around 30%, was focused on building reusable components and core features.

4. TypeScript, React, Redux 技术栈
Yes, that's right. I've used TypeScript, React, and Redux as my main stack.

We use React to build the UI
we TypeScript helps keep the code clean and predictable.
and Redux to magane a global state.
// If you aren't sure if you need it, you don't need it.
Redux is a global state management library.
It's like an efficient elevator — any component can access or update state exactly where it's needed.
Compared to React Context, Redux avoids unnecessary re-renders.

5. have you have experience about serverside rendering
Yes, I’ve worked with server-side rendering using frameworks like Next.js.
SSR builds the HTML page on the server side at request time.
allows the browser to render the page right away
We used SSR to improve initial page load speed and SEO.

// I think it's all about balance — choosing the right technology depends on cost and available resources.
// I like what Steve Jobs said: we shouldn’t start from technology and push it into a product.
// Instead, we should start from the user’s needs and find the right tools to solve the problem.

6. experience about upgrading and enhancng the system performance as a fronttend engineer before.
I want to talk about in three parts.
First, reducing unnecessary requests — 
lazy loading images when they enter the viewport
merging files or avoiding duplicate code never repeat youself,
using browser caching with proper response headers
Second, reduce resource size — enable gzip, minify JS and CSS files, and compressing images.
Third, improving rendering performance — 
For React project,use useMemo, useCallback, and shouldComponentUpdate to avoid unnecessary re-renders.
use React.lazy() and Suspense to load components only when needed.
That's what I had done in my previous company.

7. single page of react component, featching and api data 200,but ui not changing, what kind of issue you think of.
maybe didn’t store it in state.
Maybe not use setState to update state.
or the state didn’t change component didn’t re-render .

8. 100000 message, the scroll speed is very slow, how to optimize it.
I would use virtual scrolling to only render visible items.
Rendering all items at once is too heavy for the DOM.
Libraries like react-window or react-virtualized help render large lists efficiently.

// That’s the point of open source — so we don’t have to repeat and build the wheel.
// I usually check the documentation if match our requirment or not,
quickly go through the source code,
and look at how fast issues are resolved
and how active the community is.

9. testing you done, unit testing, integration testing, performance testing

About unit testing, I mainly using Jest to test components and functions.

Integration testing checks if different parts of the system work correctly together.
I use React Testing Library to simulate user actions like clicks, trigger API calls, and check if the UI updates properly.
For performance testing, I usually use Chrome DevTools to check load speed, and render time.

10. principles of coding review, where you pay attention to when you review someone's code.
When I review code,
First, I focus on readability and consistency with our coding style, Everyone must follow our coding standards.
Second, I check for performance issues, edge cases, and whether the logic is easy to understand and maintain.
we should build a long term solution.
Third, I always suggest reusing shared logic instead of duplicating code.

11. typescript ,how typescript help you date to their work,
TypeScript helps me catch errors early and makes the code more predictable.
It improves collaboration and also gives great editor support — like auto-completion and type hints.
The downside is that writing types can be time-consuming, especially for complex logic or third-party libraries.

// If a third-party library doesn’t have built-in types, I usually install the @types package or write a simple type file myself to get proper TypeScript support.

12. microservices for frontend.
Micro frontends are a way to split a large app into smaller, independently developed and deployed modules.
in Webpack use Module Federation, In Vite, use the plugin vite-plugin-federation
They improve team flexibility and easy to scale frontend development.
But there are challenges too — 
like slow HMR during local development,
and missing TypeScript types for remote modules.

13. have you ever design any component from scratch, how to design it, what kind of things you need to consider.
Yes, I’ve designed components from scratch.
My process is usually: notice repeated patterns when development, then research and thinking, then coding.
When designing components, I focus on easy to use and flexibility.
add unit tests to avoid regression 
always provide clear documentation.

For example, I built a responsive query filter component
it adjusts the number of columns based on screen width.
In my previous company, this kind of feature was common, but the user experience wasn’t great.
so I take action, notice, thinking and coding.
This helped us unify the user experience.