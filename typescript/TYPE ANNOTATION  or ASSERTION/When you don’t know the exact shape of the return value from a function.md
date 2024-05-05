When you don't know the exact shape of the return value from a function, you have a few options for type annotations in TypeScript. Let's explore them:

1. **Use `any`**:
   - The simplest approach is to annotate the return type as `any`. However, this provides minimal type safety and loses the benefits of TypeScript's static type checking.
   - Example:
     ```typescript
     function mysteryFunction(): any {
         // Implementation details...
     }
     ```

2. **Use `unknown`**:
   - A better alternative is to use the `unknown` type. It represents a value whose type we don't know yet.
   - You can later narrow down the type using type guards or type assertions.
   - Example:
     ```typescript
     function unknownFunction(): unknown {
         // Implementation details...
     }
     ```

3. **Use Union Types**:
   - If you have a limited set of possible return types, use a union type.
   - Example:
     ```typescript
     function foo(): string | number {
         // Implementation details...
     }
     ```

4. **Use Generics**:
   - If the return type depends on input parameters, consider using generics.
   - Example:
     ```typescript
     function identity<T>(value: T): T {
         return value;
     }
     ```

5. **Use `void` or `never`**:
   - If the function never returns (e.g., it always throws an error), use `never`.
   - If the function doesn't return anything (like a logging function), use `void`.
   - Example:
     ```typescript
     function logMessage(message: string): void {
         console.log(message);
     }

     function throwError(errorMsg: string): never {
         throw new Error(errorMsg);
     }
     ```

Remember that choosing the right annotation depends on your specific use case. If possible, aim for more precise types to benefit from TypeScript's type checking. 😊

²: [Function and Return Type Annotations in TypeScript](https://www.slingacademy.com/article/function-and-return-type-annotations-in-typescript/)
⁵: [TypeScript Return Type Annotations](https://www.geeksforgeeks.org/typescript-return-type-annotations/)
⁶: [TypeScript Function Annotations](https://dev.to/spukas/typescript-function-annotations-7c4)
⁷: [Type Annotations in TypeScript](https://www.tektutorialshub.com/typescript/type-annotation-in-typescript/)
⁸: [TypeScript: Documentation - More on Functions](https://www.typescriptlang.org/docs/handbook/2/functions.html)

Source: Conversation with Bing, 5/3/2024
(1) Function and Return Type Annotations in TypeScript. https://bing.com/search?q=annotate+unknown+return+type+of+function.
(2) TypeScript Return Type Annotations - GeeksforGeeks. https://www.geeksforgeeks.org/typescript-return-type-annotations/.
(3) TypeScript Function Annotations - DEV Community. https://dev.to/spukas/typescript-function-annotations-7c4.
(4) Type Annotations in TypeScript - TekTutorialsHub. https://www.tektutorialshub.com/typescript/type-annotation-in-typescript/.
(5) TypeScript: Documentation - More on Functions. https://www.typescriptlang.org/docs/handbook/2/functions.html.
(6) How to annotate types of multiple return values? - Stack Overflow. https://stackoverflow.com/questions/40181344/how-to-annotate-types-of-multiple-return-values.
(7) Function and Return Type Annotations in TypeScript. https://www.slingacademy.com/article/function-and-return-type-annotations-in-typescript/.
(8) Annotate a function return type with an instance, not a type. https://stackoverflow.com/questions/77953145/annotate-a-function-return-type-with-an-instance-not-a-type.
(9) en.wikipedia.org. https://en.wikipedia.org/wiki/TypeScript.