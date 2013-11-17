# If, else, for... Control Flow

## Conditional (if) statements

Often it's very helpful for be able to only run code if a certain condition is met. For example,

    if x > y
      do this
    otherwise
      do this

This is very easily achieved in Objective-C using the *conditional* or *if* statement. 

**Consider the following example:**

    int x = 10;
            
    if (x < 0) {
        NSLog(@"x is less than zero");
    }

Before running this code, think carefully about what will happen. Will `x is less than zero` appear in the console or not? What will you have to do to change the outcome? This is a classic conditional statement and all conditional statements look the same.

    if (something to check) {
        do this
    }

The `if` statement checks if what is inside the brackets is true and if it is, runs the code inside the `{ }`. Otherwise, it just skips it.

**Now consider the next example:**

    int x = 10;
            
    if (x < 0) {
        NSLog(@"x is less than zero");
    } else {
        NSLog(@"x is not less than zero");
    }

Execute this code now. What do you expect to happen? What happens if `x = 0`?

**One final example to consider:**

    int x = 10;
            
    if (x == 0) {
        NSLog(@"x is zero");
    } else if (x == 1) {
        NSLog(@"x is one");
    } else {
        NSLog(@"x is not one or zero");
    }

Read it carefully, see if you can guess what will be executed and alter the result.

### Examples of things to check in if statements

* `x == y` - Checks if x is equal to y. *(Note the double equals signs)*
* `x < y`  - Checks if x is less than y.
* `x > y`  - Checks if x is greater than y.
* `x >= y` - Checks if x is greater than **or** equal to y.
* `x <= y` - Checks if x is less than **or** equal to y.
* `x != y` - Checks if x is **not** equal to y.
* `x == y && x < 0` - Checks if x is equal to y **AND** that x is less than zero.
* `x < y || x == 10` - Checks if x is less than y **OR** exactly equal to 10.
* `x < 10 && x > 0 && x*x < 10` - Checks if x is less than 10 **AND** that x is greater than zero **AND** that x squared is also less than 10.

*Now go and write some if statements and try out some of these...*

## Loops

The next important concept to understand in any programming language is the `iterator` or `loop`. Loops simply allow you to run the same piece of code a specified number of times. 

**Consider the following example:**

    for (int x = 1; x <= 10; x++) {
        NSLog(@"%i", x);
    }

**WHOA!** What's happening here? That first line just like a mess of symbols and numbers, but it's really very simple! *Run the code now and see what it outputs to the console.* So, it just outputs the numbers 1 - 10, one at a time. Time to look at what this code is doing.

**This line is the most important:**

    for (int x = 1; x <= 10; x++) {

This is basically saying 'do what's inside `{ }` 10 times'. How can that be possible? Let's take a more general example:

    for (initializer; conditional; post-execution statement) {

Each `loop` has three sections:

* The `initializer` which is where we create a variable to hold our loop counter. In our example we create a variable called `x` and store the number `1` in it.
* The `conditional` is something that is checked before the loop is run. If it is true then the loop is run, otherwise the loop finishes. In our example, we're just checking that `x` is less than or equal to 10.
* The `post-execution statement` happens after each time the loop is run. In our example, every time the loop is run, `x` is increased by one. (`x++` is shorthand for `x = x+1`, don't forget this!)

So in our example, we start with `x` being equal to `1`. We run the code inside our loop (just outputting `x`) and then increase `x` by one until `x` equals `10`. Then the loop stops.

### Activities

1. Try altering the loop so that the numbers 1 - 20 appear in the console.
2. Try altering the loop so that the numbers 50 - 1 appear in the console.
3. Try altering the loop so that only the odd numbers between 1 - 99 are output to the console.
