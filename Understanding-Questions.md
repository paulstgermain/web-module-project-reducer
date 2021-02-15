# Understanding Questions:
1. What are the steps of execution from the pressing of the 1 button to the rendering of our updated value? List what part of the code executes for each step.
* The user presses the 1 button.

* Our 'clickHandler' gets called.

* 'clickHandler' calls 'dispatch(addOne())'. In other words, it passes the result of 'addOne()', which is our 'action' ({type: 'ADD_ONE}) to dispatch.

* 'Dispatch' passes our action to our reducer, which checks the 'action.type' to determine which operation will occur.

* Upon hitting the 'ADD_ONE' case in our reducer, we execute a block of code which:
    1. Spreads our current 'state'
    2. Modifies 'state.total' to be equal to 'state.total' + 1
    
* TotalDisplay gets passed 'state.total' as a prop named value, which gets used as the value for the text field TotalDisplay holds and displays in our UI. As a result...

* TotalDisplay shows the total plus 1.
