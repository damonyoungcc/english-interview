## 第一次模拟面试总结
**日期：2025年7月11号**  
**面试者：anqi 和 shogo**

---

### 1. Self Introduction

---

### 2. Only a chill talk with my friends.

---

### 3. Tell me more about this company, and what kind of product and business are they launching. What's your responsibility there?

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
- A web page points mall inside the Fumin Bank app.
Users can check and use their points to get products or services.(**WebView-based page** inside the app)
- An admin management project to ***manage merchants and products things like that.***

**My responsibility:**  
Led the team to **develop the system**, **reviewed code**, and **managed progress and quality**.
I worked closely with the **product** and **backend teams** to confirm requirements
and deliver high-quality features on time.

## 进一步的讨论
This admin system template came from our rewards system admin management project.
We designed it with a good user experience in mind.
After the product and operations teams used it, they loved it.
So we decided to promote it across the company.

**Features of the admin system template:**
- **Modular**, **component-based**, **reusable**, admin system template ready to use out of the box.
- Includes:
  2. A **layout module** with a **sidebar menu** where developers could pass in their own **routes**
  3. **Reusable business components** like **tables** and **forms**, all following our design standards

---
### 3.1
Our admin system had three subsystems: user management, points management, and report and order management.
Since some changed frequently and others didn’t, we separated them to avoid side effects.


### 4. How many members in the team?

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

Redux is like an efficient elevator — it reads and updates state only where it’s needed.
Compare to React Context can cause the whole component tree to re-render, even if only one part needs the change.

TypeScript is JavaScript with types.
It helps catch errors early and makes code easier to read and maintain.

- We use **`React`** to build the UI
- **`TypeScript`** helps keep the code clean and predictable
- **`Redux`** to manage global state  


---

### 6. Have you had experience about server-side rendering?

**Yes, I’ve worked with server-side rendering using frameworks like `Next.js`.**

- **SSR** builds the HTML page on the server side at request time
- Allows the browser to render the page right away
- We used **SSR** to improve initial page load speed and **SEO**

> **It's all about balance** — choosing the right technology depends on cost and available resources.  
> **I like what Steve Jobs said:** we shouldn’t start from technology and push it into a product.  
> Instead, we should start from the user’s needs and find the right tools to solve the problem.

---

### 7. Experience about upgrading and enhancing the system performance as a frontend engineer

**I want to talk about it in three parts:**

**First:** Reducing unnecessary requests  
- **Lazy loading images** when they enter the viewport  
- **Merging files** or avoiding duplicate code (**Don't repeat yourself**)  
- Using **browser caching** with proper response headers

**Second:** Reduce resource size  
- **Minify JS and CSS files**
- Enable **gzip**  
- **Compress images**

**Third:** Improving rendering performance  
- For **React** projects, use **`useMemo`**, **`useCallback`**, and **`shouldComponentUpdate`** to avoid unnecessary re-renders  
- Use **`React.lazy()`** and **`Suspense`** to load components only when needed

---

### 8. Single page of React component, fetching API data 200, but UI not changing. What kind of issue do you think of?

- Maybe didn’t store it in **state**
- Maybe not use **`setState`** to update state
- Or the **state** didn’t change, component didn’t **re-render**
---

### 9. 100,000 messages, the scroll speed is very slow, how to optimize it?

I would use virtual scrolling to only render visible items
it calculate which items are in view, and update the DOM based on scroll position
Rendering all items at once is too heavy for the **DOM**.
Libraries like **`react-window`** or **`react-virtualized`** can do it.

> **That’s the point of open source** — so we don’t have to repeat and build the wheel.  
> I usually check the **documentation** if it matches our requirement or not, quickly go through the **source code**, and look at how fast **issues** are resolved and how active the **community** is.

---

### 10. Testing you done: unit testing, integration testing, performance testing

- **Unit testing:** Mainly using **`Jest`** to test components and functions
- **Integration testing:** 
Use **`React Testing Library`** To test how different parts of the app work together
to simulate user actions like clicks, trigger API calls, and check if the UI updates properly
- **Performance testing:** Usually use **`Chrome DevTools`** to check load speed and render time

We’re required to test shared components and utilities, to make sure they’re stable.
For business logic, we also write tests whenever possible, especially for important features.

---

### 11. Principles of code review, what do you pay attention to when you review someone's code?
**When I review code:**
We follow a consistent coding style — everyone needs to follow our coding standards.
We check for readability and reusability, and avoid duplicated code.
The goal is to build long-term, maintainable solutions.
We also pay attention to performance issues and edge cases during reviews.
---

### 12. TypeScript: How does TypeScript help you in your work?

**TypeScript helps me catch errors early and makes the code more predictable.**  
It improves **collaboration** and also gives great **editor support** — like **auto-completion** and **type hints**.  
The downside is that writing **types** can be time-consuming, especially for complex logic or third-party libraries.

> If a third-party library doesn’t have built-in **types**, I usually install the **`@types`** package or write a simple **type file** myself to get proper **TypeScript support**.

---

### 13. Microservices for frontend

**Micro frontends** are a way to split a large app into smaller, independently developed and deployed modules.

- In **Webpack**, use **`Module Federation`**
- In **Vite**, use the plugin **`vite-plugin-federation`**

They improve team flexibility and make it easy to scale **frontend development**.  
But there are challenges too — like slow **HMR** during local development, and missing **TypeScript types** for remote modules.

---

### 14. Have you ever designed any component from scratch? How to design it? What kind of things do you need to consider?

**Yes, I’ve designed components from scratch.**

**My process:**
- Notice repeated patterns during development
- Research and think
- Coding

**When designing components, I focus on:**
- **Easy to use** and **flexibility**
- Add **unit tests** to avoid regression
- Always provide **clear documentation**

**For example:**  
I built a **responsive query filter component** — it adjusts the number of columns based on **screen width**.  
In my previous company, this kind of feature was common, but the **user experience** wasn’t great.  
So I took action: notice, think, and code.  
This helped us unify the **user experience**.