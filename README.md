Codemod: `react/19/replace-default-props@1.0.3`

```sh
npx codemod@latest react/19/replace-default-props --no-cache --target ./Button.js
```

Running the above command

```
✔ Successfully downloaded "react/19/replace-default-props" from the registry.
╭─────────────────────────────────────────────────────────────────────────────────────────────╮
│                                                                                             │
│                                                                                             │
│      Codemod: react/19/replace-default-props@1.0.3                                          │
│      Target: .                                                                              │
│                                                                                             │
│      Using paths provided by user via options                                               │
│      Included patterns: **/Button.js                                                        │
│      Patterns excluded by default: **/*.d.ts, **/node_modules/**/*.*, **/.next/**/*.*,      │
│      **/dist/**/*.*, **/build/**/*.*, **/.git/**/*.*,                                       │
│      **/.svn/**/*.*, **/.hg/**/*.*, **/.bzr/**/*.*,                                         │
│      **/_darcs/**/*.*, **/_MTN/**/*.*, **/_FOSSIL_, **/.fslckout,                           │
│      **/.view/**/*.*                                                                        │
│                                                                                             │
│      Running in 4 threads                                                                   │
│      File formatting disabled                                                               │
│                                                                                             │
│                                                                                             │
╰─────────────────────────────────────────────────────────────────────────────────────────────╯
```

results in this output:

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
