Type Aliases vs Interfaces in TypeScript
Introduction
TypeScript provides both type aliases and interface declarations to describe data shapes. They often look similar when defining an object, but they support different forms of composition and extension. Choosing the right one makes code easier to understand and maintain.
Detailed Explanation
An interface is mainly used to describe the structure that an object should follow. It can be extended by another interface, which is useful when several objects share common properties.
interface Person {
  name: string;
  age: number;
}

interface Developer extends Person {
  skills: string[];
}
A type alias can also describe an object, but it can represent more than object shapes. For example, it can define a union, a primitive alias, or a tuple.
type UserId = string | number;
type Status = "active" | "inactive";
type Point = [number, number];
Interfaces support declaration merging: declaring the same interface name more than once adds its members to the same interface. Type aliases do not support this behavior. Both interfaces and object type aliases can be combined with intersections, and interfaces can extend compatible object types.
Conclusion
Use an interface when describing an object contract that may be extended or merged, especially in public APIs. Use a type alias when you need unions, tuples, primitives, or more flexible type composition. For ordinary object shapes, either can work; consistency across a project is also important.