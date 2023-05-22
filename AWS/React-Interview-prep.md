1. Why react
2. JSX
3. Cutom components
4. Styling
5. Props and State

# Why React
- React allows us to write composable code.
- React is declarative (We just tell it what should be done)
- Maintained by skilled people
# JSX 
- JSX is a JavaScript syntax extension that allows you to write HTML-like code in JavaScript for building user interfaces.
- ReactDOM.render(navbar, document.getElementById("root")) `react-17`
- ReactDOM.createRoot(document.getElementById("root")).render(navbar) `react-18`
- custom component uses pascal case(capitalize first letter)!=Camel case
- `{props.setup && <h3>Setup: {props.setup}</h3>}` conditional rendering using javascript and JSX
# Props and state.
- Props, properties being passed to a component, they are immutable just like parameters in normal function.
- States, refers to values that are managed by the component, they are similar to variables declares inside a function.
- `let [isImportant, setisImportant] = useState()`;
- whenever we need our old version of state to have our new version of state, we should use a callback in our `setState(prevState => prevState + 1)`
- lifting up state from childen to parent to solve sibling to sibling problems can also be done by redux or Context
- derived state is when you create state from incoming props (which is state send from parent component as prop) We don't need it because it caused two source of truth and we can avoid it by using the toggle function.
- conditional rendring
## forms in React.
- People use forn library on react because form is complicated.
- name property plays a special role, if we make it match the key in the object of our state, it can help get the value.
- controlled Components (add value to input field so that state is single source of truth)
## useEffect();
- it is used to handle side effects on react.
- it takes two parameters, a callback and a dependency array
- It runs after every render.

Advance React:

1. Misc. intro topics
2. reusability/Patterns
3. performance/Optimization
4. Context
5. Hooks
6. React Router
7. Capstone Project
8. Redux, react has his own states management API.


# Misc. intro topics|Introduction
- defaultProps is used for us to have a default value if no props is given to the component
- propsTypes is used to specify that incoming props shoud have a given type.
- PropsTypes can be used for many ofher things.

# Reusability
- props.children are use to access chidren in react component.
- HOC is a function that takes a component as its first argument and returns a new component that wraps the given component, providing extra capabilities to it.
- Render props 
- Read more on render props and HOC

# Performance
## React rendering three.
- React renders one branch of the tree after another.
- Shallow comparison
- Should component update
- Pure components: React.PureComponent should be use instead of Shouldcomponents Update(this is for class component)
- React.memo() is for components

# React context.
- Pass state though the three without having to pass props manually
- Some people choose Context over Redux.

# React Hooks.
- Hook into state lifecycle methods of components without using classes.
- Only use functional components accross the board.
- Improve readability and organisation of components.
- useState() and useEffect();
- useEffect() returns a function when we want to remove some side effect after component unmount.
- Useref() gives us a way to keep values around for the entire lifecycle of the component. 