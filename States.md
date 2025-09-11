State in react Js

Why state Required
What is state
what are hooks
how to use state 
States in different Components
Multiple States 

State in class component
in app.js
function App(){
    let fruit = "mango";

    //Making a function
    const handleFruit = () =>{
        fruit = "banana";
        console.log(fruit);
    }

    return (
    <h1>States in react js</h1>
    <h2>fruit is {fruit}</h2>
    <button onClick ={handleFruit}>change fruit Name</button>
    

)
}

the react js will update the value in the ui when its component will re render
But in the above example the component is not re rendering so the value is not updating in the ui
So to re render the component we use state

**What is state ?
state is a container to store the data like variable 
This is mutable and dynamic
we have to import it when we want to use it
It re-render component automatically so that data can visible on UI
 
**What is variable ?
variable is a container to store the data like state
This is immutable and static 
this will not re-render component automatically so that data is not visible on UI

**what are hooks ?
Hooks are the special features for functional component 
Hooks let you use different React features from your components 
**State
**Lifecycle methods
Side effects

**How to identify the hooks
whenever the function name starts with use
eg: useState , useEffect


**Importing the state 
import  { useState } from 'react';

Example : in app.js
import  { useState } from 'react';
function App(){
    //Declaring the state
    const [fruit, setFruit] = useState("mango");  fruit is the variable name --> it is a  state  and setFruit is the function name --> updated state to update the value of fruit

    //Making a function
    const handleFruit = () =>{
        setFruit("banana");  //Set fruit is used to update the value of fruit it is a 2nd value of useState
        console.log(fruit);
    }

    return (
    <h1>States in react js</h1>
    <h2>fruit is {fruit}</h2>
    <button onClick ={handleFruit}>change fruit Name</button>
    //Importing the new component named Counter.js
    <Counter/>

)
}

Creating the new component named Counter.js

const Counter =()=>{
    const[data,setData] = useState(0); //data is the variable name and setData is the function name to update the value of data
    const[rCount,setRcount] =useState(10);
    return (
        <div>
            <h1>Counter App:{data}</h1>
            <button onClick={()=>setData(data+1)}>button counter</button>
            <button onClick={()=>setRcount(rCount-1)}>decrease counter</button>
            <h2>Random Count:{rCount}</h2>
        </div>
    )
}
export default Counter;
