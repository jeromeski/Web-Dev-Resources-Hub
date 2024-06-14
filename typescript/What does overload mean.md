My apologies for any confusion! Let me clarify:

In TypeScript, **overloads** refer to multiple function signatures for the same function name. Each signature specifies a different set of parameters and their types. When you call a function, TypeScript determines which overload to use based on the provided arguments. So, overloads define the valid parameter combinations for a function.

For example, consider this TypeScript function with overloads:

```typescript
function greet(name: string): string;
function greet(firstName: string, lastName: string): string;
function greet(firstOrFullName: string, last?: string): string {
  if (last) {
    return `Hello, ${firstOrFullName} ${last}!`;
  } else {
    return `Hello, ${firstOrFullName}!`;
  }
}

const result1 = greet('Alice'); // Uses the first overload
const result2 = greet('Bob', 'Smith'); // Uses the second overload
```

In this example, `greet` has two overloads: one that takes a single `name` parameter and another that takes both `firstName` and `lastName`. TypeScript selects the appropriate overload based on the arguments you provide when calling `greet`.

Feel free to ask if you'd like further clarification or have more questions! 😊👍