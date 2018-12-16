# State and lifecycle in a React component

This is a systematic guide to understand the concept of state and lifecycle in a React component for beginners.

## Assumption

- [You have a runnable react app, otherwise create a quick one!](https://github.com/h09shais/webpack4-babel7-react-app#part-04---bonus)

### React elements are immutable

React elements are the smallest building blocks of React apps and those are immutable.

#### React element

```javascript
const element = <h1>The price of this product is 200 DKK</h1>;
```

#### React component and props

Conceptually, React components are similar as JavaScript functions that accept arbitrary inputs and return React elements describing what should appear on the screen.
Those arbitrary inputs called "props" which stands for properties.
A component must never modify its own props.

We can declare a component as a function or a class.

```javascript
function Display(props) {
  return <h1>The price of this product is {props.price} DKK</h1>;
}
```

```javascript
class Display extends React.Component {
  render() {
    return <h1>The price of this product is {props.price} DKK</h1>;
  }
}
```
