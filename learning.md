Quick Commands:

`tsc src/index.ts --target ES2017 --module commonjs` => You can specifcy the destination target type.

Function return type(s):

// Typical function return type(s)
function nameOfFunction(inputArgs: <Interface>): <returnInterface> {}

interface User {
    firstName: string,
    lastName: string
}

function demo(input: User): string {
    return input.firstName + input.lastName;
}'

Function - Overload signatures:
- You can mention multiple overloads for a function

function contactPeople(method: "email", ...people: HasEmail[]): void;
function contactPeople(method: "phone", ...people: HasPhoneNumber[]): void;

// "function implementation"
function contactPeople(
  method: "email" | "phone",
  ...people: (HasEmail | HasPhoneNumber)[]
): void {

- Interfaces extend interfaces (just like classes extend classes)
- 