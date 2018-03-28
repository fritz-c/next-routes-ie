<img width="941" alt="error" src="https://user-images.githubusercontent.com/4413963/38013317-b345a528-329f-11e8-89bd-89891ad2db96.png">

------------

_A minimal implementation of a next.js app with `next-routes` to demonstrate `next-routes` error in IE 11._

### How to reproduce:

* Run the following:
  ```
  git clone git@github.com:fritz-c/next-routes-ie.git
  cd next-routes-ie
  npm install
  npm run build && npm start
  ```
* Open http://localhost:3000 in IE 11
* Look in the developer tools (F12) for the error

### Explanation
The `next-routes` code makes a call to `Object.assign`, which is not available in IE 11. `next-routes` up to `v1.2.0` was safe, presumably due to a more broadly polyfilled `next/babel` configuration.
