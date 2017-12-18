# Weekly-Assignments day 4
  Bind
     We use the Bind () method primarily to call a function with the this value set explicitly. It other words, bind () allows 
     us to easily set which specific object will be bound to this when a function or method is invoked.

     This might seem relatively trivial, but often the this value in methods and functions must be set explicitly when you need a 
     specific object bound to the function’s this value.
     
     with bind a function is returned that already has this bound. Later, when know the rest of the arguments we can pass them in
     
 This
    In most cases, the value of this is determined by how a function is called. It can't be set by assignment during execution, 
    and it may be different each time the function is called.
    
    Since the following code is not in strict mode, and because the value of this is not set by the call, this will default to the 
    global object , which is window in a browser. 

                  function f1() {
                    return this;
                  }

                  // In a browser:
                  f1() === window; // true 

                  // In Node:
                  f1() === global; // true
    Arrow Function
        An arrow function expression has a shorter syntax than a function expression and does not have its own this, arguments, 
        super, or new.target. These function expressions are best suited for non-method functions, and they cannot be used as 
        constructors.
        
