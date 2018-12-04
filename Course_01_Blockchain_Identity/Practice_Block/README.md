# Practice Block Data Exercise

To use this boilerplate code locally follow this steps:

1. Clone or download the project.
2. Open your project with your favorite IDE.
3. Run `npm install` to install the dependencies.
4. Implement your code.
5. Use `node app.js` to run the application.

## Let's do some Coding Practice

In the previous section, you learned about the basic data in a block and how it generates a hash. In this section, you will see how to get the hash using Javascript and Node.js.

### Here’s a quick look at the steps you’ll complete.

**Step 1:** `generateHash` method in the **Block** class

**Step 2:** Use Promises to generate the hash asynchronously

**Step 3:** Run the application `node app.js`

Each step you’ll take to complete this exercise is called out in comments throughout the code. You can find more details and guidance about each of these steps in the text provided below the code.

Let’s get started!

#### Step 1. Implement `generateHash` method in the Block class
In the `block.js` file, you will find the `Block` class. We have added `generateHash` method. This method should take the block object, generate the `hash`, and reassign to the hash property in the same block.

You might be wondering, why are we using `let self = this;`? You will have to use Promises when you implement the method. By using `let self = this;`, you can access the `this` object inside the Promise code.

#### Step 2. Use Promises to generate the hash asynchronously
This is not a course of Promises, but we want to help you to get starter with this new concept or refresh your knowledge.

**Note:** We introduce Promises here to help you evaluate your understanding of this feature because you will need to be able to use Promises in order to pass your project.

Promises allow you to run some code asynchronously. To create a promise, you'll need:

```
var promise = new Promise(function(resolve, reject) {
  // do a thing, possibly async, then…

  if (/* everything turned out fine */) {
    resolve("Stuff worked!");
  }
  else {
    reject(Error("It broke"));
  }
});
```

The Promise constructor takes one argument, a callback with two parameters - `resolve` and `reject`. This means: Do something within the callback (perhaps something asynchronous), then call `resolve` if everything worked; otherwise call `reject`.

And how you will read the result from the Promise?

```
promise.then(function(result) {
  console.log(result); // "Stuff worked!"
}, function(err) {
  console.log(err); // Error: "It broke"
});
```

#### Additional Resources
This is a very important skill that you will need for the rest of the program, so take your time in reviewing these resources:

- [Google Developers Promises](https://developers.google.com/web/fundamentals/primers/promises)
- [Udacity Free Course Promises](https://www.udacity.com/course/javascript-promises--ud898)

### Step 3. Run the application node `app.js`

`App.js` File

```
//Import the Block class
const BlockClass = require('./block.js');

// Creating a block object
const block = new BlockClass.Block("Test Block");

// Generating the block hash
block.generateHash().then((result) => {
    console.log(`Block Hash: ${result.hash}`);
    console.log(`Block: ${JSON.stringify(result)}`);
}).catch((error) => {console.log(error)});

#####################################################################
## Step 3: Run the application in node.js                          ##
##     -- See details for this step in the text below --           ##
#####################################################################

// From the terminal: `cd` into Project folder
// From the terminal: Run `node app.js` to run the code

```
