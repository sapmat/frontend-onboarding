# Frontend Onboarding

Welcome!

This exercise is designed to introduce you step-by-step to the fundamentals of `frontend development`

> [!NOTE]
>
> - This does not cover everything about `frontend development`, but it will give you enough understanding to begin creating your own features and improving independently
> - This is just exercises to learn how to develop from a more hands on point of view, if you want more in depth explanation feel free to do your own research

---

## LEVELS NAVIGATION

- [Level 1 – Start](#level-1)
- [Level 2 – States](#level-2)
- [Level 3 – Styling (Emotion)](#level-3)
- [Level 4 – Routes](#level-4)
- [Level 5 – Application Storage](#level-5)
- [Level 6 – JWT](#level-6)
- [Level 7 – Mock API](#level-7)
- [Level 8 – Custom Hooks](#level-8)
- [Level 9 – Table Data](#level-9)
- [Level 10 – Modal](#level-10)
- [Level 11 – Store (Redux)](#level-11)
- [Level 12 – Context](#level-12)

---

> [!WARNING]
>
> Make sure that stuff are responsive to some extent, you will not be tested on it too much because you will not be using any special UI libraries that will help, but do make sure that it has a basic responsivity

---

## <a id="level-1"></a> LEVEL 1 – START

We will begin very simple by creating a login page.

TODO:

- Create a basic `Login` page with:
  - An input for email
  - An input for password
  - A submit button
- No hooks, no styling yet

---

## <a id="level-2"></a> LEVEL 2 – STATES

React provides hooks like `useState` to easily handle component state.

TODO:

- Create a mock data file containing a few users
- Using `useState`, when the `submit` button is clicked:
  - If login data matches a user in mock data show success message
  - Otherwise show error message
- Display the message under the `submit` button

---

## <a id="level-3"></a> LEVEL 3 – STYLING (EMOTION)

Now add styling using Emotion.

TODO:

- Create a styling file using Emotion
- Add styling to your login page

---

## <a id="level-4"></a> LEVEL 4 – ROUTES

Create a second page in your application and navigate between pages.

TODO:

- Create a Home page:
  - Header with a hello message and a `Logout` button
  - Main content (empty for now)
- Style the page with natural, matching colors
- Do that when you enter a valid user in the `Login` page, that you get auto redirected to the home page
- Add a `Navbar` component and for now, just have the `home` route on it

---

## <a id="level-5"></a> LEVEL 5 – APPLICATION STORAGE

Now that you can enter the site, you want that the user to stay connected even if he exists and rejoins the page

TODO:

- Read about different types of `application storage` and store in it the connected user data
- Add to `Login` a `remember me` button that will remember the user for 30 days before forgetting him
- If the user is not logged in, automatically redirect him to the `Login` page

---

## <a id="level-6"></a> LEVEL 6 – JWT

When we need to store specific information about a user and verify their identity, we use a technology called `JSON Web Tokens (JWT)`

TODO:

- Read about `jwt` and implement it into what you did in `level 5`
- Add `jwt` validation, if the `jwt` is invalid, then logout the user

---

## <a id="level-7"></a> LEVEL 7 – MOCK API

Your project will revolve around `events`  
Since there's no backend, you'll build a simple mock API

> [!NOTE]
>
> Keep your mock API simple. It only needs to provide your UI with usable data.

TODO:

- Add additional fields to each `user` (e.g. username, job, location, etc.)
- Create a mock db for all the `events`  
  Each `event` should include (add more fields if you think it's needed):
  - name
  - time
  - duration
  - location
  - host:
    - id
    - username
  - attendees[]:
    - id
    - rating
- Create a service file for each mock data file.
- Create a function to validate `user` credentials during login.

---

## <a id="level-8"></a> LEVEL 8 – CUSTOM HOOKS

In `React` you can create your own hooks which will be annotated by using the word `use` before the hook name, like there is `useState` and `useEffect`

TODO:

- Create a custom hook that will manage doing api calls

---

## <a id="level-9"></a> LEVEL 9 – TABLE DATA

Here you will learn about how to create a table that will allow you to display the `events`

> [!NOTE]
>
> Learn about how to pass props to a component

TODO:

- Create a Table component that displays all future `events`
- Add pagination to the table (use `react-paginate`)
- Create a Filter component to filter table rows
- Add a `Clear` button to reset all filters

> [!NOTE]
>
> Consider carefully what `events` you want to display

---

## <a id="level-10"></a> LEVEL 10 – MODAL

Modal are an essential part of `frontend development`, they allow you to display a card above the rest of the screen and force the user to interact with it

So now that you have a way to display all the future `events`, you might want to view each `event` in more details  
Also, you may want to view all the events that you want to attend/attended, or the ones that you are hosting

TODO:

- Do that when you double click a row a popup opens:
  - Create a popup that will nicely display all the information of an `event`
  - Add to the popup a button that allows you to schedule yourself to the `event` if it not one that you host
  - If the host of the `event` is the user then add an `Edit` button that will enter you into an editing state and there the user can edit the information (think if there could be stuff that he can't edit), and save or cancel the new changes
  - If the host of the `event` is the user then add a `Delete` button that will open another modal that will ask you if you are sure that you want to delete the `event`
- Add a `Schedule` page, and add to it the following:
  - The user will have a table like the one in `level 8` but this time it will display `events` related specifically to the user
  - Add a button to switch between the `events` that are hosted by the user, the `events` that he is wants to attend, or both
  - Add a filter bar to filter the `events`
  - Add an `Add Event` button which will open a modal and allow you to create a new `event`

---

## <a id="level-11"></a> LEVEL 11 – STORE (REDUX)

`Stores` in `frontend development` are very important, they allow you to access states on a **global** level in your system

> [!NOTE]
>
> You can have multiple stores in your system, but each store should focus on a single, well-defined purpose

> [!WARNING]
>
> `Stores` are not meant to hold heavy data, when creating it, notice what you put in it
> You can put data, just don't put every state you have in it, make sure it is only stuff that are needed all over your system

TODO:

- Read about `Redux` and add a store to your system that will hold the information of the connected user
- Create a store that will hold some of the `events`, think what is the most accurate way to do it while keeping in mind the warning above

---

## <a id="level-12"></a> LEVEL 12 – CONTEXT

`Contexts` in `React` allow you to wrap components and have states that can be used from anywhere within those components  
As you might have guessed, the `Store` from `level 10` is also a type of context

The in order to use the `context`, you need to wrap the components you want with it's `provider`  
When creating the provider, you can also add components that will automatically be added when you call it

TODO:

- Add a `context provider` that will show alerts in your system
- Think when you should have success/failed/info or another type of alerts and add them accordingly
- The behavior of the alerts will be:
  - Make sure that the alerts will pop up in the bottom left on the screen
  - After 5 seconds the alert will be removed
  - If you click the alert it gets removed automatically
  - Each alert will have either an icon or color or anything of your choosing, that will be unique to that type of alert
  - Do that when an alert appears or gets removed it slide in/out of view and not just to pop-in

---
