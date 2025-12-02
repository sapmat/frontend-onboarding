# Frontend Onboarding

Welcome!
This exercise is designed to introduce you step-by-step to the fundamentals of frontend development, primarily using React.

NOTE:
This does not cover everything about frontend development, but it will give you enough understanding to begin creating your own features and improving independently.

------------------------------------------------------------
LEVELS NAVIGATION
------------------------------------------------------------

- [Level 1 – Start](#level-1)
- [Level 2 – States](#level-2)
- [Level 3 – Styling (Emotion)](#level-3)
- [Level 4 – Routes](#level-4)
- [Level 5 – Mock API](#level-5)
- [Level 6 – Table Data](#level-6)

------------------------------------------------------------
<a id="level-1"></a> LEVEL 1 – START
------------------------------------------------------------

We will begin very simple by creating a login page.

TODO:
- Create a basic Login page with:
  - An input for email
  - An input for password
  - A submit button
- No hooks, no styling yet.

------------------------------------------------------------
<a id="level-2"></a>LEVEL 2 – STATES
------------------------------------------------------------

React provides hooks like useState to easily handle component state.

TODO:
- Create a mock data file containing a few users.
- Using useState, when the submit button is clicked:
  - If login data matches a user in mock data → show success message
  - Otherwise → show error message
- Display the message under the submit button.

------------------------------------------------------------
<a id="level-3"></a> LEVEL 3 – STYLING (EMOTION)
------------------------------------------------------------

Now add styling using Emotion.

TODO:
- Create a styling file using Emotion.
- Add styling to your login page.

------------------------------------------------------------
<a id="level-4"></a> LEVEL 4 – ROUTES
------------------------------------------------------------

Create a second page in your application and navigate between pages.

TODO:
- Create a Home page:
  - Header with a hello message and a Logout button
  - Main content (empty for now)
- Style the page with natural, matching colors.

------------------------------------------------------------
<a id="level-5"></a> LEVEL 5 – MOCK API
------------------------------------------------------------

Your project will revolve around events. Since there's no backend, you'll build a simple mock API.

NOTE:
Keep your mock API simple. It only needs to provide your UI with usable data.

TODO:
- Add additional fields to each user (e.g. username, job, location, etc.)
- Create a mock db for user events.
  Each event should include:
    - id
    - name
    - time
    - host:
        - id
        - username
    - attendees[]:
        - id
        - rating
- Create a service file for each mock data file.
- Create a function to validate user credentials during login.

------------------------------------------------------------
<a id="level-6"></a> LEVEL 6 – TABLE DATA
------------------------------------------------------------

Learn how to display and manipulate data in a table.

TODO:
- Create a Table component that displays all events.
- Ensure that if the table body becomes long, the body scrolls while the header stays fixed.
- Create a Filter component to filter table rows.
- Add a Clear button to reset all filters.
