# Unit-Testing-for-MEAN-with-Jasmine
Unit Testing for MEAN with Jasmine

# What are unit tests?
Unit tests or Unit testing are part of the different procedures that can be carried out within the agile methodology; code that is used to test other code. Small tests created specifically to cover all the requirements of the code and verify its results.

## What are unit tests for?
* Safety net: Prevent unexpected changes in our applications by members of our team or even ourselves.
* Code quality: Continuous improvement of our code. We can review and improve old code or contemplate use cases that we did not take into account when starting development.
* Reduce costs: Prevention and detection of errors at an early age, before they can get out of control.

# Why do unit tests?
Productivity, value generated, budget, time, are considered the most important variables in any type of project. If you ask the business owner, the budget will be the main thing. If you talk to the product owner, productivity and value added will be his focus. If you talk to the client, time is probably the most important thing. That is why it is worth asking ourselves, should we reserve a space for creating unit tests?

Creating unit tests involves creating a parallel application that allows us to run and test our base code. That is, depending on the skills of the programmer, the time dedicated to its creation can be equal to or in some cases greater than the time spent writing the solution.

Let's see this with an example. Imagine that a company is tasked with creating a form to register conference attendees. As the budget is tight, the development group decides to create the solution without a test system. The first phase of the project was a "success". The testing team encounters a problem with the form validations and a console error due to a data type. The development team solves the problem and the product can finally be delivered.

From the previous situation we can analyze the following:

1. Although the first delivery of the product was successful, the lack of an alert system during development time meant that errors related to data types were only detected during quality tests.

2. The application required a new development cycle to fix the problem.

3. Due to the size of the application, making changes will be quite fast.

Now, suppose that same system is used for another client, but this time an authentication system must be added. A person from the team decides to leave the company. The development process was successful. The estimated time was increased. Again, no test system was created. Two rounds of additional testing and development were required to deliver the product.

Let's analyze the previous situation:

1. The project was delayed due to the departure and learning process of the new developer.

2. Again, there was no testing system in the application.

3. Two rounds of testing and development were carried out in addition to what was planned.

What can you conclude from these situations? How could you improve the development process of this application? As you can imagine, one of the things that could be improved would be the implementation of a test system. However, how can unit tests help you in your development?

## Unit tests
Let's start with the definition. Unit tests are nothing more than a program that allows us to test our base code. In other words, unit testing involves the creation of small code extracts that will execute all the lines within a function, so that its behavior can be verified.

The time spent creating the unit tests should be included during the development phase, so that the solution and tests related to the problem can be created at the same time.

## What are unit tests for?
Unit tests serve to:
1. Safety Net: Every time you create a unit test, you analyze the code in small parts, therefore, it is possible to create an alert system for future changes in the code.

2. Documentation: Because we have an application that will execute the lines of code in our program, it is the perfect time to document and verify what we hope will happen. That is, we are going to explain our code, showing how they should be used.

3. Code quality: During the process of creating unit tests, in addition to detecting errors, it is the ideal time to improve the solution or apply better design patterns to our code.

4. Cost reduction: All of the above points will help with cost reduction. Having adequate documentation will help us with future modifications to the code or the incorporation of new developers to the project. The safety net and the quality in the code will allow early error detection, therefore, it will prevent you from falling behind in deliveries.

## Conclusions
Incorporating unit tests into a project is one of the best decisions you can make. You should bear in mind that the tests will not only help you reduce costs, they are created with the purpose of helping us between developers during the code creation process.

Counting a test set can take time at first, but with practice it will be intuitive and fast. The concepts learned during this course will be useful to you not only for tests created using Jasmine.

# First unit test in JavaScript
Unit testing features:
* Although the results must be specific to each unit test developed, the results can be automated, so that we can do the tests individually or in groups.
* Small constant process test on part of the code, but in the end, it must be verified in its entirety.
* In the case of repeating the tests individually or in groups, the result must always be the same, giving the same order in which the tests are performed, the tests are stored to be able to perform these repetitions or to be able to use them on other occasions.
* It is an isolated code that has been created with the mission of verifying other very specific code, it does not interfere with the work of other developers.
* Despite what many developers think, unit testing code should take no more than 5 minutes to create, they are meant to get the job done faster.

# The expect() and it() functions
Runtime errors also result in a new Error object being created and launched.

Error objects are normally created with the intention of throwing them using throw. It is possible to handle the error using try catch:
```javascript
try {
     throw new Error ("Something went wrong!");
} catch (e) {
     alert ("Well done");
}
```
The it () function defines a jasmine test. It's called that because its name makes reading tests almost like reading in English.

The second argument to the it () function is itself a function, which when executed will probably execute a number of _expect () functions.

The expect () functions are used to actually test the things you "expect" to be true.

# Organizing the code to run on the web
The term refactoring is often used to describe modifying source code without changing its behavior, which is informally known for cleaning code.

Refactoring is the part of code maintenance that doesn't fix bugs or add functionality. The objective, on the contrary, is to improve the ease of understanding the code or change its structure and design and eliminate dead code, to facilitate future maintenance.

Adding new behavior to a program can be difficult with the given program structure, so a developer can refactor it first to facilitate this task and then add the new behavior.

# Organizing code to run using nodejs
Node.js is an open source, cross-platform, runtime environment for the server layer (but not limited to it) based on the ECMAScript programming language

It was created with the focus of being useful in creating highly scalable network programs, such as web servers.

Example of a hello world of an HTTP server written in Node.js:
```javascript
const http = require ('http');

const hostname = '127.0.0.1';
const port = 1337;

http.createServer ((req, res) => {
   res.writeHead (200, {'Content-Type': 'text / plain'});
   res.end ('Hello World \ n');
}). listen (port, hostname, () => {
   console.log (`Server running at http: // $ {hostname}: $ {port} /`);
});
```

# Static code analysis tools
* Linters: Alert tools. They help us to follow the rules or conventions of our teams without having to memorize the entire rule book; we just need to program and make sure these tools check our code.

For example: ESLint, JSHint, CSSComb or scsslint.

* Automatic correction: Tools that help us review and fix our code regardless of whether we use one code editor or another; they work for all cases and tastes of the community. For example: Prettier.

* Typing: JavaScript is a dynamic typing language, we can change the type of variables whenever we want or need. But, we can use different tools to implement strong typing, that is, we can use variables with different types than the one we initially defined (unless we do a conversion).

The most popular typing tool in JavaScript is TypeScript but there are also some alternatives like Flow and React PropTypes.

# ESLint: Adding alerts to our code with ECMA Script
ESLint is a tool that identifies and reports patterns and errors in ECMAScript / JavaScript code. It is similar to JS-Lint and JSHint with some differences:

ESLint uses Espree to parse JavaScript.
ESLint uses an AST to evaluate patterns in code.
ESLint supports plugins, each rule is a plugin and you can add more in development.

Documentation:
```https
https://eslint.org/docs/user-guide/configuring
```

NPM:
```terminal
$ npm install -g eslint
```

# Style correction tools
Documentation:
```https
https://prettier.io/
```

Prettier is an opinionated code formatter. Apply a consistent style when parsing your code and reprinting it with your own rules that take into account the maximum line length, wrapping the code when necessary.

It can be run in your editor when saving, on a pre-commit hook, or in CI environments to ensure your codebase is consistent in style without developers having to post a thorough comment on a code review.

It offers support for:
* JavaScript, including ES2017
* JSX
* Angular
* Go
* Flow
* TypeScript
* CSS, Less, and SCSS
* HTML
* JSON
* GraphQL
* Markdown, including GFM and MDX
* YAML

For example we have this malformed JavaScript code:
```javascript
foo (reallyLongArg (), omgSoManyParameters (), IShouldRefactorThis (), isThereSeriouslyAnotherOne ());
```

Passing Prettier leaves us in a more readable way:
```javascript
foo (
  reallyLongArg (),
  omgSoManyParameters (),
  IShouldRefactorThis (),
  isThereSeriouslyAnotherOne ()
);
```

NPM:

```terminal
$ npm install -g prettier
$ prettier --write [DOCUMENT NAME]
```

# Typing tools
TypeScript is a free and open source javascript programming language superset developed and maintained by Microsoft.

It is a JavaScript superset, which essentially adds static typing and class-based objects.

TypeScript extends JavaScript syntax, so any existing JavaScript code should work fine.

It is intended for large projects, which through a TypeScript compiler are translated into original JavaScript code.

# Jasmine spyOn
The separation of responsibilities is one of the good practices that we find in a software project. Separating responsibilities means grouping code in such a way that each set handles a specific task.

Now let's talk about unit tests. When we test a component, we want to test the responsibilities that we are delegating to the component and not all the code that is executed. That is, if component A uses the b () function, what we want to test is the component's own logic and not the function's code.

Let's look at the following example:
```javascript
function GetMonthApi () {
  this.currentMonth = function () {
    return 'May';
  }
  this.nextMonth = function () {
    return 'June'
  }
}
export function MonthCalculator () {
  this.api = new getMonthApi ();
  this.getNextMonth = function () {
    return this.api.nextMonth ();
  }
  this.getCurrentMonth = function () {
    return this.api.currentMonth ();
  }
}
```
The MonthCalculator class allows us to calculate the value of the current and next month. As you can see, the function getMonthApi is used inside the class. If you run the set of tests associated with our class it runs in May the value of the following month would be June, or if you run them in January the next month would be February. Do you see the problem?

If we execute code that is outside the domain of a component, we can find unexpected results. That is why jasmine has a spy system (spyOn), whose main objective is to intercept the execution of a function and simulate its result.

## Let's see a bit of code:
The first method we are going to try is to get the current month **currentMonth**. If we create the test in May, the code should be:
```javascript
describe ('MonthCalculator', () => {
   it ('returns the current month', () => {
     // Arrange
     const monthCalculator = new MonthCalculator ();
     // act
     const month = monthCalculator.currentMonth ();
     // Assert
     expect (month) .toBe ('May');
   });
});
```
This code has a problem. The **currentMonth** function will return a value that depends on the current month.

As you can already imagine, the use of spies is quite useful in this case because we can control the value of the returned month.

That is to say:
```javascript
describe ('MonthCalculator', () => {
  it ('returns the current month', () => {
    // Arrange
    const monthCalculator = new MonthCalculator ();
    const spy = spyOn (
                 monthCalculator.api,
                 'currentMonth'
               ) .and.returnValue ('Cristian Month');
    // act
    const month = monthCalculator.currentMonth ();
    // Assert
    expect (month) .toBe ('Cristian Month');
    expect (spy) .toHaveBeenCalled ();
  });
});
```
The API instance is stored in the variable this.api of our class.
Jasmine allows us to intercept the call to our API using the spyOn function. For this, as the first parameter we must pass the object that contains the method that we are going to intercept and as the second parameter its name.

Once our spy is created, in order to control the returned value we must concatenate the following: **.and.returnValue ()**.
Finally Jasmine allows us to verify the execution of the function by means of the operator **.toHaveBeenCalled ()**.

## List of questions and answers about everything you can do with spies:
### How do you create a spy?
```javascript
spyOn (obj, 'method') // obj.method is a function
```
### How to verify that a method was called?
```javascript
const ref = spyOn (obj, 'method');
expect (ref) .toHaveBeenCalled ();
// Or directly
expect (obj.method) .toHaveBeenCalled ()
```
### How to verify that a method was called with a specific parameter?
```javascript
const ref = spyOn (obj, 'method');
expect (ref) .toHaveBeenCalledWith ('foo', 'bar');
// Or directly
expect (obj.method) .toHaveBeenCalledWith ('foo', 'bar')
```
### How can I check the exact number of executions of a method?
```javascript
expect (obj.method.callCount) .toBe (2)
```
### How to spy on a method without modifying its behavior?
```javascript
spyOn (obj, 'method'). andCallThrough ()
```
### How can I change the returned value by a method?
```javascript
spyOn (obj, 'method'). andReturn ('value')
```
### How can I overwrite a method?
```javascript
spyOn (obj, 'method'). andCallFake (() => 'this is a function');
```

# Set up a work environment to work with the jasmine framework
Jasmin documentation:
```https
https://jasmine.github.io/
```
```https
https://github.com/jasmine/jasmine#installation
```
```https
https://github.com/jasmine/jasmine/releases
```

Jasmine is a Behavior Driven Development framework for conducting our unit tests with JavaScript.

It can be run in the browser but we can also use a headless browser to better automate the tests. For example, with PhantomJS, CasperJS or ZombieJS.

We also don't need a DOM; therefore, it is possible to test on any Javascript Engine like Rhino or V8 (like Node.js).

## How does it work?
Jasmine's main functions for testing are as follows:
* **describe(a, b)** where "a" is the description of our suite and "b" the anonymous function where the entire suite or series of specifications will be included.
* **it(a, b)** where “a” is the description of the specification and “b” the anonymous function where the expectations that the application must meet will be included.
* **expect(a)** where "a" is a value to be tested, using string arguments (method chaining). For example: expect (true) .not.toBe (false).
* **beforeAll(a)** where "a" will be the function that will be executed before starting the tests.
* **afterAll(a)** where “a” will be the function that will be executed after starting the tests.
* **beforeEach(a)** where "a" will be the function that will be executed before each test.
* **afterEach(a)** where "a" will be the function that will be executed after each test.

# Configure Jasmine using Node.js
Add Jasmine to your package.json:
```terminal
$ npm install --save-dev jasmine
```

Initialize Jasmine in your project:
```terminal
$ npx jasmine init
```

Set jasmine as your test script in your package.json
```
"scripts": { "test": "jasmine" }
```

Run your tests
```
$ npm test
```

# First set of tests with Jasmine
Jasmine functions with which we can experiment:
* expect(x).toEqual(y) checks if both values are equal.
* expect(x).toBe(y) checks if both objects are the same.
* expect(x).toMatch(pattern) checks if the value belongs to the set pattern.
* expect(x).toBeDefined() checks if the value is defined.
* expect(x).toBeUndefined() checks if the value is undefined.
* expect(x).toBeNull() checks if the value is null.
* expect(x).toBeTruthy() checks if the value is true.
* expect(x).toBeFalsy() check if the value is false.
* expect(x).toContain(y) checks if the current value contains the expected one.
* expect(x).toBeLessThan(y) checks if the current value is less than expected.
* expect(x).toBeGreaterThan(y) checks if the current value is greater than expected.

# Jasmine Dictionary:
This reading will serve as a reference for the things you can do with Jasmine:

## Creating a test set
```javascript
describe("Component", () => {
   it ("should ...", () => {
     expect(true).toBe(true);
   });
});
```

## Grouping by functionality
```javascript
describe("Component", () => {
   describe("Functionality one", () => {
     it ("should ...", () => {
       expect(true).toBe(true);
     });
   });
});
```

## Matchers
```javascript
expect(false).not.toBe(true); // negative test
```

## comparison with ===, example: 1 === 1 1! == '1'
```javascript
expect(thing).toBe(realThing);
```

## Value is not undefined
```javascript
expect(result).toBeDefined();
```

## The current value is false, example: 0, '', false
```javascript
expect(result).toBeFalsy();
```

## The current value is true, example: 'sd', 1, true
```javascript
expect(thing).toBeTruthy();
```

## The current value is greater than expected
```javascript
expect(result).toBeGreaterThan(3);
```

## The current value is greater than or equal to the expected
```javascript
expect(result).toBeGreaterThanOrEqual(25);
```

## The current value is less than expected
```javascript
expect(result).toBeLessThan(0);
```

## The current value is less than or equal to the expected
```javascript
expect(result).toBeLessThanOrEqual(123);
```

## The current value is NaN
```javascript
expect(thing).toBeNaN();
```

## The current value is -Infinity
```javascript
expect(thing).toBeNegativeInfinity();
```

## The current value is Infinity
```javascript
expect(thing).toBePositiveInfinity();
```

## The current value is null
```javascript
expect(result).toBeNull();
```

## The current value continues a string. Example:
```javascript
 'Hello world'.toContain(' Hello ') // true
['Hello', 'world'].ToContain('Hello') // true
expect(array).toContain(anElement); 
expect(string).toContain(substring);
```

## The current value is the same using a deep comparison
```javascript
expect(bigObject).toEqual({"foo": ['bar', 'baz']});
```

## The spy was called
```javascript
expect(mySpy).toHaveBeenCalled(); 
expect(mySpy).not.toHaveBeenCalled();
```

## The spy was called before another
```javascript
expect (mySpy) .toHaveBeenCalledBefore (otherSpy);
```

## The spy was called n times:
```javascript
expect(mySpy).toHaveBeenCalledTimes(3);
```

## The spy was called with the following parameters
```javascript
expect(mySpy).toHaveBeenCalledWith('foo', 'bar', 2);
```

## Check if an element has a class
```javascript
const el = document.createElement ('div');
el.className = 'foo bar baz';
expect(el).toHaveClass('bar');
```

## The current value compared to a regular expression
```javascript
expect("my string").toMatch(/ string $ /);
expect("other string").toMatch("her");
```

## Lifecycles
```javascript
describe("Component", () => {
  // Shared variables
  var foo = 0;
beforeAll(() => {})
  beforeEach(() => {})
  afterEach(() => {})
  afterAll(() => {})
});
```

## Disabling tests
```javascript
xdescribe("A spec", () => {
  it("waiting to be enable", function () {
    expect(true).toEqual(true);
  });
});
describe("A spec", () => {
  it("this run", () => {
    expect(true).toEqual(true);
  });
  xit("this is skipped", () => {
    expect(true).toEqual(true);
  });
});
```

## Using spyOn
```javascript
describe('A spy', () => {
  let foo,
    bar = null;
  beforeEach(() => {
    foo = {
      setBar: value => {
        bar = value;
      },
    };
    spyOn(foo, 'setBar');
    foo.setBar(123);
    foo.setBar(456, 'another param');
  });
  it('tracks that the spy was called', () => {
    expect(foo.setBar).toHaveBeenCalled();
  });
  it('tracks that the spy was called x times', () => {
    expect(foo.setBar).toHaveBeenCalledTimes(2);
  });
  it('tracks all the arguments of its calls', () => {
    expect(foo.setBar).toHaveBeenCalledWith(123);
    expect(foo.setBar).toHaveBeenCalledWith(456, 'another param');
  });
});
```

## Create spy when we don't know if the function exists
```javascript
describe("Create a 'bare' spy", () => {
  let notSure;
  beforeEach(function () {
    notSure = jasmine.createSpy('notSure');
    notSure("I", "am", "a", "spy");
  });
  it("tracks that the spy was called", function () {
    expect(notSure).toHaveBeenCalled();
  });
});
```

## Creating multiple spies on the same object
```javascript
describe("Multiple spies", () => {
  const tape;
  beforeEach(() => {
    tape = jasmine.createSpyObj('tape', ['play', 'pause', 'stop']);
    tape.play();
      tape.pause();
      tape.rewind(0);
    });
  it("creates spies for each requested function", () => {
    expect(tape.play).toBeDefined();
    expect(tape.pause).toBeDefined();
    expect(tape.stop).toBeDefined();
  });
});
```

## Verify a property of an object
```javascript
describe("jasmine.objectContaining", () => {
  let foo;
  beforeEach(() => {
    foo = {
      a: 1,
      b: 2,
      bar: "baz"
    };
  });
  it("matches objects with the expect key / value pairs", () => {
    expect(foo).toEqual(jasmine.objectContaining({
      bar: "baz"
    }));
    expect(foo).not.toEqual(jasmine.objectContaining({
      c: 37
    }));
  });
});
```

## Verify a property inside an object passed as a parameter to a function
```javascript
describe('jasmine.objectContaining', () => {
  it('is useful for comparing arguments', () => {
    const callback = jasmine.createSpy('callback');
    callback({
      bar: 'baz',
    });
    expect(callback).toHaveBeenCalledWith(
      jasmine.objectContaining({
        bar: 'baz',
      })
    );
  });
});
```

## Verify a value within an array
```javascript
describe("jasmine.arrayContaining", () => {
  let foo;
  beforeEach(function () {
    foo = [1, 2, 3, 4];
  });
  it("matches arrays with some of the values", () => {
    expect(foo).toEqual(jasmine.arrayContaining([3, 1]));
    expect(foo).not.toEqual(jasmine.arrayContaining([6]));
  });
});
```

## Verify a value within an array passed as a parameter to a function
```javascript
describe('jasmine.arrayContaining', () => {
  it('is useful when comparing arguments', () => {
    const callback = jasmine.createSpy('callback');
    callback([1, 2, 3, 4]);
   expect(callback).toHaveBeenCalledWith(jasmine.arrayContaining ([4, 2, 3]));
   expect(callback).not.toHaveBeenCalledWith (jasmine.arrayContaining ([5, 2]));
  });
});
```

## Using regex to compare compare text strings
```javascript
describe('jasmine.stringMatching', () => {
  it("matches as a regexp", () => {
    expect({foo: 'bar'}).toEqual ({foo: jasmine.stringMatching (/ ^ bar $ /)});
    expect({foo: 'foobarbaz'}).toEqual({foo: jasmine.stringMatching ('bar')});
  });
   describe("when used with a spy", () => {
    it("comparing arguments", () => {
      const callback = jasmine.createSpy ('callback');
      callback('foobarbaz');
      expect(callback).toHaveBeenCalledWith(jasmine.stringMatching ('bar'));
      expect(callback).not.toHaveBeenCalledWith(jasmine.stringMatching (/ ^ bar $ /));
    });
  });
});
```

# Introduction to the server-side testing module
We are going to create the unit tests of an application built with the MEAN Stack: Node.js and Express.js in the backend, MongoDB as the database and Angular (with TypeScript) in the frontend.

We are going to test the interaction of the frontend (Angular) with the server or with the clients and how the server interacts with the framework that makes the queries to the database and with the client that makes the requests. We are NOT going to test the database directly.