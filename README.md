# Redux Saga Snippets

## Features
`exaction →` 
```js 
// input
export const get_foo = "get_foo";
// output
export const GET_FOO = "GET_FOO";
```

`reaction → `
```js
// input
export function get_foo(foo, bar,) {
    return {
        foo, bar,
        type: get_foo
    };
};
// output
export function getFoo(foo, bar) {
    return {
        foo,
		bar,
        type: GET_FOO,
    };
};
```

`saga → `
```js
export function* callFoo() {
    while (true) {
        const { payload } = yield take(ACTION);
        
    }
}
```


|      Prefix | Method   |
| ----------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|      `yp →` | ```yield put({ payload, type: ACTION });``` |
|      `yc →` | `yield call(() => func());` |
|      `cyc →` | `const res = yield call(() => func());` |
|      `cys →` | `const selector = yield select((state) => state.property);` |
|      `cyt →` | `const { payload } = yield take(ACTION);` |

## Release Notes
Feel to free to fork my [repo](https://github.com/alexkev/clg) and if I like it I'll merge it in.

## Enjoy!

Support Open Source Code by buying me a drink ⚡🥤 😉.

[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_donations&business=axel720%40gmail.com&currency_code=USD&source=url)