# Login and Auth


## Review, Research, and Discussion

**Why is the [Context API](https://reactjs.org/docs/context.html) useful?**

  - provides a way to share values like these between components without having to explicitly pass a prop through every level of the tree.

**Can a component outside of a provider get its context?**

  - if the component is between the opening and closing context tags then it can use the context. Only children of the context tags can use the context.

**What are some common use cases for using the Context API?**

  - Themes
  - Alternate languages
  - Authorization

**Describe “[Context Hell](https://www.polidea.com/blog/react-hooks-vs-wrapper-hell-writing-state-in-a-function-with-ease/)”**

  - When your applications have a massive quantity of nested Components

---
## Vocabulary Terms


- global state - a way to pass props from a parent component to grandchild components without having to pass the props through all child components
- global context - provides a way to share values like these between components without having to explicitly pass a prop through every level of the tree.
- provider - Every Context object comes with a Provider React component that allows consuming components to subscribe to context changes.
- consumer - All consumers that are descendants of a Provider will re-render whenever the Provider’s value prop changes.