
### 1. 自我介绍Self Introduction
### 2. 为什么来日本
### 3. Only a chill talk with my friends.
### 4. Tell me more about Your last company and what kind of product and business are they launching. What's your responsibility there?
Fumin Bank provides **financial services** like:
- savings
- loan services
- wealth products
- reward points system
I was in charge of the banking **reward points system**.  
When Users saving their money in bank or buying wealth products,
they could earn points.
and then use those points in a **points mall** (**e-commerce coupons**, **streaming membership**, and **mobile top-ups**).

This system had two parts:
- A mobile web page points mall inside the Fumin Bank app.
Users can check and use their points to get products or services.(**WebView-based page** inside the app)
- An admin management project to ***manage merchants and products things like that.***

**My responsibility:**  
Led the team to **develop the system**, **reviewed code**, and **managed progress and quality**.
I worked closely with the **product** and **backend teams** to confirm requirements
and deliver high-quality features on time.

## 5.后台管理系统的模板 进一步的讨论
This admin system template came from our rewards points system admin management project.
We designed it with a good user experience in mind.
After the product and operations teams used it, they loved it.
So we decided to promote it across the company.

**Features of the admin system template:**
- **Modular**, **component-based**, **reusable**, admin system template ready to use out of the box.
- Includes:
  2. A **layout module** with a **sidebar menu** where developers could pass in their own **routes**
  3. **Reusable business components** like **tables** and **forms**, all following our design standards

---
### 6.系统的构成进一步的回答
Our admin system had three subsystems: user management, points management, and report and order management.
Since some changed frequently and others didn’t, we separated them to avoid side effects.


7. 怎么做系统设计
First, we need have a meeting to clarify and summarize the requirement. make sure we understand the task before we start.
Second, plan the project structure ahead. let the frequently updated business separated from stable business, to avoid unnecessary side effects.
Third, do technical selection, base on the user experience and project requirement. also consider the team members background and the available resources.
and Then set coding standards and plan for the long term, make sure the project easy to maintain.
### 8. How many members in the team?

**Four of us** on the team, including me.  
All of us were **front-end engineers**.

- **40%** time: discussing requirements with **product** and **backend teams**
- **30%**: **code review** and manage progress
- **30%**: building **reusable components** and core features

---

### 5. TypeScript, React, Redux 技术栈

**Yes, that's right. I've used `TypeScript`, `React`, and `Redux` as my main stack.**
Yes, I used React, Redux, and TypeScript in my daily development.

React is for building UI.
**`Redux`** is a global state management library.
we also need React-Redux library that connects Redux to React.

Redux is like an efficient elevator
Redux only updates components that use the changed state.
Compare to React Context can cause the whole component tree to re-render, even if only part changes.
So Redux is better for large apps with frequent state updates.

TypeScript is JavaScript with types.
**TypeScript helps developer catch bugs early and makes the code more predictable.**  
It also gives great **editor support** — like **auto-completion** and **type checking**.  
The downside is that writing **types** can be time-consuming, especially for complex logic or third-party libraries.
If a library doesn’t have built-in types, I have to install @types or write a type file by myself.
---

### 6. Have you had experience about server-side rendering?

**Yes, I’ve worked with server-side rendering using frameworks like `Next.js`.**

- **SSR** builds the HTML page on the server side at request time
- Allows the browser to render the page right away
- We used **SSR** to improve initial page load speed and **SEO**

> **It's all about balance** — choosing the right technology depends on cost and available resources.  
> **I like what Steve Jobs said:** we shouldn’t start from technology and push it into a product.  
> Instead, we should start from the user’s needs and find the right tools to solve the problem.

// hydration
First, with SSR, the server sends a static HTML page to the browser, it can show the content quickly.
Then, React runs on the client to attach event listeners and make the page interactive
— this step is called hydration.
So hydration connects the HTML to JavaScript logic, can enable full React features after the initial load.

---

### 7. Experience about upgrading and enhancing the system performance as a frontend engineer

**I want to talk about it in three parts:**

**First:** Reducing unnecessary requests  
- **Lazy loading images** when they enter the viewport  
- **Merging files** to avoiding mutiple requests.
- Using **browser caching** with proper response headers

**Second:** Reduce resource size  
use webpack or vite to enble compression, 
minify JS and CSS files
and tree-shaking to remove unused code.
compress images size used in the project

**Third:** Improving rendering performance  
- For **React** projects, use **`useMemo`**, **`useCallback`**, and **`shouldComponentUpdate`** to avoid unnecessary re-renders  
- Use **`React.lazy()`** and **`Suspense`** to load components only when needed
- use SSR to improve initial page load speed and SEO
- use virtual scrolling to render only visible items in a long list


## CDN
A CDN is a content delivery network that stores static files like images, scripts, and HTML in servers around the world.
When a user visits the website, the CDN can return the static files from the closest server to reduce load time.
This improves performance.

---

### 8. Single page of React component, fetching API data 200, but UI not changing. What kind of issue do you think of?

- Maybe didn’t store it in **state**
- Maybe not use **`setState`** to update state
- Or the **state** didn’t change, component didn’t **re-render**
---

### 9. 100,000 messages, the scroll speed is very slow, how to optimize it?

Virtual scrolling only renders the items visible in the viewport
When you scroll, it loads more items and removes the ones you don’t see.
This makes the page faster, even with lots of data.
Libraries like **`react-window`** or **`react-virtualized`** can do it.

> **That’s the point of open source** — so we don’t have to repeat and build the wheel.  
> I usually check the **documentation** if it matches our requirement or not, quickly go through the **source code**, and look at how fast **issues** are resolved and how active the **community** is.

---

### 10. Testing you done: unit testing, integration testing, performance testing

- **Unit testing:** Mainly using **`Jest`** to test components and functions
- **Integration testing:** 
Use **`React Testing Library`** To test different parts can work together properly.
For example: to simulate user actions like clicks, trigger API calls, and check if the UI updates properly
- **Performance testing:** Usually use **`Chrome DevTools`** to check load speed and render time，

We’re required to test shared components and utilities, to make sure they’re stable.
For business logic, we also write tests whenever possible, especially for important features.

---

### 11. Principles of code review, what do you pay attention to when you review someone's code?
**When I review code:**
We follow a consistent coding style — everyone needs to follow our coding standards.
We use ESLint and Prettier to enforce and check the code style.
I focus on writing clear, easy-to-read code, with good naming and comments.
I also make sure to split common logic into components or functions to avoid duplication code.
make sure make the project easy to maintain in the long term.
We also pay attention to performance issues and edge cases during reviews.
---

### 13. Microservices for frontend

**Micro frontends** are a way to split a large app into smaller, individually developed and deployed modules.

- In **Webpack**, use **`Module Federation`**
- In **Vite**, use the plugin **`vite-plugin-federation`**

They improve team flexibility and make it easy to scale **frontend development**.  
But there are challenges too — like slow **HMR** during local development, and missing **TypeScript types** for remote modules.

---

### 14. Have you ever designed any component from scratch? How to design it? What kind of things do you need to consider?

**Yes, I’ve designed components from scratch.**

**My process:**
- Notice repeated patterns during development
- Research and think how to extract common logic into reusable components or hooks.
- defined component APIs，like props and events
- Coding tetsing and write documentation

**When designing components, I focus on:**
- **Easy to use** and **flexibile**
- Add **unit tests** to avoid regression
- Always provide **clear documentation**
- Listen to feedback and keep coding.

**For example:**  
I built a **responsive query filter component** — it adjusts the number of columns based on **screen width**.  
In my previous company, this kind of feature was common, but the **user experience** wasn’t great.  
So I took action: notice, think, define APIs and coding.
This helped us unify the **user experience**.