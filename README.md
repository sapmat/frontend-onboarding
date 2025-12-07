# Frontend Onboarding

Welcome!

This exercise is designed to introduce you step-by-step to the fundamentals of `frontend development`!

> [!NOTE]
>
> - This does not cover everything about `frontend development`, but it will give you enough understanding to begin creating your own features and improving independently
> - This is just exercises to learn how to develop from a more hands on point of view, if you want more in depth explanation feel free to do your own research

> [!IMPORTANT]
>
> This exercise is meant to be completed using the `React` framework
> If you choose to work with another framework such as `Vue` or `Angular`, make sure you understand the equivalent concepts and how to implement them there

> [!NOTE]
>
> Don't worry, with time and experience you will grow to have a natural feel for everything that you practice here and learn more about `frontend development` and that it's not that scary

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

> [!NOTE]
>
> When solving a level, only use what you have learned from previous levels

---

## <a id="level-1"></a> LEVEL 1 – START

Every good project has to start from somewhere, so we will start simple and grow our project with each level.

The goal for this level is simply to get comfortable creating components and rendering inputs.


TODO:

- Create a basic `Login` page with:
  - An input for email
  - An input for password
  - A submit button

---

## <a id="level-2"></a> LEVEL 2 – STATES

`React` provides us the ability to use `hooks`, like `useState` and `useEffect`, to easily handle component states and behavior.

TODO:

- Create a mock data file containing a few `users` (think what fields each `user` might need)
- Using `useState`, when the `submit` button is clicked:
  - If login data matches a user in mock data show success message
  - Otherwise show error message
- Display the message under the `submit` button

---

## <a id="level-3"></a> LEVEL 3 – STYLING (EMOTION)

Styling is a very important part of `frontend development` which allows us to add colors, designs and much more to bring life and personality into our project.

In this project, we will be styling our system using `Emotion` (CSS-in-JS).  
Focus on creating separate style files and keeping styles clean and organized.

TODO:

- Create a styling file using Emotion
- Add styling to the `Login` page

---

## <a id="level-4"></a> LEVEL 4 – ROUTES

A good site _(normally)_ has more than just a single page, and each page is represented by a different `route` in the system. For example, `coolDomain.com/login`, `coolDomain.com/home`, etc.  
In order to actually tell the system that we want to go from one page to another, we will have to create new `routes` and a way to navigate between them.

Here we will practice navigation using `React Router`, by creating a `Home` page, and adding a `navigation bar`, aka a `navbar`.

TODO:

- Create a Home page:
  - Header with a hello message and a `Logout` button
  - Main content (empty for now)
- Style the page with natural, matching colors
- Make it that when the `user` enters a valid user in the `Login` page, that he gets auto-redirected to the `Home` page
- Add a `Navbar` component, for now just have the `home` route on it

---

## <a id="level-5"></a> LEVEL 5 – APPLICATION STORAGE

When we log into a site, we want the site to remember who we are and not have to login every time we refresh the page.

So now that we created the ability to log into the site, we will practice remembering for the short and long term the user's login info.

TODO:

- Read about different types of `application storage` and store in it the connected `user` data (think what data should and shouldn't be saved)
- Add to `Login` a `remember me` button that will remember the `user` for 30 days before forgetting him
- If the user is not logged in, automatically redirect him to the `Login` page

---

## <a id="level-6"></a> LEVEL 6 – JWT

When we save the user’s info in the browser, the `user` can see it and even change it, which is a problem.  
To fix this, we use `JSON Web Tokens (JWTs)`.

A `JWT` is a small token the server creates after the `user` logs in.  
It’s signed, so the server can check if it was changed.  
If someone tries to tamper with it, the server will know.  
This lets us store `user` data safely, and be sure the token really belongs to that `user`.

TODO:

- Read about `jwt` and implement it into what we did in `level 5`
- Add `jwt` validation, if the `jwt` is invalid, then logout the user

---

## <a id="level-7"></a> LEVEL 7 – MOCK API

Normally, projects have a `backend` and `data base`, which hold and provide all the data that is used in the system.  
Since we are not using either right now, we will practice creating and using a `mock API` which will fill the role of both.

> [!NOTE]
>
> - This could happen a lot in projects, when you want to create a `frontend` feature, but you don't have the `backend` ready yet, or don't know what `data` you might need, so you create a `mock` and use it for the start
> - Remember to keep your `mock API` simple, it only needs to provide your UI with usable data.

Our project will revolve around `events`. So we will practice creating a `mock API` to store those `events`.

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
- Create a service file for each mock data file
- Create a function to validate `user` credentials during login

---

## <a id="level-8"></a> LEVEL 8 – CUSTOM HOOKS

In `React`, we can create our own `custom hooks`, which will allow us to create and manage our own states and other behaviors.  
To create a `hook`, is traditionally annotated by using the word `use` before the `hook` name. Just like there is `useState` and `useEffect`, which are `hooks` provided by `React`, we can create our own hook, for example `useHook`.

Here we will practice creating our own `custom hook`.

TODO:

- Create a custom hook that will manage doing api calls

---

## <a id="level-9"></a> LEVEL 9 – TABLE DATA

When we have a site, in one way or another, we want to display our data.  
There are many ways we can do so, such as `cards`, `tables`, `lists` and many more.

Here we will create a `table` that will display the `events` and their information.

TODO:

- Learn about how to pass props into a component
- Create a Table component that displays all future `events`
- Add pagination to the table (use `react-paginate`)
- Create a Filter component to filter table rows
- Add a `Clear` button to reset all filters

> [!NOTE]
>
> Consider carefully what `events` we want to display

---

## <a id="level-10"></a> LEVEL 10 – MODAL

Modal are an essential part of `frontend development`, they allow us to display a sort of `card` above the rest of the screen and force the user to interact with it.

So now that we have a way to display all the future `events`, we might want to view each `event` in more details.  
Also, we might want to view all the `events` that we want to attend/attended, or the ones that we are hosting.

TODO:

- Add to the table the functionality, which when the `user` double click a row a `modal` opens:
  - Create a `modal` that will nicely display all the information of an `event`
  - Add to the `modal` a button that allows the `user` to schedule to himself the `event` if it not one that they host
  - If the host of the `event` is the `user` then add an `Edit` button that will enter the `user` into an editing state and there the `user` can edit the `event's` information (think if there could be stuff that he can't edit), and save or cancel the new changes
  - If the host of the `event` is the user then add a `Delete` button that will open another modal that will ask you if you are sure that you want to delete the `event`
- Add a `Schedule` page, and add to it the following:
  - The user will have a table like the one in [`level 9`](#level-9) but this time it will display `events` related specifically to the user
  - Add a button to switch between the `events` that are hosted by the user, the `events` that he is wants to attend, or both
  - Add a filter bar to filter the `events`
  - Add an `Add Event` button which will open a modal and allow you to create a new `event`

---

## <a id="level-11"></a> LEVEL 11 – STORE (REDUX)

`Stores` in `React` are very important, they allow us to access states on a **global** level in our system. Supposed we have a state that is used all over the system, such as the `connected user`, instead of having to pass it every time into every component, or just across many components just to access it somewhere down the line, we can create a `store` that will, to no surprise, store the information and access it anywhere.   
Another thing we can do with `stores`, is that we can add functions that we call to update the `store's` data, and using those functions we can do that any time it's called, the same common behavior will happen. For example, if we store the user's birth date, we can do that automatically every time we call the function to update it, it also updates the age field, and also calls the `backend` to update it.

> [!NOTE]
>
> We can have multiple stores in our system, but each `store` should focus on a single, well-defined purpose

> [!WARNING]
>
> `Stores` are not meant to hold heavy data, when creating it, notice what we put in it
> We can put data, even rather large and complex data, just don't put every state we have in it, make sure it is only stuff that are needed all over our system

TODO:

- Read about `Redux` and add a store to your system that will hold the information of the `connected user`
- Create a store that will hold some of the `events`, think what is the most accurate way to do it while keeping in mind the warning above

---

## <a id="level-12"></a> LEVEL 12 – CONTEXT

In `React`, we have special `Providers` that are called `Contexts Providers`, which allow us to wrap components and have states that can be used from anywhere within those components.  
As you might have realized, our `Store` from [`level 11`](#level-11) is also a type of `context`.

In order to use a `context`, we need to wrap the components we want with it's `provider`.  
When creating the provider, we can also add components that will automatically be added when we call it. For example, if we were to add a `Light-Dark Mode Provider`, we can add that it will automatically add a button to switch between the modes on the bottom-right of the screen.

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
