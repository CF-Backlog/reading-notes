# Custom Hooks

What does a component’s lifecycle refer to?
> M.U.U. - the process of inserting(Mounting), updating(Update), deletion(Unmounting).

Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect
> callback will prevent repeat renders.

Why are functional components preferred over class components?
> they are cleaner and have fewer lines of codes for the same/more flexible functionality. Less margin for confusion.

What is wrong with the following code?
> effect hook might not work inside the loop.

=================================================
import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
===================================================

state hook - like a magic wand, let's you use state and other features of react without a class.

effect hook - Data fetching, setting up a subscription, and manually changing the DOM in React components are all examples of side effects. Effect hook allows you to perform these.

reducer hook - usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one.


Which 3 things had you heard about previously and now have better clarity on?

Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

What are you most excited about trying to implement or see how it works?
Redux
