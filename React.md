React Syntax:
function User(){
    return (
    <h1>hello user</h1>
    <User name = "aish"/>

)
}
export default User



React props 
What is props ?
Make component 
Pass the data between components 
***var ,object ,array
Click event 

receive and display Data
Pass the data in component with click 


Props:
when we need to pass the data from one components into another
Props are used to pass data from one component to another component in React. Props are read-only and cannot be modified by the receiving component.
we will define as 
<Componentname propname={"Value"} />
The componentname is the name of the component we are passing the data to, and propname is the name of the prop we are defining. The value can be a string, number, boolean, object, or array.

Example : In app.js file
function App(){
    return (
    <h1>hello user</h1>
    <User name = "aish"/>

)
}
export default User;

Now v need to receive the data in the User component

function User(props){
    return (
    <h1>hello {props.name}</h1>

)
}  

if v have multile props to pass:
function App(){
    return (
    <h1>hello user</h1>
    <User name = "aish" age={20} city={"bangalore"}/>

)
}
export default

User component:
function User(props){
    return (
    <h1>hello {props.name} , age is {props.age} , city is {props.city}</h1>

)
}

Object as props:***** passing object as props ***** General syntax to pass object as props is <Componentname propname={objectname}/>
function App(){
    const user = {
        name:"aish",
         age:20, 
         city:"bangalore"
         };
         const user2 = {
            name:"ram",
             age:22, 
             city:"hyd"
             };

    return (
    <h1>hello user</h1>
    <User user={user}/> ***** passing object as props ***** General syntax to pass object as props is <Componentname propname={objectname}/> propname can be any name
    <User user={user2}/>

)
}

export default User;

function User(props){
    return (
    <h1>hello {props.user.name} , age is {props.user.age} , city is {props.user.city}</h1>

)
}


Arrays as props:  everything as to be done in app.js
function App(){
    const users = [
        {name:"aish", age:20, city:"bangalore"},
        {name:"ram", age:22, city:"hyd"},
        {name:"sam", age:21, city:"chennai"}
    ];

    return (
    <h1>hello user</h1>
    <College users={users}/> ***** passing object as props ***** General syntax to pass object as props is <Componentname propname={objectname}/> propname can be any name

)
}
export default User;
 ** this in component file called College.js
function College(props){
    return (
    <div>
        {props.users.map((user, index) => (
            <h1 key={index}>hello {user.name} , age is {user.age} , city is {user.city}</h1>
        ))}
    </div>

)
}


Click event :
