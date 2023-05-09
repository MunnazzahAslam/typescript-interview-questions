# typescript-interview-questions

| No. | Questions |
| --- | --------- |
| 1.  | What is TypeScript, and why would I use it in place of JavaScript? |
| 2.  | What are the difference beetween Typescript and JavaScript? |
| 3.  | Do we need to compile TypeScript files and why? |
| 4.  | What is the purpose of the tsconfig.json file? |
| 5.  | What are the Benefits of using TypeScript? |
| 6.  | What are the Disadvantages of TypeScript? |
| 7.  | What are the Components of TypeScript? |
| 8.  | What is Interface in TypeScript? |
| 9.  | What is the difference between Classes and Interfaces in Typescript? |
| 10. | When to use interfaces and when to use classes in TypeScript? |
| 11. | Explain generics in TypeScript? |
| 12. | What is "Decorators" in TypeScript? |
| 13. | Does TypeScript support all object oriented principles? |
| 14. | Which object oriented terms are supported by TypeScript? |
| 15.	| What are the primitive types in TypeScript? |
| 16.	|	What is any type, and when to use it? |
| 17.	|	What is void, and when to use the void type? |
| 18.	|	What is an unknown type, and when to use it in TypeScript? |
| 19.	|	What are the different keywords to declare variables in TypeScript? |
| 20.	|	What is the Function type in TypeScript? |
| 21.	|	How to create objects in TypeScript? |
| 22. | Explain the different variants of the for loop in TypeScript. |
| 23. | Explain the symbol type in TypeScript. |
| 24. | Explain how optional chaining works in TypeScript. |
| 25. | Provide the TypeScript syntax to create function overloads. |
| 26. | What is meant by type inference? |
| 27. | What is meant by contextual typing? |
| 28. | What is the purpose of noImplicitAny? |
| 29. | What is an interface? |
| 30. | Explain the various ways to control member visibility in TypeScript. |
| 31. | Does TypeScript support static classes? If not, why? |
| 32. | What are abstract classes? When should you use one? |
| 33. | What are anonymous functions? Provide their syntax in TypeScript. |
| 34. | What are union types in TypeScript? |
| 35. | What are intersection types? |
| 36. | What are type aliases? How do you create one? |
| 37. | Explain the tuple types in TypeScript. |
| 38. | Explain how tuple destructuring works in TypeScript. |
| 39. | What are type assertions in TypeScript? |
| 40. | How to enforce strict null checks in TypeScript? |
| 41. | How to make object properties immutable in TypeScript? (hint: readonly) |
| 42. | What is a type declaration file? |
| 43. | What are triple-slash directives? |
| 44. | Explain the purpose of the ‘in’ operator. |
| 45. | What are the ‘implements’ clauses in TypeScript? |
| 46. | What are string literal types? |
| 47. | What are template literal types? |
| 48. | Explain the concept of inheritance in TypeScript. |
| 49. | What are conditional types? How do you create them? |
| 50. | List some of the utility types provided by TypeScript and explain their usage. |

# 1. What is TypeScript, and why would I use it in place of JavaScript?

- TypeScript is a superset of JavaScript with static typing (type checking is done at compile time and you to declare the data types of your variables before you use them), classes and interfaces.
- It allows for better error-spotting in IDEs.
- It can lead to more robust software in large projects while still being deployable like regular JavaScript.

---

# 2. What are the difference beetween Typescript and JavaScript?

| Typescript | Javascript |
| --- | --------- |
|  TypeScript is an Object-Oriented language | JavaScript is a Scripting language |
|  It has Static typing | It does not have static typing |
|  TypeScript gives support for modules | JavaScript does not support modules |
|  It supports optional parameter function | It does not support optional parameter function |

---

# 3. Do we need to compile TypeScript files and why? 

Yes we do. Typescript is just a language Extension browsers can't interpret it. Converting from TypeScript to JavaScript is called compiling. Compiling doesn't mean binary code is created in this case. For this kind of translation, also the term transpilation is used instead of compilation (Compiling is the process of taking source code written in one language and transforming it into another. Transpiling is the process of taking source code written in one language and transforming it into another language that has a similar level of abstraction).

---

# 4. What is the purpose of the tsconfig.json file?

A tsconfig.json file in a directory marks that directory as the root of a TypeScript project. It provides the compiler options to compile the project.

---

# 5. What are the Benefits of using TypeScript?

Easier to debug, quicker development

---

# 6. What are the Disadvantages of TypeScript?

More initial setup, additional learning on top of JavaScript required

---

# 7. What are the Components of TypeScript?

There are three different types of components in TypeScript which includes:

- Language − It comprises of the syntax, keywords, and type annotations.

- The TypeScript Compiler − This compiler (tsc) converts the instructions written in TypeScript to its JavaScript equivalent.

- The TypeScript Language Service − The Language Service exposes an additional layer around the core compiler pipeline, editor-like applications. The language service supports the common set of typical editor operations.

---

# 8. What is Interface in TypeScript?

One of TypeScript’s core principles is that type-checking focuses on the shape that values have.

An interface is a virtual structure that only exists within the context of TypeScript. The TypeScript compiler uses interfaces solely for type-checking purposes.

When you define your interface you’re saying that any object (not an instance of a class) given this contract must be an object containing interfaces properties.

---

# 9. What is the difference between Classes and Interfaces in Typescript?

A class defines a blueprint of what an object should look like and act like and then implements that blueprint by initialising class properties and defining methods. Classes are present throughout all the phases of our code.

Unlike classes, an interface is a virtual structure that only exists within the context of TypeScript. The TypeScript compiler uses interfaces solely for type-checking purposes. Once code is transpiled to its target language, it will be stripped from interfaces.

A class may define a factory or a singleton by providing initialisation to its properties and implementation to its methods, an interface is simply a structural contract that defines what the properties of an object should have as a name and as a type.

---

# 10. When to use interfaces and when to use classes in TypeScript?

If you want to create a custom object instance with the advantages of type-checking for things like arguments, return types, or generics, you should use a class. But if you don't need to create instances, you can use interfaces. Interfaces don't generate any source code, but allow you to virtually type-check your code.

---

# 11. Explain generics in TypeScript?

Generics are able to create a component or function to work over a variety of types rather than a single one.

/** A class definition with a generic parameter */
class Queue<T> {
  private data = [];
  push = (item: T) => this.data.push(item);
  pop = (): T => this.data.shift();
}

const queue = new Queue<number>();
queue.push(0);
queue.push("1"); // ERROR : cannot push a string. Only numbers allowed

---

# 12. What is "Decorators" in TypeScript?

A Decorator is a special kind of declaration that can be attached to a class declaration, method, accessor, property, or parameter. Decorators are functions that take their target as the argument. With decorators we can run arbitrary code around the target execution or even entirely replace the target with a new definition.
  
---
  

# 13. Does TypeScript support all object oriented principles?

The answer is YES. There are 4 main principles to Object Oriented Programming:

- Encapsulation,
- Inheritance,
- Abstraction, 
- Polymorphism.
  
---

# 14. Which object oriented terms are supported by TypeScript?

TypeScript supports following object oriented terms:

- Modules
- Classes
- Interfaces
- Data Types
- Member functions
  
---

# 15. What are the primitive types in TypeScript?

TypeScript has three primitive types that are frequently used: string, number, and boolean. These correspond to the similarly named types in JavaScript. 

- string: represents text values such as “javascript”, “typescript”, etc.
- number: represents numeric values like 1, 2, 32, 43, etc.
- boolean: represents a variable that can have either a ‘true’ or ‘false’ value.
  
---

# 16. What is any type, and when to use it?

There are times when you want to store a value in a variable but don’t know the type of that variable in advance. The ‘any’ type allows you to assign a value of any type to the variable of type any.

TypeScript assumes a variable is of type any when you don’t explicitly provide the type, and the compiler cannot infer the type from the surrounding context. 

---
  
# 17. What is void, and when to use the void type?
  
The void indicates the absence of type on a variable. It acts as the opposite type to any. It is especially useful in functions that don’t return a value.

If a variable is of type void, you can only assign the null or undefined values to that variable. 
  
---
  
# 18. What is an unknown type, and when to use it in TypeScript?
 
The unknown type is the type-safe counterpart of any type. You can assign anything to the unknown, but the unknown isn’t assignable to anything but itself and any, without performing a type assertion of a control-flow-based narrowing. You cannot perform any operations on a variable of an unknown type without first asserting or narrowing it to a more specific type.

Consider the following example. We create the foo variable of unknown type and assign a string value to it. If we try to assign that unknown variable to a string variable bar, the compiler gives an error.

let foo: unknown = "Akshay";
let bar: string = foo; // Type 'unknown' is not assignable to type 'string'.(2322)
You can narrow down a variable of an unknown type to something specific by doing typeof checks or comparison checks or using type guards. For example, we can get rid of the above error by

let foo: unknown = "Akshay";
let bar: string = foo as string;
  
---
  
# 19. What are the different keywords to declare variables in TypeScript?

- var: Declares a function-scoped or global variable. You can optionally set its value during the declaration. Its behavior and scoping rules are similar to the var keyword in JavaScript. For example,

var foo = "bar";

- let: Declares a block-scoped local variable. Similar to var, you can optionally set the value of a variable during the declaration. For example,

let a = 5;

if (true) {
  let a = 10;
  console.log(a);  // 10
}
console.log(a);  // 5
  
- const: Declares a block-scoped constant value that cannot be changed after it’s initialized.  For example,

const a = 5;

if (true) {
  a = 10; // Error: Cannot assign to 'a' because it is a constant.(2588)
} 

---
  
# 20. What is the Function type in TypeScript?
  
Function is a global type in TypeScript. It has properties like bind, call, and apply, along with the other properties present on all function values.

function perform(fn: Function) {
fn(10);
}
  
You can always call a value of the Function type, and it returns a value of ‘any’ type. 

---

# 21. How to create objects in TypeScript?

Objects are dictionary-like collections of keys and values. The keys have to be unique. They are similar to arrays and are also sometimes called associative arrays. However, an array uses numbers to index the values, whereas an object allows you to use any other type as the key.
  
---
  
# 22. Explain the different variants of the for loop in TypeScript.



---
# 23. Explain the symbol type in TypeScript.
---
# 24. Explain how optional chaining works in TypeScript.
---
# 25. Provide the TypeScript syntax to create function overloads.
---
# 26. What is meant by type inference?
---
# 27. What is meant by contextual typing?
---
# 28. What is the purpose of noImplicitAny?
---
# 29. What is an interface?
---
# 30. Explain the various ways to control member visibility in TypeScript.
---
# 31. Does TypeScript support static classes? If not, why?
---
# 32. What are abstract classes? When should you use one?
---
# 33. What are anonymous functions? Provide their syntax in TypeScript.
---
# 34. What are union types in TypeScript?
---
# 35. What are intersection types?
---
# 36. What are type aliases? How do you create one?
---
# 37. Explain the tuple types in TypeScript.
---
# 38. Explain how tuple destructuring works in TypeScript.
---
# 39. What are type assertions in TypeScript?
---
# 40. How to enforce strict null checks in TypeScript?
---
# 41. How to make object properties immutable in TypeScript? (hint: readonly)
---
# 42. What is a type declaration file?
---
# 43. What are triple-slash directives?
---
# 44. Explain the purpose of the ‘in’ operator.
---
# 45. What are the ‘implements’ clauses in TypeScript?
---
# 46. What are string literal types?
---
# 47. What are template literal types?
---
# 48. Explain the concept of inheritance in TypeScript.
---
# 49. What are conditional types? How do you create them?
---
# 50. List some of the utility types provided by TypeScript and explain their usage.



