# Function Returning a Function

## Concept of Closures

- The code demonstrates the concept of closures.
- It defines a type `IAdderFunction` for a function that takes a number and returns a number:

  ```typescript
  type IAdderFunction = (val: number) => number;
  ```
- The adder function takes a number as an argument and returns an `IAdderFunction`. It creates a closure where the returned function "remembers" the initial value.

  ```typescript
  export function adder(number: number): IAdderFunction {
      return (value: number) => value + number;
  }
  ```
- It creates two instances, test and test2, of the adder function with different initial values:

  ```typescript
  const test = adder(2);
  const test2 = adder(5);
  ```
- It showcases the closure concept by calling the test and test2 functions with different values and logging the results:

  ```typescript
  console.log(test(50)); // Outputs 52 (50 + 2)
  console.log(test(60)); // Outputs 62 (60 + 2)
  console.log(test2(70)); // Outputs 75 (70 + 5)
  ```
