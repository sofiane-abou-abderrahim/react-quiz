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

## 7. Highlighting Selected Answers & Managing More State

1. add a new `answerState` state that controls our current answer state in `Quiz.jsx`
2. dynamically change the color of the selected answer

## 8. Splitting Components Up To Solve Problems

1. shuffle the answers once when the `activeQuestionIndex` changes by using the `useRef` hook in `Quiz.jsx`
2. create a `Answers.jsx` component to make sure that the answers are shuffled every next questions & that the answer doesn't remain selected
3. output the `<Answers>` component in `Quiz.jsx`
4. create a `Question.jsx` component to use only one `key` prop

## 9. Moving Logic To Components That Actually Need It ("Moving State Down")

1. move the state down from the `Quiz.jsx` component to the `Question.jsx` component
2. disable the button to prevent from clicking it when an answer was selected in `Answers.jsx`

## 10. Setting Different Timers Based On The Selected Answer

1. update the `<QuestionTimer>` component in `Question.jsx`
   1. if an answer was selected so that a new timer starts and only expires after we showed the correct or wrong answer
   2. when this timer expires don't tell the `Quiz.jsx` component that the question was not answered
2. add a `mode` prop in `QuestionTimer.jsx` & set it as a `className`, then set its value to the `answerState` in `Question.jsx` for styling purposes
3. reset the interval whenever the timer changes to make the interval inline with the new timer and the new `max` value of the `progress` bar by adding a `key` prop with a value of `timer` in `Question.jsx`
4. trigger the `onSkipAnswer` function only if no answer was selected in `Question.jsx` to avoid skipping questions unexpectedly
