# React Typescript

[React Typescript Tutorial #1](https://www.youtube.com/watch?v=Z5iWr6Srsj8&t=409s)
going over props, hooks, and render props.

#### Props

<!-- Create a textfield component -->

```javascript
// creating the interface

// Can create another interface and pass that as a type to obj
interface Person {
  fName: string;
  lName: string;
}
interface Props {
  // can have object, boolean,function, number, string
  person: Person;
  text?: string;
  isOk: boolean;
  fn?: () => string; // can also pass parameters
  // etc
}

export const TextField: React.FC<Props> = () => {
  return <div>{Props.person.fName}</div>;
};
// so now we just added all our fields as props to our TF and now they're all required to pass into our Parent

export default function App() {
  return (
    <div className="App">
      <TextField text="Manu" ..etc />
    </div>
  );
}
```
