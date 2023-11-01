# Understanding Type Enforcement

## Type Checking in TypeScript

- TypeScript performs type checking at **compile time**, not at runtime.
- Avoids runtime type checking due to its high cost.
- Ensure type safety at **interface points** when using both TypeScript and JavaScript.

## Optional Chaining Operator

- Use the **optional chaining operator (`?`)** to safely access object properties and prevent referencing undefined variables.

## Null Coalescing Operator

- The **null coalescing operator (`??`)** returns a default value if a variable is undefined.

# Runtime Type Checking in TypeScript

- Perform runtime type checking by validating the structure of an object passed to a function.

```typescript
export function blendFruityName(fruityValue: { firstName: string; lastName: string }): string {
  return `${fruityValue?.firstName ?? 'apple'} ${fruityValue?.lastName ?? 'crunchy'}`;
}
```

- The code uses the optional chaining operator (?.) to safely access object properties.
- Provides fallback values if fruityValue or its properties are undefined.
- Uses `apple` as a fallback for firstName and `crunchy` for `lastName`.
