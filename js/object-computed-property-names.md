Using the [] syntax, objects can be instantiated with keys derived from other variables:

```js
const key = 'test';
const val = 'hugely important';
      
{
  [key]: val
}

// => { test: 'hugely important' }
```

See computed property names from ES2015 notes in MDN: https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Operators/Object_initializer#Computed_property_names
