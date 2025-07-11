## Native Module Federation

### What is Native Module Federation

<b>Native Module Federation</b> is a modern approach to building modular and independently deployable JavaScript applications using native browser features—specifically import maps and ESM (ECMAScript Modules).

It allows JavaScript assets—such as micro frontends or individual app components—to be <b>developed</b>, <b>tested</b>, and <b>deployed</b> independently. These assets are then fetched remotely and integrated at runtime using the browser’s native ESM capabilities, without relying on a bundler like Webpack to stitch them together.

---

### WHY Native Module Federation

The development of this architecture arose from the need to transform deliveries of from a <b>Siloed Workflow</b> to a <b>Value Stream</b>.

#### Silos separate work by department or function (e.g., design, development, QA, operations), often with:
  -  Poor communication across teams
  -  Handoffs and delays between stages
  -  Local optimization over global outcomes
  -  A focus on task completion rather than customer value



| Aspect         | **Value Stream**             | vs | **Siloed Process**                |
| -------------- | ---------------------------- | -- |---------------------------------- |
| Focus          | End-to-end customer value    |    | Departmental tasks or KPIs        |
| Flow           | Continuous, cross-functional |    | Fragmented, with handoffs         |
| Visibility     | Full workflow is transparent |    | Limited to functional areas       |
| Feedback Loops | Fast, integrated             |    | Slow, disconnected                |
| Optimization   | System-level (global)        |    | Local (per team or department)    |
| Deployment     | Small Deployments, less risk |    | Monotlithic Deployment, high risk |         


<b>Native Module Federation focuses on a strategy for decoupling yet maintaining cohesion betweeen each front end application that represents a value stream.</b>

---

### OVERVIEW OF REQUIREMENTS

This section will outline the necessary implementation requirements to build an application using the Native Module Federation approach.


#### ECMAScript Modules

  Javascript assets <b>MUST</b> be ECMAScript Modules

  In Native Module Federation (ESM) refers to both:
  
  - The module system (language feature) defined by the ECMAScript standard
  - The build type or format of the JavaScript file produced by a bundler or build tool
    

#### Import Maps

  [ImportMap Documentation](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/script/type/importmap)

  Import maps are required for Native Module Federation because they provide a way for the browser to resolve bare module specifiers (like 'app1/Button' or 'shared-lib') to actual URLs at runtime — a critical part of how Native Module Federation works.

---

#### APPLICATION ARCHITECTURE


1. <b>Static/Common Web Application</b> (index.html with importmap)</b>

    A static application, which simply includes an index.html with the import map. Generally this web application should not require any build tools or package management. 

    
2. <b>Host Web Application</b>

    A host web application in the context of Micro Frontends (MFEs) is the main shell or container that loads and integrates multiple independently developed     frontend modules (called remote or child applications) into a single user interface. The host application would be the first script that is loaded in index.html.
   

4. <b>Sub Web Application(s)</b>

    A sub web application is any javascript module that can be consumed by the Host Web Application, as well as other Sub Web Application.
   


<!--
### Introduction
Outline and instructions on how to implement native module federation
-->
<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
