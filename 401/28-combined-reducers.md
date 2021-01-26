# Redux - Combined Reducers

## Review, Research, and Discussion

Why choose Redux instead of the Context API for global state?

    because we are learning redux and don't have much time to look at other options

What is the purpose of a reducer?

    determines changes to state

What does an action contain?

    a type and payload that calls a case to return specified data

Why do we need to copy the state in a reducer?

    to export it everywhwere using the use case

## Vocabulary 

**immutable state** - state that cannot be changed

**[time travel in redux](https://medium.com/the-web-tub/time-travel-in-react-redux-apps-using-the-redux-devtools-5e94eba5e7c0)** - The Redux DevTools records dispatched actions and the state of the Redux store at every point in time. This makes it possible to inspect the state and travel back in time to a previous application state without reloading the page or restarting the app

**action creator** - creates action to determine which use case to implement to return state based on use case

**reducer** - determines changes to state

**[dispatch](https://react-redux.js.org/using-react-redux/connect-mapdispatch)** - is a function of the Redux store. You call store.dispatch to dispatch an action. This is the only way to trigger a state change
