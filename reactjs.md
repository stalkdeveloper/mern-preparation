# React.js Interview Questions & Answers

---

### 1. What is React.js?
**Answer:** React.js is an open-source JavaScript library developed by Facebook for building user interfaces, especially single-page applications. It enables developers to create reusable UI components and efficiently update the view when data changes.

---

### 2. What is JSX?
**Answer:** JSX (JavaScript XML) is a syntax extension for JavaScript used in React to describe what the UI should look like. JSX allows writing HTML structures in the same file as JavaScript code, making component creation intuitive.

---

### 3. What are components in React?
**Answer:** Components are the building blocks of a React application. They split the UI into independent, reusable pieces. There are two types:
- **Functional components** (stateless, use hooks for state)
- **Class components** (stateful, use lifecycle methods)

---

### 4. What is the Virtual DOM?
**Answer:** The Virtual DOM is a lightweight copy of the real DOM kept in memory by React. When state changes, React updates the Virtual DOM first, then efficiently updates only the changed parts in the real DOM, improving performance.

---

### 5. What are props and state?

**Answer:**
- **Props** are inputs passed from parent to child components, making components reusable and dynamic.
- **State** is data managed within a component that can change over time, triggering re-renders when updated.

---

### 6. What are hooks in React?
**Answer:** Hooks are functions that let you use state and other React features in functional components. Common hooks include `useState`, `useEffect`, `useContext`, and custom hooks.

---

### 7. What is the Context API?
**Answer:** The Context API allows you to share values (like theme, user info) across the component tree without passing props at every level, helping avoid "props drilling".

---

## React.js Interview Questions & Answers (Intermediate)

---

### 1. Explain the React component lifecycle.
**Answer:**  
Class components have lifecycle methods like:
- `componentDidMount`
- `componentDidUpdate`
- `componentWillUnmount`

Functional components use the `useEffect` hook to handle side effects at different stages.

---

### 2. What is props drilling and how do you avoid it?
**Answer:** Props drilling is passing data through many nested components via props, even if only the deepest child needs it. You can avoid it using the **Context API** or state management libraries like **Redux**.

---

### 3. What are React Fragments?
**Answer:** Fragments let you group multiple elements without adding extra nodes to the DOM. You can use:
```jsx
<></> or <React.Fragment>
4. What is useMemo and when should you use it?
Answer: useMemo is a hook that memoizes the result of an expensive calculation, recomputing it only when dependencies change. Use it to optimize performance when passing complex objects or functions as props.

5. What is Redux and how does it work with React?
Answer: Redux is a state management library. It centralizes the app’s state in a store, and components interact with it via actions and reducers. Redux is useful for large applications with complex state needs.

6. What is the difference between controlled and uncontrolled components?
Answer:

Controlled components have their form data managed by React state.

Uncontrolled components manage their own state internally using refs.

7. How does React Router handle navigation in a single-page app?
Answer: React Router enables client-side routing, allowing navigation between views without full page reloads. It updates the URL and renders the corresponding component.

8. What is React Strict Mode?
Answer: React Strict Mode is a tool for highlighting potential problems in an application, such as unsafe lifecycle methods and legacy API usage. It helps write more robust code.

9. What are higher-order components (HOCs)?
Answer: HOCs are functions that take a component and return a new component with enhanced functionality. They are commonly used for code reuse and cross-cutting concerns.

10. What is reconciliation in React?
Answer: Reconciliation is the process React uses to update the DOM efficiently by comparing the new Virtual DOM with the previous one and applying only the necessary changes.

Advanced React.js Learning Questions & Answers
1. What are custom hooks in React?
Answer: Custom hooks are JavaScript functions whose names start with use and can call other hooks. They allow you to extract and reuse stateful logic across multiple components.

2. What is the difference between controlled and uncontrolled components?
Answer:

Controlled: Form data managed by React state.

Uncontrolled: State is managed internally using refs; useful for non-React code or simple scenarios.

3. What is the purpose of the key prop in React lists?
Answer: The key prop uniquely identifies elements in a list, helping React efficiently update and reorder items by tracking changes, insertions, and deletions.

4. What are React Fragments and why are they used?
Answer: React Fragments (<></> or <React.Fragment>) group multiple elements without adding extra nodes to the DOM, keeping it clean and lightweight.

5. What is the difference between the Virtual DOM and the Shadow DOM?
Answer:

Virtual DOM: Used by React for efficient UI updates.

Shadow DOM: A browser feature for encapsulating DOM and styles inside web components.

6. What is the Context API and when should you use it?
Answer: Use the Context API when you need to share global data like user info or theme across many components without prop drilling.

7. What are the main types of hooks in React?
Answer:

Basic hooks: useState, useEffect, useContext

Additional hooks: useReducer, useCallback, useMemo, useRef

Custom hooks: Developer-defined for reusable logic

Advanced React.js Interview Questions & Answers
1. What are the different phases of the React component lifecycle?
Answer:

Mounting: constructor, getDerivedStateFromProps, render, componentDidMount

Updating: getDerivedStateFromProps, shouldComponentUpdate, render, getSnapshotBeforeUpdate, componentDidUpdate

Unmounting: componentWillUnmount

2. How do you optimize performance in a React application?
Answer:

Use React.memo to avoid unnecessary re-renders

Use useMemo and useCallback for memoization

Use React.lazy and Suspense for code splitting

Avoid deeply nested component trees

3. What is the difference between Redux and Context API?
Answer:

Redux: More powerful and scalable with middleware and dev tools.

Context API: Lightweight and easier to use, suited for simpler use cases.

4. What are higher-order components (HOCs) and what are their use cases?
Answer: HOCs are functions that take a component and return a new one with added features. Use cases include authentication, theming, and logic reuse.

5. What does the three dots (...) syntax mean in React?
Answer: It is the spread operator, used to:

Spread props

Copy or merge arrays/objects

6. How do you avoid binding in React class components?
Answer:

Use arrow functions as class properties

Bind methods in the constructor

7. What is React Strict Mode?
Answer: A development tool to detect unsafe lifecycle methods, legacy APIs, and potential problems in components.

8. What are the main components of Redux?
Answer:

Store: Holds the state

Actions: Describe what happened

Reducers: Describe how state changes

9. What is prop drilling and how do you solve it?
Answer: Prop drilling is passing props down through multiple layers. Solve it using the Context API or Redux.

10. What is server-side rendering (SSR) in React and why is it important?
Answer: SSR renders components on the server and sends HTML to the client. It improves:

Performance
SEO
