# react-tac-toe

My _code-along_ of the official [React Tutorial](https://reactjs.org/tutorial/tutorial.html).

## Notes

- We pass data to Components through `props`

```jsx
<MyComponent name="foobar" />;

// ...
class MyComponent extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}

/** <h1>Hello, foobar!</h1> */
```

- Components can have its own internal `state`

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);

    this.state = {
      name: null
    };
  }

  render() {
    return <h1>Hello, {this.props.name}!</h1>;
  }
}

// Now, name refers to an internal state instead of a passed prop.
```

- In React, We use `setState` instead of _mutating_ `this.state` directly.

```jsx
class MyComponent extends React.Component {
  constructor(props) {
    super(props);

    this.state = {
      name: "foo"
    };
  }

  render() {
    return (
      <h1 onClick={() => this.setState({ name: "bar" })}>
        Hello, {this.props.name}!
      </h1>
    );
  }
}
/** <h1>Hello, bar!</h1> */
```

- If a Component doesn't maintain its own state, it could be simplified to a functional component.

```jsx
function MyFunctionalComponent(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```
