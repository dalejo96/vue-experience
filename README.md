# Vue-experience

This is my journey and experience with the [Vue.js](https://vuejs.org/) framework.

Every folder contains an application, from the simple CounterApp to ...

## Folders - Projects

- *CounterApp*: a basic JS counter with two buttons one for subtraction and the other to add 1 to the general count, includes an Options API vs Composition API approach to solve the problem.

- *NotesApp*: a JS notes application with a modal, a textarea and some buttons, here you can see some vue directives, state (ref) and iteratively rendering DOM elements and some error handling.

- *QuizApp*: a JS quiz application with a predefined JSON data, with all the relevant information. Listeners for watching state changes (watch), create components for isolation and reusability, routing, emitting events (defineEmits) and Vue animations (CSS and JS with gsap).

- *ShowApp*: A JS basic application that fetches data from an external API. You can check how to handle HTTP requests, usage of Suspense wrapper, <slot>, slot with ids, and KeepAlive.

## Development

If you want to check any project just go to the respective folder and run:

```bash
npm install
npm run dev
```