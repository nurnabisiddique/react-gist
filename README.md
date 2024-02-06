# react-gist
Each useEffect hook is called at different times during the component's lifecycle, based on its dependency array (the second argument).

Initial Render and Dependency Changes: When the component mounts for the first time, or when any of the variables listed in the dependency array change, the useEffect hook is triggered.

Cleanup on Unmount: If the useEffect hook returns a function (cleanup function), that function is called when the component is unmounted or when the dependency array changes.

Let's break it down further:

No Dependency Array: If the dependency array is omitted (useEffect(callback)), the effect runs after every render.
Empty Dependency Array: If the dependency array is an empty array (useEffect(callback, [])), the effect runs only once after the initial render, similar to componentDidMount in class components.
Non-empty Dependency Array: If the dependency array contains variables (useEffect(callback, [variable1, variable2])), the effect runs after the initial render and whenever any of the listed variables change.
In the example provided:

The first useEffect runs whenever the count state changes.
The second useEffect runs only once after the initial render because it has an empty dependency array.
The third useEffect runs whenever the count state changes.
These useEffect hooks provide a way to execute side effects or perform cleanup operations at different points in the component's lifecycle.