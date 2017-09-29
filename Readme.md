Custom errors

## Error

```js
var errorObject = require("error-object")

function doSomethingBad() {
  throw new errorObject('It went bad!', {
    errorCode: 1,
    foo: "bar",
    obj: {

    },
    // ...
  });
}

try {
  doSomethingBad()
} catch (e) {
  console.error(err.message);
  console.error(err.extra.errorCode);
  console.error(err.extra.foo);
  console.error(err.extra.obj);
} finally {

}
```
