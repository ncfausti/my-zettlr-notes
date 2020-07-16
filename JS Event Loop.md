20200708193624

# JS Event Loop

essentially a task queue that runs functions/code when the stack is empty

if the stack is empty, the event loop pushes next item in queue onto the stack

usage: `setTimeout(callBack, 0)`  // just waits until the stack is empty to run `callBack` function. setTimeout is a  minimum, not an exact.

Components of the browser:

1. Stack
2. webapis
3. event loop
    4. render queue - higher priority than callback queue
    5. callback queue

main ideas:
1. don't put slow code on the stack so we don't block the render queue and freeze the ui
    2. animations, high cpu processing, web requests
    3. but also don't flood the event queue, only do the work every n seconds or something similar

#javascript