# What is redux?

It is a state management system for cross-component or add-wide state.

It helps us manage state data that changes and affects our application and
what we display on the screen. It helps us manage such data across multiple
components or even the complete app.

We can split the definition of state into three kind of state

- local state (managed by useState and useReducer)
- cross component state (state passed from parent to child components using prop drilling)
- app-wide state (managed by Context API, Redux, Redux toolkit)

Why do we need redux if we have context api for managing app wide state?

## Redux vs React Context

React context has some potential disadvantages

- React context has complex setup for large scale application
- Potential problem: deeply nested providers
  `
return (
       <AuthContextProvider>
           <ThemeContextProvider>
               <UIInteractionContextProvider>
                   <MultiStepFormContextProvider>
                       <UserRegistration />
                   </MultiStepFormContextProvider>
               </UIInteractionContextProvider>
           </ThemeContextProvider>
       </AuthContextProvider>
   )`

here you have multiple piece of state which manages manages different components

- If we move the above providers in to one big context that will introduce another level of
  complexity because the same context context will be managing multiple states.

- Another potential disadvantage could be performance

- Context API is recommended for apps which have low frequency updates and small amount of shared state.
- It is not recommended for apps in which the data changes a lot

## How redux works?
