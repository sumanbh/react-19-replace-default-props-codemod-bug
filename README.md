Codemod: `react/19/replace-default-props@1.0.3`

```sh
npx codemod@latest react/19/replace-default-props --target ./Button.js
```

Running the above command results in

```jsx
const Button = ({ size, color }) => {
  return <button style={{ color, fontSize: size }}>Click me</button>;
};
```

It should instead be

```jsx
const Button = ({ size = '16px', color = 'blue' }) => {
  return <button style={{ color, fontSize: size }}>Click me</button>;
};
```
