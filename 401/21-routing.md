# Routing

## Review, Research, and Discussion

1. **Do child components have direct access to props/state from the parent?**

Not direct, but indirectly if functions are passed. Reading something about hooks, but didn't get too into that as we were told we'll be learning about that next week and I'm confused enough as is with what we have.

2. **When a component “wraps” another component, how does the child component’s output get rendered?**

        <Main>
          <Content />
        </Main>

It is rendered inside of the parent components render. When the parent is rendered, it calls the child component and the child components render is used at that time.

3. **Can a component, such as < Content />, which is a child also be used as a standalone component elsewhere in the application?**

I believe so, if they are declared. Not sure if they take the parent props or if they can only take their own.

4. **What trick can a parent use to share all props with its children**

With a spread operator -allows an iterable such as an array expression or string to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected

## **Vocabulary**

- props.children - can be used to display whatever you include between the opening and closing tags when invoking a component.

- composition - the arrangement of components to create something bigger. (building blocks)