Using the [] syntax, objects can be instantiated with keys derived from other variables:

```js
const key = 'test';
const val = 'hugely important';
      
{
  [key]: val
}

// => { test: 'hugely important' }
```
