# vitejs-vite-fm6asf

## React - The complete guide - Advanced lessons

- Login and Logout screens - Currently if you refresh after login it will take back to login screen
  -- The reason for this is the useState returns to false for isLoggedIn as default state
  -- Setting up localStorage and useEffect with no dependencies evaluates isLoggedIn sets a persistent 1 time condition
  -- because the dependency doesn't change
  -- Both handlers are updating localStorage

  # Examples of useEffect with and without dependencies

  ## Login.jsx

  ```js
   useEffect(() => {
    setFormIsValid(
      enteredEmail.includes('@') && enteredPassword.trim().length > 6
    );
  }, [enteredEmail, enteredPassword]);
  ```

  ## App.jsx

  ```js
   useEffect(() => {
    const storedUserLoginInformation = localStorage.getItem('isLoggedIn');

    if (storedUserLoginInformation === '1') {
      setIsLoggedIn(true);
    }
  }, []);

  const loginHandler = (email, password) => {
    // We should of course check email and password
    // But it's just a dummy/ demo anyways
    localStorage.setItem('isLoggedIn', '1');
    setIsLoggedIn(true);
  };

  const logoutHandler = () => {
    localStorage.removeItem('isLoggedIn');
    setIsLoggedIn(false);
  };
  ```

[Edit on StackBlitz ⚡️](https://stackblitz.com/edit/vitejs-vite-fm6asf)
