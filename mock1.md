## 第一次模拟面试总结
**日期：2025年7月11号**  
**面试者：anqi 和 shogo**

---

### 1. Self Introduction

---

### 2. Only a chill talk with my friends.

---

### 3. Tell me more about this company, and what kind of product and business are they launching. What's your responsibility there?

**Fumin Bank** provides financial services like:
- savings
- wealth products
- loan services
- **reward points system**

**My responsibility:**  
I was in charge of the banking **reward points system**.  
Users could earn points by saving money or buying wealth products, and then use those points in a **points mall** (**e-commerce coupons**, **streaming memberships**, and **mobile top-ups**).

**This project had two parts:**
- A **mobile web page** in the Fumin Bank app for users to check and use their points (**WebView-based page** inside the app)
- An **admin system** to manage merchants and products

I also built an **admin system template** based on our work, which improved the user experience across different teams in the company.

**Features of the admin system template:**
- **Modular**, **component-based**, **reusable**, ready to use out of the box
- Includes:
  1. A ready-to-use **login page** with **permission control**
  2. A **layout module** with a **sidebar menu** where developers could pass in their own **routes**
  3. **Reusable business components** like **tables** and **forms**, all following our design standards

**My responsibility:**  
Led the team to develop the system, **reviewed code**, and managed progress and quality.  
Worked closely with the **product** and **backend teams** to confirm requirements and deliver high-quality features on time.

---

### 4. How many members in the team?

**Four of us** on the team, including me.  
All of us were **front-end engineers**.

- **40%** time: discussing requirements with **product** and **backend teams**
- **30%**: **code review** and manage progress
- **30%**: building **reusable components** and core features

---

### 5. TypeScript, React, Redux 技术栈

**Yes, that's right. I've used `TypeScript`, `React`, and `Redux` as my main stack.**

- We use **`React`** to build the UI
- **`TypeScript`** helps keep the code clean and predictable
- **`Redux`** to manage global state  
  > **`Redux`** is a global state management library.  
  > It's like an efficient elevator — any component can access or update state exactly where it's needed.  
  > Compared to **`React Context`**, **`Redux`** avoids unnecessary re-renders.

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
- Enable **gzip**  
- **Minify JS and CSS files**  
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

**I would use virtual scrolling to only render visible items.**  
Rendering all items at once is too heavy for the **DOM**.  
Libraries like **`react-window`** or **`react-virtualized`** help render large lists efficiently.

> **That’s the point of open source** — so we don’t have to repeat and build the wheel.  
> I usually check the **documentation** if it matches our requirement or not, quickly go through the **source code**, and look at how fast **issues** are resolved and how active the **community** is.

---

### 10. Testing you done: unit testing, integration testing, performance testing

- **Unit testing:** Mainly using **`Jest`** to test components and functions
- **Integration testing:** Use **`React Testing Library`** to simulate user actions like clicks, trigger API calls, and check if the UI updates properly
- **Performance testing:** Usually use **`Chrome DevTools`** to check load speed and render time

---

### 11. Principles of code review, what do you pay attention to when you review someone's code?

**When I review code:**
1. Focus on **readability** and consistency with our **coding style** (**Everyone must follow our coding standards**)
2. Check for **performance issues**, **edge cases**, and whether the logic is easy to understand and maintain (**We should build a long-term solution**)
3. Always suggest **reusing shared logic** instead of duplicating code

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