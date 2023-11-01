# TypeScript Functions with Functions

## Callback Functions

- Define a type for a callback function `IMutationFunction`, which takes a number and returns a number:

  ```typescript
  type IMutator = (v: number) => string;
  ```

- Create a function arrayMutate that takes an array of numbers and a callback function. It maps the callback function to each element in the array:

  ```typescript
  export function arrayMutator(arrNumbers: number[], mutator: IMutator): string[] {
    return arrNumbers.map(mutator);
  }  
  ```
- Utilize the IMutationFunction to define a new callback function myNewMutateFunction:

   ```typescript
  const stringify: IMutator = (v: number) => `${v}`;
  const prefixToId: IMutator = (v: number) => `NDAS-${v}`;
   ```
- Invoking `IMutationFunction`

   ```typescript
  // arrayMutator([10, 20, 30], stringify) -> [ '10', '20', '30' ] 
  // arrayMutator([10, 20, 30], prefixToId) -> [ 'NDAS-10', 'NDAS-20', 'NDAS-30' ]
   ```
