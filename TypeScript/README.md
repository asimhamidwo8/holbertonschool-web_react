# TypeScript

A set of exercises to learn the basics of TypeScript: interfaces, classes, functions, advanced types, ambient declarations, namespaces, declaration merging, and nominal typing.

## Requirements

- Node.js and npm
- TypeScript 3.x
- Webpack 4 (with `ts-loader` and `fork-ts-checker-webpack-plugin`)
- Ubuntu 20.04 LTS (or WSL)

## Installation and build

Each task folder has its own configuration files (`package.json`, `tsconfig.json`, `webpack.config.js`).

```bash
cd task_0
npm install
npm run build
```

On recent Node.js versions, Webpack 4 needs this option:

```bash
NODE_OPTIONS=--openssl-legacy-provider npm run build
```

A successful build shows `No type errors found`.

## Tasks

| # | Folder | Description |
|---|--------|-------------|
| 0 | `task_0` | `Student` interface, a list of students, and a table rendered with Vanilla JavaScript. |
| 1 | `task_1` | `Teacher` interface with readonly, optional, and dynamic properties. |
| 2 | `task_1` | `Directors` interface that extends `Teacher`. |
| 3 | `task_1` | `printTeacher` function described by the `printTeacherFunction` interface. |
| 4 | `task_1` | `StudentClass` described by a class interface and a constructor interface. |
| 5 | `task_2` | `Director` and `Teacher` classes, and `createEmployee` that returns one of them based on salary. |
| 6 | `task_2` | `isDirector` type predicate and `executeWork`. |
| 7 | `task_2` | `Subjects` string literal type and `teachClass`. |
| 8 | `task_3` | Ambient declarations (`crud.d.ts`) for a third-party JavaScript library (`crud.js`). |
| 9 | `task_4` | `Subjects` namespace with declaration merging for `Teacher`, and the `Cpp`, `React`, and `Java` classes. |
| 10 | `task_5` | `MajorCredits` and `MinorCredits` interfaces using brand properties for nominal typing. |

## Key concepts

- **Interfaces:** Describe the shape of objects, functions, and classes.
- **Readonly and optional properties:** `readonly` can only be set at creation; `?` makes a property optional.
- **Index signatures:** `[key: string]: any` allows extra properties.
- **Union types and type predicates:** `Director | Teacher` and `employee is Director`.
- **String literal types:** Limit a value to specific strings, like `'Math' | 'History'`.
- **Ambient declarations:** `.d.ts` files add types to JavaScript libraries.
- **Namespaces and declaration merging:** The same interface can be extended across files.
- **Brand convention:** A unique property makes two similar types incompatible.

## Author

Asim Hamid
