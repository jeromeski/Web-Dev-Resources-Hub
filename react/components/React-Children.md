In React, `Children` is a utility provided by the React library that allows you to work with the children of React components. When you have a component that can have nested elements or components inside it, `Children` provides a way to interact with those nested elements in a more controlled manner.

Here's how you import `Children` from React:

```javascript
import React, { Children } from 'react';
```

And here's an example of how you can use `Children`:

```javascript
import React, { Children } from 'react';

const MyComponent = ({ children }) => {
  // Using React.Children.map to iterate over the children
  const modifiedChildren = Children.map(children, child => {
    // Manipulate each child element, for example, adding a prop
    return React.cloneElement(child, { newProp: 'someValue' });
  });

  return <div>{modifiedChildren}</div>;
};

const App = () => {
  return (
    <MyComponent>
      <ChildComponent />
      <AnotherChildComponent />
    </MyComponent>
  );
};
```

In this example:

- `MyComponent` is a custom React component that accepts `children` as a prop.
- `React.Children.map` is used to iterate over each child element passed to `MyComponent`.
- `React.cloneElement` is used to clone each child element and add a new prop to it.
- Finally, the modified children are rendered inside the `MyComponent`.

This is just one example of how you can use `Children` in React. It's commonly used for scenarios where you need to manipulate or iterate over the children of a component.