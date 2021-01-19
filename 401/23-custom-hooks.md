# Custom Hooks

## Review, Research, and Discussion

1. What does a component’s lifecycle refer to?

    - From componentDidMount() to componentWillUnmount

2. Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect

    - when passing callbacks to optimized child components that rely on reference equality to prevent unnecessary renders

3. Why are functional components preferred over class components?

    - component doesn’t have its own state and has access to lifecycle hook

4. What is wrong with the following code?

    - supposed to be const arrow functions
    - there is a floating for loop


```
import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);


  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
```

## Vocabulary Terms

[state hook](https://reactjs.org/docs/hooks-state.html) - a Hook that lets you add React state to function components

[effect hook](https://reactjs.org/docs/hooks-effect.html) - using this Hook, you tell React that your component needs to do something after render. React will remember the function you passed, and call it later after performing the DOM updates.

reducer hook - Accepts a reducer of type (state, action) => newState, and returns the current state paired with a dispatch method.