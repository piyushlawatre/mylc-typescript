## TypeScript Concepts in the Code

### Defining Functions in TypeScript

In TypeScript, functions can be defined using the `function` keyword.

```typescript
function blendTwoFruits(fruityOne: number, fruityTwo: number): number {
    return fruityOne + fruityTwo;
}
```
Module Exports and TypeScript
Module exports using module.exports are not compatible with TypeScript.
```typescript
// module.exports = blendTwoFruits
// 🚫 Module exports aren't compatible with TypeScript. 🚫
```
Exporting Functions Using export
To make functions or variables accessible in TypeScript, use the export keyword.
```typescript
export default blendTwoFruits;
```
The export default syntax is used to export functions, like blendTwoFruits, in a TypeScript-friendly manner.
This allows the function to be accessible for use in other modules.


### Type Annotations

TypeScript uses type annotations to specify the data types of variables, function parameters, and return types. This helps to ensure type safety and prevent errors during development.

In the code, type annotations are used to declare the types of variables, function parameters, and return types. For example:

```typescript
function blendTwoFruits(fruityOne: number, fruityTwo: number): number {
  return fruityOne + fruityTwo;
}

export const harvestFruit = (fruitTree: string): Promise<string> => {
  return Promise.resolve(`Ripe fruit from the ${fruitTree}`);
};
```

This function takes two parameters, `fruityOne` and `fruityTwo`, both of which are of type `number`. The function also has a return type of `number`, indicating that it will return a numerical value.

### Default Parameter Values

TypeScript allows you to specify default values for function parameters. This means that if a parameter is not provided when the function is called, the default value will be used instead.

In the code, the `combineFruityStrings` function has a default value for its second parameter:

```typescript
export const combineFruityStrings = (fruityStringOne: string, fruityStringTwo: string = 'pineapple'): string => {
  return `${fruityStringOne} ${fruityStringTwo}`;
};
```
This means that if the second parameter is not provided when the function is called, the value `pineapple` will be used instead.


### Union Types
Union types in TypeScript allow a variable to hold values of different types. This is useful when a variable can be one of several different types.
In the code, the `blendFruityValues` function uses a union type for its second parameter:

```typescript
export const blendFruityValues = (fruityValueOne: number, fruityValueTwo: number | string): string => {
  return `${fruityValueOne} ${fruityValueTwo}`;
};
```
This means that the `fruityValueTwo` parameter can be either a number or a string.

### Void Types
The void type in TypeScript indicates that a function does not return a value. In the code, the `fruityVoidExample` function has a return type of `void`:

```typescript
export const fruityVoidExample = (fruityObject: object): void => {
  console.log('🍊 Fruity Void Object: 🍎', fruityObject);
};

```
