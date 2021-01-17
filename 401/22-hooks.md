# Hooks API

## Review, Research, and Discussion

1. Why do we not need more .html pages in a multi-page React app?

    - The pages are created by components that can be assigned routes in JSX format

2. If we wanted a component to show up on every page,  where would we put it and why?

    - Inside the < BrowserRouter />, outside a < Route /> <---I think this one, but not 100

3. What does props.children contain? 

      - whatever you include between the opening and closing tags when invoking a component.

## Vocabulary

- Composition - the arrangement of components to create something bigger. (building blocks)

- Children / Child Components - Children allow you to pass components as data to other components, just like any other prop you use.

- [Hash Routing](https://reactrouter.com/web/api/HashRouter) - A < Router > that uses the hash portion of the URL to keep your UI in sync with the URL

- [Link Routing](https://reactrouter.com/web/api/Link) - Provides declarative, accessible navigation around your application.