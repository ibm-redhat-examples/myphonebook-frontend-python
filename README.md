# myphonebook-frontend




### React Explained
React is a library, not a framework. Unlike client-side MVC frameworks, like Backbone, Ember, and AngularJS, it makes no assumptions about your tech stack so you can easily integrate it into a new or legacy code base.

React’s only concern is with the user interface (the ‘V’ in MVC), which is defined by a hierarchy of modular view Components that couple static markup with dynamic JavaScript. If you’re familiar with Angular, these Components are similar to Directives. Components use an XML-like syntax called JSX that transcompiles down to vanilla JavaScript.

Since Components are defined in a hierarchical order, you don’t have to re-render the entire DOM when a state changes. Instead, it uses a Virtual DOM that only re-renders the individual Components after the state has changed, at blazingly fast speeds!

React has been designed from the start for gradual adoption, and you can use as little or as much React as you need. Whether you want to get a taste of React, add some interactivity to a simple HTML page, or start a complex React-powered app, the links in this section will help you get started.

For more details checkout - https://realpython.com/the-ultimate-flask-front-end/

## 1. Project Setup
Let’s start with what we know: Flask.
Here are the highlevel steps
- verify you have pip installed
- create a working directory such as "myphoneapp-frontend"
- Download the boilerplate code from the repository, 
- extract the files, 
- create then activate a virtualenv, and 
- install the requirements:


### Install the requirements

```
$ pip install -r requirements.txt
```

Finally, let’s run the app and start the show:

$ sh run.sh
