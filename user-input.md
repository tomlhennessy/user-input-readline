# User Input with Readline

* Before, our programs always behaved the same way whenever we ran them. Now, we want users to be able to interact with our programs while they're running, influencing what happens next.

* We use Node's "readline" module to gather input from users while the program is running. This happens asynchronously, meaning the program doesn't wait for the user to respond before continuing.

* We start by importing the "readline" module into our JavaScript file. Then, we set up an interface to communicate with the user, using standard input and output streams.

* To ask the user a question, we use the "question" method on our interface. This method takes a question to display and a callback function to handle the user's response.

* It's important to close the interface after we're done asking questions to avoud the program hanging.

* Since the "question" method is asynchronous, we have to be careful about the order of execution. We can use callback chaining to ensure commands happen in the right sequence after the user responds.

* If we need to ask multiple questions in a row, we nest the "question" calls inside each other's callback functions. this prevents the program from moving on to the next question before the user answers the current one.

* To keep our code neat and readable, especially with longer chains of questions, we can use named functions instead of anonymous ones.

* Callback chaining is a common pattern in JavaScript, especially for handling asynchronous operations. Later on, we'll learn about more advanced techniques to avoid "callback hell" and keep our code organised.
