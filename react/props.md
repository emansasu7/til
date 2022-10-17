# Props!!!

- present in both function and class
- data passed from the top down to component and that renders on the screen, and now we're able to render several different components with differnet data
- TREE LIKE STRUCTURE

```
<!-- BOTTOM! -->
function Welcome(props){
    return Hello {props.name};
}


<!-- TOP!!! -->
function App(){
    return (
        <Welcome name="John"/>
        <Welcome name="Doe"/>
    )
}


function itemDesc (props){
    return Hello {props.item};
}
function Product (props){
    return(
    Hello {props.name};



    )
}

export default function App() {
  return (
      <Cepo name="Energed" price={11.99} />
      );


}

const Cepo = (props) => {
  return (
    <>
      <h2>{props.name}</h2>
      <Item desc="flavoured" />
      <h5>Price: {props.price}</h5>
    </>
  );
};

const Item = (props) => {
  return <p>{props.desc}</p>;
}


<!-- CLASS -->
{this.props.name}

OR const {name, decs} = this.props

then continue
<h2>{name}</h2>
```
