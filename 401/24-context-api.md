# Context API

## Review, Research, and Discussion

1. **Describe use cases for useMemo() and useReducer()**

    - **useMemo** will only recompute the memoized value when one of the dependencies has changed. This optimization helps to avoid expensive calculations on every render. performance optimization, not as a semantic guarantee

    - **useReducer()** An alternative to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one

2. **Why do custom hooks need the use prefix?**

    - Its name should always start with use so that you can tell at a glance that the rules of Hooks apply to it.

3. **What do custom hooks usually do?**

    - modularize code. hide complex logic.

4. **Using any list of custom hooks, research and name one that you think will be useful in your applications**

    - uesEffect() it can be used 

5. **Describe how a hook that fetches API data might work**

    - gives it a one-liner ability, more declarative code style, reusable logic, and overall cleaner code

---

## Vocabulary

- **reducer** - a function that determines changes to an application's state. It uses the action it receives to determine this change