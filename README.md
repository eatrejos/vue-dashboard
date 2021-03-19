# vue-tailwind-admin
A simple admin template built using [TailwindCSS](https://tailwindcss.com) & [Vue.js](https://vuejs.org). This project is also running [Vuex](https://vuex.vuejs.org) in order to control the sidebar state throughout components. 

At first, main.js is the one that runs the routes on the App, the file root path is running by defualt so the first path will be: /dashboard/home/ ...in dashboard component, there is a router-view and it's matched with the children route in above path, /dashboard is parent and /home is child so, /dashboard/* pages will be display in dashboard layout. I think this is the same conception as react, know as passing props to the child component or also known as one-way binding.
Team.vue page it's very simple code its consunming data from /json/cards.json mock api file, and it also brings Card component and ContactsTable component.

Essentialy I took 8 hours to just build the demo itself in case you find something missing from requirements thats why, how ever the rest of the time I used it to understand  VueJS a little better, but for the most part what took me more was implementing vuex and handling global state and finding the right template with the right components from tailwindcss but I actually feel that Vue is a lot simpler than Angular 10 and React 17.

## Live Demo

This is the demo I used to create this test for reference, it uses tailwind.css as intended.

[https://angry-mahavira-9b32ec.netlify.com/](https://angry-mahavira-9b32ec.netlify.com/)

## Project setup
```
npm i
```

### Compiles and hot-reloads for development environment
```
npm run serve
```

### Compiles and minifies for production environment
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
