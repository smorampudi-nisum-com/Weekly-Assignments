# Weekly-Assignments Day 5
  Mediator Pattern:
    
    Define an object that encapsulates how a set of objects interact. Mediator promotes loose coupling by keeping objects from referring     to each other explicitly, and it lets you vary their interaction independently.
  
    The Mediator pattern provides central authority over a group of objects by encapsulating how these objects interact. This model is       useful for scenarios where there is a need to manage complex conditions in which every object is aware of any state change in any       other object in the group.

    The Mediator patterns are useful in the development of complex forms. Take for example a page in which you enter options to make a       flight reservation. A simple Mediator rule would be: you must enter a valid departure date, a valid return date, the return date         must be after the departure date, a valid departure airport, a valid arrival airport, a valid number of travelers, and only then the     Search button can be activated.
  
  Advantages:
  
      Two of the benefits of using the Mediator pattern are that that it decouples colleagues and simplifies object interaction. 
      Instead of using the Observer pattern to explicitly set many-to-many listeners and events, Mediator allows you to broadcast 
      events globally across colleagues. 
      
  Disadvantage in Using Mediator Pattern
  
      The biggest drawback of using Mediator pattern is that due to the centralized control, the mediator can become difficult to                 manage. In the case of this implementation, event broadcasting is greatly simplified which keeps the mediator managable.
      
  Pub/Sub Pattern
  
      The Publish/Subscribe pattern, however, uses a topic/event channel that sits between the objects wishing to receive notifications           (subscribers) and the object firing the event (the publisher). This event system allows code to define application-specific events         that can pass custom arguments containing values needed by the subscriber. The idea here is to avoid dependencies between the               subscriber and publisher.
  Difference between Pub/Sub and Observer
    
      This differs from the Observer pattern since any subscriber implementing an appropriate event handler to register for and receive           topic notifications broadcast by the publisher.
     
     From the code(in the design patterns folder consider the example pub Sub.html), the below line expalins 
      
          this.events[eventName] = this.events[eventName] || [];
          
          event can have multiple listeners, and those listeners may run different functions when that event occurs. If the 
          event already exists it's corresponding function will be added to the array of that list, otherwise it will create a 
          new item in the events object. He is storing all of the functions to be run when that event occurs in an array. Then 
          on emit when that event is triggered it will iterate though that array and run all of the functions belonging to that event.
Obsrever pattern
    Define a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated       automatically.
    
   The Observer pattern offers a subscription model in which objects subscribe to an event and get notified when the event occurs. This    pattern is the cornerstone of event driven programming, including JavaScript. The Observer pattern facilitates good object-oriented      design and promotes loose coupling.

   When building web apps you end up writing many event handlers. Event handlers are functions that will be notified when a certain        event fires. These notifications optionally receive an event argument with details about the event (for example the x and y position    of the mouse at a click event).
