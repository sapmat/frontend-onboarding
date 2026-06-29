# Frontend Onboarding

**Welcome to your frontend onboarding!**

This exercise is designed to introduce you step-by-step to the fundamentals of frontend development!

> [!NOTE]
> - This won't cover everything there is to know in frontend development — but it will give you enough foundation to start building features and growing independently.
> - These are hands-on exercises focused on practical development. For deeper explanations, feel free to research on your own.

> [!IMPORTANT]
> This exercise is meant to be completed using the `React` framework.
> If you choose to work with another framework such as `Vue` or `Angular`, make sure you understand the equivalent concepts and how to implement them there.

> [!NOTE]
> Don't worry — with time and practice, these concepts will become second nature.
>
> Frontend development is way more fun and enjoyable than people think.

---

## Overview

In this project, you will build a single project and expand it step by step through the levels below. Each level builds on the previous ones — stick to concepts introduced in the current level or earlier.

> [!NOTE]
> If you need a reference along the way, the official [react.dev Learn](https://react.dev/learn) guide is a great place to start.

---

## Tech Stack

You will use the following throughout this exercise:

- **React** (function components only)
- **TypeScript**
- **Vite** (project bootstrapping and dev server)
- **Emotion** (CSS-in-JS — keep styles in dedicated `styles.ts` files)
- **React Router** (routing)
- **React Query** (server state management and data fetching)
- **MobX** (global state management)

> [!WARNING]
> Maintain basic responsiveness all throughout your project. You won't be tested heavily on it, but layouts should not break on common screen sizes.

---

## Levels

- [Level 1 – Components & Inputs](#level-1)
- [Level 2 – State & Effects](#level-2)
- [Level 3 – Styling with Emotion](#level-3)
- [Level 4 – Routing](#level-4)
- [Level 5 – Application Storage](#level-5)
- [Level 6 – JWT](#level-6)
- [Level 7 – Mock API](#level-7)
- [Level 8 – Custom Hooks](#level-8)
- [Level 9 – React Query](#level-9)
- [Level 10 – Table Data](#level-10)
- [Level 11 – Modals](#level-11)
- [Level 12 – Stores (MobX)](#level-12)
- [Level 13 – Context & Providers](#level-13)

---

> [!WARNING]
> Make sure that stuff are responsive to some extent, you will not be tested on it too much because you will not be using any special UI libraries that will help, but do make sure that it has a basic responsively

> [!NOTE]
> When solving a level, only use what you have learned from previous levels

---

## <a id="level-1"></a> LEVEL 1 – Components & Inputs

Every good project has to start from somewhere, so we will start simple and grow our project with each level.

The goal for this level is simply to get comfortable creating components and rendering inputs.

Tasks:

1. Create your very own, new `React` + `TypeScript` project with `Vite`.
2. Create a `Login` page with the following:
   - An email input.
   - A password input.
   - A submit button.

---

## <a id="level-2"></a> LEVEL 2 – State & Effects

`React` provides us with the ability to use custom built-in `hooks` like `useState` and `useEffect`, to easily handle component states and behavior.

**Tasks:**

1. Create a mock data file containing several users (decide what fields a user might needs).
2. Using `useState`, when the submit button is clicked:
   - If the credentials match a user in the mock data — display a success message.
   - Otherwise — display an error message.
3. Render the message below the submit button.

---

## <a id="level-3"></a> LEVEL 3 – Styling with Emotion

Styling is a very important part of frontend development which allows us to add colors, designs and much more to bring life and personality into our project.

In this project, we will be styling our system using `Emotion` (CSS-in-JS).

Tasks:

1. Create a `styles.ts` file for the `Login` page.
2. Style the login form — use natural, matching colors and clear visual hierarchy.

---

## <a id="level-4"></a> LEVEL 4 – Routing

A good site *(normally)* has more than just a single page, and each page is represented by a different `route` in the system. For example, `coolDomain.com/login`, `coolDomain.com/home`, etc.

In order to actually tell the system that we want to go from one page to another, we will have to create new `routes` and a way to navigate between them.

Here we will practice navigation using `React Router`, by creating a `Home` page, and adding a `navigation bar` (aka a `navbar`).

Tasks:

1. Create a `Home` page containing:
   - A header with a greeting message and a `Logout` button.
   - A main content area (empty for now).
2. Style the page with consistent colors.
3. On successful login, redirect the user to the `Home` page.
4. Add a `Navbar` component with a link to the home route.

---

## <a id="level-5"></a> LEVEL 5 – Application Storage

When we log into a site, we want the site to remember who we are and not have to login every time we refresh the page.

So now that we created the ability to log into the site, we will practice remembering for the short and long term some of the user's login info.

Tasks:

1. Read about different types of application storage, and store in it the connected `user` data.
2. Add to the `Login` page a `remember me` checkbox, that will remember the `user` for 30 days before forgetting him.
3. If the user is not logged in, automatically redirect him to the `Login` page.

> [!NOTE]
> Think carefully about what data should and should not be stored client-side.
> Think carefully about where that data should be saved.

---

## <a id="level-6"></a> LEVEL 6 – JWT

When we save the user's information in the browser, anyone can easily see it in the browser and change it, which is a huge problem.

To fix this, we use JSON Web Tokens (`JWT`s).

A `JWT` is a small token the server creates after the `user` logs in.  
It’s signed, so the server can check if it was changed.  
If someone tries to tamper with it, the server will know.  
This lets us store `user` data safely, and be sure the token really belongs to that `user`.

**Tasks:**

1. Read about JWT structure and purpose and implement it into what we did in `level 5`.
2. Generate and store a JWT upon successful login instead of raw user data.
3. Add JWT validation — if the token is invalid or expired, log the user out and redirect to `Login`.

---

## <a id="level-7"></a> LEVEL 7 – Mock API

Normally, projects have a backend and database, which hold and provide all the data that is used in the system.

Since we are not using either right now, we will practice creating and using a mock API which will fill the role of both.

> [!NOTE]
> This is a common pattern — building frontend features before the backend is ready.  
> Remember to keep your mock simple — it only needs to provide usable data to your UI.

Our project will revolve around `events`. So we will practice creating a mock API to store those `events`.

**Tasks:**

1. Expand user objects with additional fields (e.g. username, role, location, or whatever you think is necessary).
2. Create a mock database for events. Each event should include at minimum:
   - `name`
   - `time`
   - `duration`
   - `location`
   - `host` — `{ id, username }`
   - `attendees[]` — `{ id, rating }`
   -  whatever other information that you think will be useful.
3. Create a `*.service.ts` file for each mock data entity.
4. Add to your mock server also your user management.

---

## <a id="level-8"></a> LEVEL 8 – Custom Hooks

In `React`, we can create our own custom hooks, which allow us to encapsulate and reuse stateful logic and other behaviors.  
By convention, a custom hook's name must start with the word `use` — just like React's built-in hooks such as `useState` and `useEffect`. For example, we might create a hook called `useApi`.


Here we will practice creating our own custom hooks.

**Tasks:**

1. Create a custom hook that will manage our API calls.
2. Create a custom hook that will manage our connection to the application storage.

---

## <a id="level-9"></a> LEVEL 9 – React Query

`React Query` is a powerful library for managing server state in `React` applications. Unlike client state (which we manage with `useState` or `MobX` *(which we will get to that later)*), server state is data that lives on a remote server and can become outdated, needs to be fetched, cached, synchronized, and updated.

`React Query` handles all of this for us, providing features like automatic caching, background re-fetching, stale data management, and optimistic updates — without having to write all that logic manually.

> [!NOTE]
> - `React Query` replaces the need for most custom data-fetching hooks and manual loading/error state management
> - It is not a replacement for `MobX` — `MobX` handles client/global state, while `React Query` handles server/remote state

Tasks:

1. Read about `React Query` and install `@tanstack/react-query` in your project.
2. Set up a `QueryClientProvider` at the root of your application.
3. Refactor your existing API calls (from the custom hook in [`level 8`](#level-8)) to use `useQuery` for fetching data:
   - Fetch the `events` list using `useQuery` instead of your custom hook.
   - Notice how `React Query` manages loading and error states for you.
4. Use `useMutation` for modifying data:
  - Creating a new `event`.
  - Editing an existing `event`.
  - Deleting an `event`.
5. After each mutation, invalidate the relevant queries so the UI stays in sync with the server.
6. Add a visible loading indicator while data is being fetched.
7. Implement optimistic updates for at least one mutation (e.g. deleting an `event` should immediately remove it from the table before the server confirms).

---

## <a id="level-10"></a> LEVEL 10 – Table Data

When we have a site, in one way or another, we want to display our data.

There are many ways we can do so, such as cards, tables, lists and many more.

In our case, we will create a table that will display the `events` and their information.

**Tasks:**

1. Read about passing props into components.
2. Create a `Table` component that displays all future events.
3. Add pagination (use `react-paginate` or a similar library).
4. Create a `Filter` component to filter table rows by relevant fields.
5. Add a `Clear` button to reset all filters.

> [!NOTE]
> Consider carefully what events should be shown.

---

## <a id="level-11"></a> LEVEL 11 – Modals

Modals are an essential part of frontend development — they allow us to display a sort of card above the rest of the screen and force the user to interact with it.

So now that we have a way to display all the `events`, we might want to view each `event` in more details.

**Tasks:**

1. When the user double-clicks a table row, open a modal displaying full event details.
2. If the user is **not** the host — show a button to register for the event.
3. If the user **is** the host:
   - Add an `Edit` button that switches the modal to an editing state. The user can modify fields (think about which fields should be editable), then save or cancel.
   - Add a `Delete` button that opens a confirmation modal before deleting the event.
4. Create a `Schedule` page containing:
   - A table showing events related to the current user.
   - A toggle to filter between: events hosted by the user, events attended by the user, or both.
   - A filter bar.
   - An `Add Event` button that opens a creation modal.
5. Add the `Schedule` route to the `Navbar`.

---

## <a id="level-12"></a> LEVEL 12 – Stores (MobX)

Stores in `React` are very important — they allow us to access state on a global level in our system. Supposed we have a state that is used all over the system, such as the `connected user`, instead of having to pass it every time into every component, or just across many components just to access it somewhere down the line, we can create a `store` that will, *to none's surprise*, store the information and access it anywhere.

Another thing we can do with stores is add functions that we call to update the store's data, and using those functions we can do that any time it's called, the same common behavior will happen. For example, if we store the user's birth date, we can do that automatically every time we call the function to update it, it also updates the age field, and also calls the backend to update it.

> [!WARNING]
> Stores are not meant to hold heavy data. Only put state that is genuinely needed across multiple unrelated components.

> [!NOTE]
> You can have multiple stores — each should focus on a single, well-defined purpose.

**Tasks:**

1. Read about MobX — stores, observables, actions, and reactions.
2. Create a store for the connected user.

---

## <a id="level-13"></a> LEVEL 13 – Context & Providers

In `React`, we have special providers called context providers, which allow us to wrap components and have states that can be used from anywhere within those components.  
As you might have realized, our store from [`level 12`](#level-12) is also a type of context.

In order to use a context, we need to wrap the components we want with its provider.  
When creating the provider, we can also add components that will automatically be added when we call it. For example, if we were to add a light/dark mode provider, we can add that it will automatically add a button to switch between the modes on the bottom-right of the screen.

**Tasks:**

1. Create an `AlertProvider` context that manages system-wide alerts (success, error, info, warning).
2. Alerts should:
   - Appear in the bottom-left of the screen.
   - Auto-dismiss after 5 seconds.
   - Dismiss immediately on click.
   - Have a distinct visual indicator per type (icon, color, or both).
   - Animate in/out (slide transition — not abrupt pop-in).
3. Add alerts throughout the app where appropriate (login success/failure, event creation, deletion confirmation, etc.).

---
