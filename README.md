# Working with Effects

## Practice & Dive Deeper

- Apply your Knowledgge
- Dealing with Effect Dependencies & Cleanup
- Combining Effects with Other React Concepts

# Steps

## 0. Starting Project

1. run `npm install`
2. run `npm run dev`
3. create a `README.md`

## 1. A First Component & Some State

1. create a `components` folder
2. Inside it, add a `Header.jsx` component & a `Quiz.jsx` component
3. built `Header.jsx` component
4. add states in `Quiz.jsx` to manage the questions & answers
5. output `<Header>` & `<Quiz>`components in `App.jsx`

## 2. Deriving Values, Outputting Questions & Registering Answers

1. create a `questions.js` file with questions & answers inside
2. change the logic in `Quiz.jsx` for managing questions & answers

## 3. Shuffling Answers & Adding Quiz Logic

1. shuffle the answers by using the `sort` method in `Quiz.jsx`
2. make sure the app doesn't break if we answer all the questions & display a summary instead of the quiz

## 4. Adding Question Timers

1. create a `QuestionTimer.jsx` component
2. set a progress bar inside `QuestionTimer.jsx`
3. define a timeout & an interval using the `useState` & `useEffect` hooks inside `QuestionTimer.jsx`
4. ouptut the `<QuestionTimer>` component inside `Quiz.jsx`

## 5. Working with Effect Dependencies & useCallback

1. make sure the timeout doesn't execute again by wrapping the `handleSelectAnswer` function with the `useCallback` hook in `Quiz.jsx`

## 6. Using Effect Cleanup Functions & Using Keys for Resetting Components

1. cleanup the existing interval if the effect function runs again in `QuestionTimer.jsx`
2. cleanup the existing timer to prevent it from keeping on going in `QuestionTimer.jsx`
3. reset the `<QuestionTimer>` component when the question changes by adding a `key` prop to it
