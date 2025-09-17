# Queue Management App

## -- HOW TO RUN --

1. Download the ZIP file  
2. Extract it  
3. Open Terminal  
   - Type:  
     1. `npm install`  
     2. Then type: `npm start`  
     3. Copy the link and open it in your browser  

---

## Core of the project: Redux functionality

### How it works:

When the form is submitted, the `addToInQueue` method is invoked. The submitted data is pushed into the `InTheQueue` array. This triggers a re-render of the component because the initial state in the Redux slice has changed. As a result, the `UserDetails` component becomes visible in the `InTheQueue` section.

Up to this point, everything works as expected.

### What happens when the user clicks on the UserDetails card?

Each `UserDetails` card has an `onClick` function:

- On the **first click**, the user is moved from `InTheQueue` to `MixingQueue`.  
- On the **second click**, the user is moved from `MixingQueue` to `ReadyQueue`.  
- On the **third click**, the order is marked as collected and removed from the queue.
