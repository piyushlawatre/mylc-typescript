## TypeScript Types

### Type Annotations

TypeScript uses type annotations to specify the data types of variables, function parameters, and return types. This helps to ensure type safety and prevent errors during development.

In the code, type annotations are used to declare the types of variables, arrays, objects, and interfaces. For example:

```typescript
let fruityName: string = "Apple";
let orchardIds: number[] = [11250, 68465];
let produceDetails: {
  name: string;
  lastName: string;
  contact: number;
} = {
  name: fruityName,
  lastName: citrusName,
  contact: produceCode,
};
```

### Interfaces

Interfaces are a way to define the structure of objects in TypeScript. They provide a blueprint for objects and ensure that they have the required properties and methods.

In the code, an interface is used to define the structure of the `produceExtraDetails` object:

```typescript
interface IExtraDetails {
  isOrganicProducer: boolean;
  splitFruityName: string[];
}

let produceExtraDetails: IExtraDetails = {
  isOrganicProducer,
  splitFruityName,
};
```

### Record Types

Record types are a way to define the structure of map-like objects in TypeScript. They allow you to specify the types of the keys and values in the object.

In the code, a record type is used to define the structure of the `orchardDetails` object:

```typescript
const orchardDetails: Record<number, { name: string; isRipe: boolean }> = {
  10101: { name: "Apple Orchard", isRipe: true },
  10102: { name: "Citrus Grove", isRipe: true },
};
```

### Nested Record Types

Record types can be nested to create more complex data structures. In the code, a nested record type is used to define the structure of the `produceDetailsByName` array:

```typescript
type produceDetailsByName = Array<Record<string, { description: string }>>;

const produceDetailsByName: produceDetailsByName = [
  { Orchard: { description: "Apple Orchard" } },
  { Grove: { description: "Citrus Grove" } },
];

produceDetailsByName.push({ Farm: { description: "Berry Farm" } });
```

These TypeScript concepts help to make the code more type-safe and prevent errors during development. They also make the code more readable and maintainable.
