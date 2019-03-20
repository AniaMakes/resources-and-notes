### Go through an object and replace values if the current value meets a condition (eg replace values of `null` with and empty string)

```
const initialValues = Object.keys(initialValuesWithNulls).reduce((acc, current) => {
    if (initialValuesWithNulls[current] === null) {
        acc[current] = '';
    } else {
        acc[current] = initialValuesWithNulls[current];
    }
    return acc;
}, {});
```