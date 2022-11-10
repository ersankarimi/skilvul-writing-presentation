# Materi Minggu 8

## Daftar Isi

1. [React Context](#react-context)
2. [React Testing](#react-testing)

<br>

## React Context

Context menyediakan cara untuk membagi data yang dapat diakses oleh banyak
komponen tanpa harus mengirimkan props secara manual ke setiap level. Context
dapat digunakan untuk mengatasi masalah yang sering terjadi dalam React, seperti
prop drilling dan membagi state yang berbeda antar komponen.

### Membuat Context

Context dapat dibuat dengan menggunakan `React.createContext()`. Context ini
dapat digunakan untuk menyimpan data yang dapat diakses oleh komponen-komponen
yang berada di dalamnya.

```jsx
import React from "react";

const UserContext = React.createContext();

export default UserContext;
```

### Menggunakan Context

Context dapat digunakan dengan menggunakan `Context.Provider` dan
`Context.Consumer`. `Context.Provider` digunakan untuk menyediakan data yang
dapat diakses oleh komponen-komponen yang berada di dalamnya. `Context.Consumer`
digunakan untuk mengakses data yang disediakan oleh `Context.Provider`.

```jsx
import React from "react";
import UserContext from "./UserContext";

const User = () => {
  return (
    <UserContext.Provider value={{ name: "John Doe" }}>
      <div>
        <h1>User</h1>
        <Profile />
      </div>
    </UserContext.Provider>
  );
};

const Profile = () => {
  return (
    <div>
      <h2>Profile</h2>
      <Name />
    </div>
  );
};

const Name = () => {
  return (
    <UserContext.Consumer>{({ name }) => <p>{name}</p>}</UserContext.Consumer>
  );
};

export default User;
```

### Menggunakan Hooks

Context juga dapat digunakan dengan menggunakan Hooks. `useContext()` digunakan
untuk mengakses data yang disediakan oleh `Context.Provider`.

```jsx
import React, { useContext } from "react";
import UserContext from "./UserContext";

const User = () => {
  return (
    <UserContext.Provider value={{ name: "John Doe" }}>
      <div>
        <h1>User</h1>
        <Profile />
      </div>
    </UserContext.Provider>
  );
};

const Profile = () => {
  return (
    <div>
      <h2>Profile</h2>
      <Name />
    </div>
  );
};

const Name = () => {
  const { name } = useContext(UserContext);

  return <p>{name}</p>;
};

export default User;
```

### Membuat Custom Hooks

Custom Hooks dapat dibuat untuk mempermudah penggunaan Context. Custom Hooks
dapat dibuat dengan menggunakan `useContext()`.

```jsx
import { useContext } from "react";
import UserContext from "./UserContext";

const useUser = () => useContext(UserContext);

export default useUser;
```

Custom Hooks dapat digunakan seperti ini:

```jsx
import React from "react";
import useUser from "./useUser";

const User = () => {
  return (
    <UserContext.Provider value={{ name: "John Doe" }}>
      <div>
        <h1>User</h1>
        <Profile />
      </div>
    </UserContext.Provider>
  );
};

const Profile = () => {
  return (
    <div>
      <h2>Profile</h2>
      <Name />
    </div>
  );
};

const Name = () => {
  const { name } = useUser();

  return <p>{name}</p>;
};

export default User;
```

<br>

## React Testing

React Testing Library menyediakan cara untuk melakukan testing pada komponen
React. React Testing Library dapat digunakan untuk melakukan testing pada
komponen React tanpa harus menguji implementasi detail dari komponen tersebut.
React Testing Library dapat digunakan untuk melakukan testing pada komponen
React tanpa harus menguji implementasi detail dari komponen tersebut.

### Menginstall React Testing Library

React Testing Library dapat diinstall dengan menggunakan `npm` atau `yarn`.

```bash
npm install --save-dev @testing-library/react
```

```bash
yarn add --dev @testing-library/react
```

### Menginstall Jest

Jest adalah library yang digunakan untuk melakukan testing pada JavaScript. Jest
dapat diinstall dengan menggunakan `npm` atau `yarn`.

```bash
npm install --save-dev jest
```

```bash
yarn add --dev jest
```

### Menginstall Jest DOM

Jest DOM menyediakan cara untuk melakukan testing pada DOM. Jest DOM dapat
diinstall dengan menggunakan `npm` atau `yarn`.

```bash
npm install --save-dev @testing-library/jest-dom
```

```bash
yarn add --dev @testing-library/jest-dom
```

### Setup Testing

Untuk melakukan testing pada React, kita perlu melakukan setup pada file
`jest.config.js`.

```js
module.exports = {
  setupFilesAfterEnv: ["@testing-library/jest-dom/extend-expect"],
};
```

### Setup Testing pada Create React App

Untuk melakukan testing pada React yang dibuat dengan Create React App, kita
perlu melakukan setup pada file `src/setupTests.js`.

```js
import "@testing-library/jest-dom/extend-expect";
```

### Membuat Test

Test dapat dibuat dengan menggunakan `test()` atau `it()`.

```jsx
import React from "react";
import { render } from "@testing-library/react";
import App from "./App";

test("renders learn react link", () => {
  const { getByText } = render(<App />);
  const linkElement = getByText(/learn react/i);
  expect(linkElement).toBeInTheDocument();
});
```

### Membuat Mock

Mock dapat dibuat dengan menggunakan `jest.fn()`.

```jsx
import React from "react";
import { render } from "@testing-library/react";
import App from "./App";

test("renders learn react link", () => {
  const mock = jest.fn();
  const { getByText } = render(<App />);
  const linkElement = getByText(/learn react/i);
  expect(linkElement).toBeInTheDocument();
});
```

### Membuat Snapshot

Snapshot dapat dibuat dengan menggunakan `toMatchSnapshot()`.

```jsx
import React from "react";
import { render } from "@testing-library/react";
import App from "./App";

test("renders learn react link", () => {
  const mock = jest.fn();
  const { getByText } = render(<App />);
  const linkElement = getByText(/learn react/i);
  expect(linkElement).toBeInTheDocument();
  expect(linkElement).toMatchSnapshot();
});
```
