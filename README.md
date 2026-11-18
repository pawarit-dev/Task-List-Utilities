# JavaScript Task List Utilities

A small JavaScript project that demonstrates basic array methods and immutable operations through a simple task management utility.

This project is based on the [JavaScript Task List Utilities roadmap project](https://roadmap.sh/projects/js-task-list-utilities).

## Features

- Add a task with an automatically generated ID
- Mark an existing task as completed
- Remove a task by ID
- Count tasks that are not completed
- Use immutable operations without modifying the original task array

## Project Structure

```text
Task-List-Utilities/
|-- taskListUti.js
`-- README.md
```

## Getting Started

Make sure Node.js is installed.

Run the project from the terminal:

```bash
node taskListUti.js
```

## Available Functions

### `addTask(tasks, title)`

Creates a new task and adds it to a new array.

```js
const tasks = [];
const result = addTask(tasks, 'Learn JavaScript');
```

The new task is assigned an ID greater than every existing task ID.

### `completeTask(tasks, taskId)`

Marks the task with the matching ID as completed.

```js
const result = completeTask(tasks, 2);
```

### `removeTask(tasks, taskId)`

Returns a new array without the task matching the supplied ID.

```js
const result = removeTask(tasks, 1);
```

### `countIncompleteTasks(tasks)`

Returns the number of tasks whose `completed` property is `false`.

```js
const count = countIncompleteTasks(tasks);
```

## Example

```js
const tasks = [
    { id: 1, title: 'Review variables', completed: true },
    { id: 2, title: 'Practice functions', completed: false },
];

const withNewTask = addTask(tasks, 'Build task utilities');
const completed = completeTask(withNewTask, 2);

console.log(countIncompleteTasks(completed)); // 1
console.log(tasks.length); // 2
```

## JavaScript Concepts Used

- Arrow functions
- Array methods: `map()` and `filter()`
- Ternary operator
- Spread syntax
- Object and array immutability
- Template-free shorthand object properties
- `Math.max()` with spread arguments

## Learning Goals

This exercise practices creating utility functions, transforming arrays without direct mutation, filtering data, and calculating values from JavaScript objects.
