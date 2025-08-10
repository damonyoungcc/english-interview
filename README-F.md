## Introduction & Motivation

### Introduction
currently, base tokyo, study school, 7years, build use, expecially .

### Why are you looking for a job now?
planning apply job, many friends, speak highly
I admire culture, use rakuten pay, deep connection to daily life, have a global impact
skill and experience great match
I enjoy working background, one years japanese course finish, move on,
After one year living in Japan, I really like here, and I want work and live here.
that's why I am looking for a job now.

### When you join the company, what kind of environment and requirement are you looking for?
corporation, open environment, work close teammates, share technology knowledge, support each other.
take challenge and learn new things,grow skills, build tools and components, and solve problems.

### What do you expect from the new work environment?
expect corporation, open environment, work close teammates, share technology knowledge, support each other.
take challenge and learn new things,grow skills, build tools and components, and solve problems.

### What is your mid/long-term career goal?


## Current Role & Teamwork

### What is your current role and responsibilities?
### What kind of front end task are you handling?
clarify and summarize requirements
talk with stakeholders set priorities, manage progress and timelines
front-end architecture, build reusable components
develop features, write code, test and debug
review code, ensure code quality and project maintain in long term
work with my team and support them and motivate them

### What % of your time do you spend for Front-end?
### How are you guys working as a team?
I think the most important thing is keep communicating, 
every morning we had a quick stand up meeting check the progress and confirm today's plan.
I always encourage them to notice the repeat pattern during development, and do some research find out best practice, Then we had a open discussion to do technical share and review.
By doing this, I think everyone will improve their skills and confidence. It’s important that they feel a value in their work. we support each other， and work closely with each other.

### How do you guys testing new features?
unit test, integration test, jest, React Testing Library
CI pipeline, make sure code validate before merge
also we have a QA team use tools like Cypress to do end-to-end testing.
use devtools check the performance,
real device testing, browser compatibility

### Who deploys the system?
We have a DevOps team responsible for deploying the project.
First, we submit a request in our Jira system, we provide the requirement details, deployment plan, and rollback solution.
After stakeholder testing and confirm in a staging environment, the DevOps team handles the deployment, which is executed through GitLab CI/CD pipelines. and then deploy automatically

### How are you guys doing code review?

### How do you keep the quality good?
use tools like eslint and prettier or husky pre-commit hooks to enforce code style and quality
write test cases, unit test, integration test， end-to-end test and we also do a real device testing
code review check the code quality and best practices

## Skills & Technical Experience

### Do you have any experiences with Typescript?
yes, I have a lot of experience with TypeScript, I have been working with TypeScript and build a lot of production projects.
At my previous company,  I use Typescript in React projects to improve type safety, reduce runtime errors, and ensure the project easy to maintain in a long term.
When I build resuable component, I use TypeScript features like generics, utility types like Pick and Partial Omit to create reusable components and APIs.
Overall, TypeScript has helped me catch bugs earlier, improve code quality, and collaborate better with my team.

### type and interface differences
In TypeScript, both types and interfaces can be used to define the shape of an object, but the type is more flexible can define the unions and intersections. 
Interfaces are generally preferred for defining object shapes

###  unknown vs any difference
any can be used for anything, unsafe.
unknown requires type checking before use, more safer.

### Generics
Generics make types as parameters for reusability and make it not lose type information.
For example, I wrote a generic function to remove duplicates from arrays,
but you can early know the type of the elements in the array,
and it works for numbers, strings, or even custom objects without losing type information.

### utility
Partial<T>: make all properties optional
Pick<T,K>: keep only some properties
Omit<T,K>: remove some properties

### Which version of VueJS are you using?
In the beginning of my carrer, I used vue2 to build the ZBJ network official website. At that time we migrated the stack from jQuery to Vue2, and use framework Nuxt.js to improve the initial page load performance and SEO.

At my previous company, we have many projects collaborate with other companies, and we used Vue 3 for those.
Vue 3 has better performance, a smaller bundle size, and introduces the Composition API, which allows us to write many reusable functions to organize logic better. It also has better TypeScript support compared to Vue 2.

### VueJS VS React differences
1. Vue uses a template-based syntax, while React uses JSX
2. React has a one-way data flow, and Vue supports both one-way and two-way binding
3. The biggest difference is that Vue automatically tracks dependencies through its reactivity system, so developers don’t need to manually specify them. In React, you have to declare dependencies, like in the dependency array of useEffect. 
This makes Vue less of a mental burden for developers.


### Do you know what is Vite?
yes, I have a lot of experience with Vite. and I really like it.
it's build by Evan You, after he release Vue3.
Vite is a modern frontend build tool.
not like Webpack bundle everything at first, it uses native ES modules to load files on needed.
During the development, it only compiles affected modules for fast HMR.
use Rollup to build production bundles, which is very fast and efficient.
and also have a powerful plugin system.
In our single page application, I used Vite virtual modules to build a vite plugin, it can automatically generated route path from the folder structure. it's like Nuxt file-system routing.
it's very easy to define the router configuration, and improve the development efficiency.

### What kind of architecture do you have experience?
About the front-end architecture
In tools side, I have experience with Vite, Webpack, and Rollup.


Number 1 about front-end style side, I use CSS variables to support theming, and sometimes CSS-in-JS for components with dynamic styles. I also use PostCSS plugins like Autoprefixer add vendor prefixes to CSS to handle browser compatibility.

Number 2, design a proper routing, I use Vite’s virtual modules to build a plugin to support file-based routing. It automatically generates route paths from the file system, similar to how Nuxt.js file system routing.

Number 3, I also focus on component reusability. During development, I try to notice repeating patterns and extract the common logic into reusable components.

Number 4, I set up tools like ESLint, Prettier to enforce code style, and Husky to run pre-commit and build CI pipelines to validate code quality before merging.

Number 5, I also use state management libraries like Pinia or Vuex to do global state management.

Number 6, I set up tools like ESLint, Prettier to enforce code style, and Husky to run pre-commit and build CI pipelines to validate code quality before merging.

### Do you have any experience with cookies?
we don't use cookies to persist data, it's not a good solution, actually, it's a bad solution, we use cookies maintain the user's login state, when a user logs in, the server verifies the user and creates a session id. 
then server use Set-Cookie header to contains the session ID,  and send back this cookie to browser,
then the browser will carry the cookie in each request automatically. so the server can identify the user by the cookie.

### Which storage have you ever used?
In front-end, we use LocalStorage and SessionStorage to persist data in the browser.
LocalStorage can persist data even after the browser is closed,
while SessionStorage only lasts for the current browser tab session and
it will be cleared when the tab is closed.

sessionStorage is useful for temporary data and LocalStorage maybe used for theme settings record user preferences.
I think sometimes if need to persist objects shape data, always use JSON.stringify before set, and use JSON.parse after get. so create a function extract the logic can help check the edge cases and avoid errors.

### Are you familiar with module federation?
Yes, I’m familiar with Module Federation.
 It’s a Webpack 5 feature that allows different applications to share code and load modules from each other at runtime, 
With you don't needing to rebuild everything together.
 It’s often used in micro‑frontend architectures,
increases build and deployment complexity, since different apps may use different versions of package.json
debugging and testing become harder，and when use Typescript, the load module my don't have a type file, so it's need to difine it another time.

### Difference between synchronous and asynchronous function in JavaScript. Can you provide some examples of when we will use one over another?
synchronous functions block the following code or other task until the function finish,
asynchronous functions allow the following code or task to continue execute without waiting for the function to finish.
We use asynchronous functions like fetching data, reading files, or waiting for timers.
For example, when we fetch data from an API, use asynchronous functions to avoid blocking the UI 
and allow the user to another interaction and wait for the data to be returned.

### Can you provide examples of when you use web accessibility and why it is important?
yes, I have experience with web accessibility. it can help ensure that all users, including disabilities, can access and use the web page and have a good user experience. it's human rights to use the open web.

We had a wheel picker component, sometimes it has a lot of items we used aria-hidden and aria-label on each list item.
Only the currently selected item it can is read by screen readers, while the others are hidden.
We also provided aria-label hints for the first and last items — for example, add additional text like “No previous item” or “No next item” to guide screen reader users clearly.

### How would you evaluate a new package into your project?
First, I would check the package's popularity and  GitHub activity, and issues resolved time.

Then I would check the package's documentation, make sure it can resolve my problem and easy to use.

Then I would read the source code of the package see if it has good code quality, and check if it has good test coverage.

Finally, I would try to use the package in a small demo to see if it works as expected and fit my project needs.

### How would you define unit testing? Have you done any other test than unit testing?
About design the unit test, First is spearation of concerns, and make sure the component or function has a single responsibility.
By doing this, it is easy to test and maintain.
And I also use the integration test to test the interaction between components, ensuring they work together and run smoothly.
I have contributed to the open-source project ant design mobile, I improved the unit test coverage from 20% to 90%,
and always check the test coverage and focus on the highlighted lines that your test cases are not covering.
and add test cases to cover the highlighted lines.

### Have you ever had any issues implementing SSR?（DDD）
Yes, I think the most issue is the browser-only APIs like window or document, may caused errors during server-side rendering
To fix this, I used it in the client side or moved the logic into onMounted.

Another challenge was hydration mismatch, especially when using random IDs or timestamps, so avoid using them during initial render.

Or some third-party libraries not designed for SSR, May cause issues.

## Design & Strategy

### What kind of design pattern and strategy are you following?
In the browser compatibility, we follow the progressive enhancement strategy and graceful degradation strategy.
we analyze the browser used by our customers, and for the modern browsers, we use provide a full support and use the modern features.
for the older devices, we use graceful degradation strategy, we provide a basic fallback solution.

For the reusable components, we follow the high cohesion and low coupling principle. make sure the component and function have a single responsibility. by doing this, it easy to resue and test. also can maintain the project in the long term.

For business logic, we follow the separation concerns principle. we separate the frquently changing business and the stable business logic. so it avoid the side effects when we change the business logic.

### Could you explain about the design of your project working at the previous company?

### What you need to consider when you design e-commerce service.

## Problem-Solving & Challenges

### What kind of challenges did you face during the project?
browser compatibility

### What kind of interesting problem/solution do you have experience?
migration strategy, gradual migration

### What was your biggest achievement so far?

### What was most challenging?

### Can you give a specific example of when you faced a challenging situation? What was the reason? What did you determine your solution could fix the problem?


### Describe a time your team completed a task on a tight schedule. How did you manage your time and what did you sacrifice to make it on time?
At my previous company, we had a tight deadline to deliver a new feature, we only have two weeks to add a coupon feature to our rewards point system.
First thing I do is to clarify the requirements with the stakeholders before starting the development,
make sure we do the right thing in the beginning.because we don't have much time to waste.

Then we break down the feature into smaller tasks, set priorities, and focus on the most important and emergency tasks first.
Every morning, we have a quick standup meeting to check the progress, and make sure everyone is on the same page.

And about sacrifice we just focused on the core functionality. Only supported the most common coupon type, use a basic UI, and in the admin system we just added basic management functions.

so By planning ahead, set priorities, focusing on the most important features, and keeping communication open, we were able to deliver the coupon feature on time.

### Specific examples of innovative things you have done? And what kind of problems have you solved?
web-worker

### Example of when you took a lead, but you took responsibility although it was not your responsibility?
we had a shared upload image component,

### Can you describe if there was a team member that is not aligning but working on same project.How did you solve the issue? 

### Could you give specific example when you and your team solved a complex problem in innovative or simple way.

### How was the volume of the migration system? And how did you approach?
we follow a gruadual migration strategy.
## Leadership & Soft Skills

### Do you have any experience of leading a team of engineers?

### What did you learn from team leading experience and what would you do differently?
About leadership, I think communication is the first important thing.
have a open discussion, ask for feedback, and trust them and respect them.
I always like to encourage them by taking ownership of their work, and give them the freedom to explore solutions.
then we have a open discussion to share ideas review the solutions together.
I think it's better than just let them follow the instructions.
let them feel value and confident in their work is very important.

### If you join our team, what can you contribute to our team?
deliver high-quality features, build reusable components, strong problem-solving skills.
I always like to build some tools to improve the development process and efficiency.
I focus on code quality and I can make sure the project maintainable in the long term.
I have strong experience in frontend architecture, I can help design a proper architecture for the project.

### Are you open to legacy system?
Yes, I’m open to working with old systems. I think it's a good chance to understand the business logic, and I also like to help refactor the system gradually when it possible.
I want share my experience at my previous company, In one of my previous projects, we were using a legacy UED architecture where the dev server was very slow — it took over two minutes to start and didn’t support hot module replacement.


## Career & Learning

### What kind of skills do you want to focus on as a software engineer? Please elaborate.

I like to focus on frontend architecture.
because I really like build tools to improve the develop process or efficiency. and it can grow my skills and let me leave my comfort zone.
For example, I used Vite virtual modules to build a vite plugin, it can automatically generated route path from the folder structure. it's like Nuxt file-system routing.
notice thinking pratice and share,These kinds of projects are what I really enjoy doing.

### How do you catch up with new technologies?
I always catch up with new technologies by github trending, social media to follow the software engineering and technology websites.
Then I always like to build some side projects or tools to practice new technologies. 

Recently, I built a side project website to help me learn Japanese, I use the openAI open source project Whisper to read a audio file and generate the text

Sometimes I also like to explore how to use it to resolve some problems about my current work. Like I just said, I  use vite to improve our development experience.

### If you join our team what is your mid-term, long term career goals?
In the mid term, First, I want to understand the business, work closely with the team to deliver high-quality features. I also like to notice the problems during development, and do some research build some tools or components to improve the development process.

In the long term, I want to grow into a system architect role. I’m interested in expanding my skills beyond front-end, including backend, DevOps, and system design, so I can better understand and build systems end to end.

## Miscellaneous

### Can you explain what is jsx and when is appropriate to use?
JSX is a extension for JavaScript that lets you write HTML-like code in your JavaScript.
It’s common in React, but Vue also supports JSX.

### When do you use snack in vue.js and when it is not appropriate to use?
snack is a component that provides a way to display brief messages or notifications to users, typically used for feedback on user actions like form submit success or error messages. 
Negative snack is used to display messages need user to confirm or take action, should use confirm dialog instead.


### vue中计算属性和方法的区别
- vue difference between computed properties and methods

