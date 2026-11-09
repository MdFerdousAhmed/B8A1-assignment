Type Narrowing in TypeScript
Introduction
Type narrowing is the process of reducing a variable's possible types inside a particular part of a program. It helps TypeScript understand which operations are safe after a condition has been checked. This is especially useful when a parameter has a union type.
Detailed Explanation
The typeof operator narrows primitive values such as strings and numbers. For example, the function below accepts either type and safely handles each case.
function formatValue(value: string | number): string {
  if (typeof value === "string") {
    return value.trim().toLowerCase();
  }
  return value.toFixed(2);
}
The instanceof operator checks whether an object was created by a particular class or constructor. It is useful for built-in classes such as Date and Error.
function getMessage(value: Date | Error): string {
  if (value instanceof Date) {
    return value.toISOString();
  }
  return value.message;
}
The in operator checks whether a property exists on an object. TypeScript can use that check to distinguish object types in a union.
type Admin = { permissions: string[] };
type Customer = { shippingAddress: string };

function describeAccount(account: Admin | Customer): string {
  if ("permissions" in account) {
    return account.permissions.join(", ");
  }
  return account.shippingAddress;
}
TypeScript also tracks conditions through control flow, so a type may become narrower after an early return or inside an else branch.
Conclusion
Use typeof for primitive checks, instanceof for class instances, and in for checking object properties. These guards make union-typed code safer and reduce the need for unsafe type assertions.