# Homework: React Film Releases

When creating React applications, we want to break up our UI into components, so each component is responsible for one part of the page. Your task for this homework is to start to think about how you might approach this task in your own applications by reading an article published by Facebook (creators of React) and examining an existing codebase.

## Reading

Thinking In React (20 mins) https://facebook.github.io/react/docs/thinking-in-react.html

## Film Releases Application

Run the Film Releases Application:

```bash
npm install
npm start
```
Your task is to get familiar with the application.

## Part 1
Draw a diagram that details:
  - the component hierarchy (which component renders which)
  - any props that are passed from parent to child components
  - any state inside any of the components

## Part 2
Answer the following questions:
  1. Where do we directly access an element from the DOM in our React application?
  This is in our index.js file with the code 'document.getElementById('root')'
  2. From looking at the code, what do you think might be the difference between the components in the `containers` and `components` directories?
  The container groups together all of the components and hold the movies array of objects. All of the components can then access these objects (and their attributes) using props, in order to render their individual data.
  3. What is the responsibility of the `ReleasesBox` component?
  This creates an array of objects with the movie information (name, id and url), which are accessed from app.js using props. It then renders these and has a state, so that these are rendered again when there is any update from movie list.
  3. What is the responsibility of the `MovieList` component?
  This accesses the movie data from ReleasesBox using props and creates an array of the movies ensuring they are the correct shape - if no data is given then the default is an empty array. It creates an unordered list of the characteristics of the objects.
  4. What is the responsibility of the `MovieItem` component?
  This accesses the url and name of the movie using props and creates a list item for each movie. The list item displays the text content as the name and creates a hyperlink using the url. Again it checked the shape is correct, and states that these are required.
