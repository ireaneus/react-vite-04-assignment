# vitejs-vite-fm6asf

## React - The complete guide - Advanced lessons

- Login and Logout screens - Currently if you refresh after login it will take back to login screen
  -- The reason for this is the useState returns to false for isLoggedIn as default state
  -- Setting up localStorage and useEffect with no dependencies evaluates isLoggedIn sets a persistent 1 time condition
  -- because the dependency doesn't change
  -- Both handlers are updating localStorage

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/vitejs-vite-fm6asf)
