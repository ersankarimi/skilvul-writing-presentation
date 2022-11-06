# Materi Minggu 7

## Daftar Isi

1. [React Router](#react-router)
2. [Redux](#redux)

<br>

## React Router v6

React Router v6 adalah library yang digunakan untuk membuat routing pada
aplikasi React. React Router v6 merupakan versi terbaru dari React Router yang
sebelumnya adalah React Router v5. React Router v6 memiliki beberapa perubahan
yang cukup signifikan dibandingkan dengan versi sebelumnya. Perubahan tersebut
antara lain:

1. React Router v6 menggunakan konsep hooks untuk membuat routing. Hal ini
   berbeda dengan React Router v5 yang menggunakan komponen-komponen seperti
   `<BrowserRouter>`, `<Route>`, dan `<Link>`.
2. React Router v6 menggunakan konsep declarative routing. Hal ini berbeda
   dengan React Router v5 yang menggunakan konsep imperative routing.
3. React Router v6 menggunakan konsep lazy loading untuk memuat
   komponen-komponen yang ada pada routing. Hal ini berbeda dengan React Router
   v5 yang menggunakan konsep eager loading.
4. React Router v6 menggunakan konsep dynamic routing. Hal ini berbeda dengan
   React Router v5 yang menggunakan konsep static routing.
5. React Router v6 menggunakan konsep nested routing. Hal ini berbeda dengan
   React Router v5 yang menggunakan konsep flat routing.
6. React Router v6 menggunakan konsep route parameters. Hal ini berbeda dengan
   React Router v5 yang menggunakan konsep query parameters.
7. React Router v6 menggunakan konsep route config. Hal ini berbeda dengan React
   Router v5 yang menggunakan konsep route props.
8. React Router v6 menggunakan konsep route object. Hal ini berbeda dengan React
   Router v5 yang menggunakan konsep route component.
9. React Router v6 menggunakan konsep route hooks. Hal ini berbeda dengan React
   Router v5 yang menggunakan konsep route components.

Dan masih banyak lagi perbedaan-perbedaan lainnya antara React Router v6 dengan
React Router v5. Untuk lebih jelasnya, silahkan baca dokumentasi React Router v6
di [sini](https://reactrouter.com/docs/en/v6/getting-started/overview).

### Instalasi

Untuk menginstall React Router v6, jalankan perintah berikut pada terminal:

```bash
npm install react-router-dom -S
```

### Penggunaan

Untuk menggunakan React Router v6, kita perlu mengimport beberapa komponen dari
library tersebut. Komponen-komponen tersebut antara lain:

1. `BrowserRouter` - Komponen ini digunakan untuk membuat routing pada aplikasi
   React.
2. `Routes` - Komponen ini digunakan untuk membuat routing pada aplikasi React.
3. `Route` - Komponen ini digunakan untuk membuat routing pada aplikasi React.
4. `Link` - Komponen ini digunakan untuk membuat link pada aplikasi React.
5. `Outlet` - Komponen ini digunakan untuk membuat routing pada aplikasi React.
6. `useNavigate` - Komponen ini digunakan untuk membuat routing pada aplikasi
   React.
7. `useParams` - Komponen ini digunakan untuk membuat routing pada aplikasi
   React.
8. `useLocation` - Komponen ini digunakan untuk membuat routing pada aplikasi
   React.
9. `useMatch` - Komponen ini digunakan untuk membuat routing pada aplikasi
   React.
10. `useRoutes` - Komponen ini digunakan untuk membuat routing pada aplikasi
    React.
11. `useHistory` - Komponen ini digunakan untuk membuat routing pada aplikasi
    React.

Dan masih banyak lagi komponen-komponen lainnya yang dapat digunakan untuk
membuat routing pada aplikasi React. Untuk lebih jelasnya, silahkan baca
dokumentasi React Router v6 di
[sini](https://reactrouter.com/docs/en/v6/getting-started/overview).

Berikut ini adalah contoh penggunaan React Router v6 pada aplikasi React:

```jsx
import React from "react";
import { BrowserRouter, Routes, Route, Link, Outlet } from "react-router-dom";

const Home = () => {
  return (
    <div>
      <h1>Home</h1>
    </div>
  );
};

const About = () => {
  return (
    <div>
      <h1>About</h1>
    </div>
  );
};

const Users = () => {
  return (
    <div>
      <h1>Users</h1>
      <Outlet />
    </div>
  );
};

const UsersList = () => {
  return (
    <div>
      <h1>Users List</h1>
    </div>
  );
};

const UsersDetail = () => {
  return (
    <div>
      <h1>Users Detail</h1>
    </div>
  );
};

const App = () => {
  return (
    <BrowserRouter>
      <nav>
        <ul>
          <li>
            <Link to="/">Home</Link>
          </li>
          <li>
            <Link to="about">About</Link>
          </li>
          <li>
            <Link to="users">Users</Link>
          </li>
        </ul>
      </nav>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="about" element={<About />} />
        <Route path="users" element={<Users />}>
          <Route path="/" element={<UsersList />} />
          <Route path=":id" element={<UsersDetail />} />
        </Route>
      </Routes>
    </BrowserRouter>
  );
};

export default App;
```

### Referensi

1. [React Router v6](https://reactrouter.com/docs/en/v6/getting-started/overview)
2. [React Router v5](https://reactrouter.com/docs/en/v5/getting-started/overview)
3. [React Router v6 vs React Router v5](https://reactrouter.com/docs/en/v6/upgrading/v5)

## Redux

### Pengenalan

Redux adalah library JavaScript yang digunakan untuk mengelola state pada
aplikasi React. Redux memiliki beberapa kelebihan antara lain:

1. Redux memudahkan kita untuk mengelola state pada aplikasi React.
2. Redux memudahkan kita untuk mengelola state pada aplikasi React yang
   kompleks.
3. Redux memudahkan kita untuk mengelola state pada aplikasi React yang berskala
   besar.
4. Redux memudahkan kita untuk mengelola state pada aplikasi React yang berskala
   besar dan kompleks.
5. Redux memudahkan kita untuk mengelola state pada aplikasi React yang berskala
   besar dan kompleks dengan banyak pengguna.

### Instalasi

Untuk menginstall Redux, jalankan perintah berikut pada terminal:

```bash
npm install redux react-redux -S
```

### Penggunaan

Untuk menggunakan Redux, kita perlu mengimport beberapa komponen dari library
tersebut. Komponen-komponen tersebut antara lain:

1. `Provider` - Komponen ini digunakan untuk membuat store pada aplikasi React.
2. `useSelector` - Komponen ini digunakan untuk mengambil state dari store pada
   aplikasi React.
3. `useDispatch` - Komponen ini digunakan untuk mengirimkan action ke store pada
   aplikasi React.
4. `createStore` - Komponen ini digunakan untuk membuat store pada aplikasi
   React.
5. `combineReducers` - Komponen ini digunakan untuk menggabungkan beberapa
   reducer pada aplikasi React.
6. `createAction` - Komponen ini digunakan untuk membuat action pada aplikasi
   React.
7. `createReducer` - Komponen ini digunakan untuk membuat reducer pada aplikasi
   React.
8. `createAsyncThunk` - Komponen ini digunakan untuk membuat action pada
   aplikasi React.

Dan masih banyak lagi komponen-komponen lainnya yang dapat digunakan untuk
membuat store pada aplikasi React. Untuk lebih jelasnya, silahkan baca
dokumentasi Redux di [sini](https://redux.js.org/introduction/getting-started).

Berikut ini adalah contoh penggunaan Redux pada aplikasi React:

```jsx
import React from "react";
import {
  Provider,
  useSelector,
  useDispatch,
  createStore,
  combineReducers,
  createAction,
  createReducer,
  createAsyncThunk,
} from "react-redux";

const initialState = {
  count: 0,
};

const increment = createAction("INCREMENT");
const decrement = createAction("DECREMENT");

const counterReducer = createReducer(initialState, {
  [increment]: (state) => {
    return {
      ...state,
      count: state.count + 1,
    };
  },
  [decrement]: (state) => {
    return {
      ...state,
      count: state.count - 1,
    };
  },
});

const store = createStore(combineReducers({ counter: counterReducer }));

const Counter = () => {
  const count = useSelector((state) => state.counter.count);
  const dispatch = useDispatch();

  return (
    <div>
      <h1>Counter</h1>
      <p>{count}</p>
      <button onClick={() => dispatch(increment())}>+</button>
      <button onClick={() => dispatch(decrement())}>-</button>
    </div>
  );
};

const App = () => {
  return (
    <Provider store={store}>
      <Counter />
    </Provider>
  );
};

export default App;
```

### Redux Thunk

Redux Thunk adalah middleware yang digunakan untuk mengelola action pada Redux.
Redux Thunk memiliki beberapa kelebihan antara lain:

1. Redux Thunk memudahkan kita untuk mengelola action pada Redux.
2. Redux Thunk memudahkan kita untuk mengelola action pada Redux yang kompleks.
3. Redux Thunk memudahkan kita untuk mengelola action pada Redux yang berskala
   besar.

### Instalasi

Untuk menginstall Redux Thunk, jalankan perintah berikut pada terminal:

```bash
npm install redux-thunk -S
```

### Penggunaan

Untuk menggunakan Redux Thunk, kita perlu mengimport beberapa komponen dari
library tersebut. Komponen-komponen tersebut antara lain:

1. `applyMiddleware` - Komponen ini digunakan untuk mengaktifkan middleware pada
   Redux.
2. `thunk` - Komponen ini digunakan untuk mengaktifkan middleware pada Redux.
3. `createAsyncThunk` - Komponen ini digunakan untuk membuat action pada
   aplikasi React.

Berikut ini adalah contoh penggunaan Redux Thunk pada aplikasi React:

```jsx
import React from "react";
import {
  Provider,
  useSelector,
  useDispatch,
  createStore,
  combineReducers,
  createAction,
  createReducer,
  applyMiddleware,
  thunk,
  createAsyncThunk,
} from "react-redux";

const initialState = {
  count: 0,
};

const thunkIncrement = createAsyncThunk("THUNK_INCREMENT", (payload) => {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve(payload);
    }, 1000);
  });
});

const thunkDecrement = createAsyncThunk("THUNK_DECREMENT", (payload) => {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve(payload);
    }, 1000);
  });
});

const counterReducer = createReducer(initialState, {
  [thunkIncrement.fulfilled]: (state, action) => {
    return {
      ...state,
      count: state.count + action.payload,
    };
  },
  [thunkDecrement.fulfilled]: (state, action) => {
    return {
      ...state,
      count: state.count - action.payload,
    };
  },
});

const store = createStore(
  combineReducers({ counter: counterReducer }),
  applyMiddleware(thunk)
);

const Counter = () => {
  const count = useSelector((state) => state.counter.count);
  const dispatch = useDispatch();

  return (
    <div>
      <h1>Counter</h1>
      <p>{count}</p>
      <button onClick={() => dispatch(thunkIncrement(1))}>+</button>
      <button onClick={() => dispatch(thunkDecrement(1))}>-</button>
    </div>
  );
};

const App = () => {
  return (
    <Provider store={store}>
      <Counter />
    </Provider>
  );
};

export default App;
```
