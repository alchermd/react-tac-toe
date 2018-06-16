# react-tac-toe

My _code-along_ of the official [React Tutorial](https://reactjs.org/tutorial/tutorial.html).

## Notes

- Pass data through `props`

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
