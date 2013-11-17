# Arrays and Dictionaries

Two of the most important types of data in any programming languages are Arrays and Dictionaries. We'll start by looking at the simpler of the two, arrays.

## Arrays

**Arrays are just lists.** Like `1, 2, 3, 4` or `a, b, c, d`. They're perfect for holding ordered lists of data for accessing later. Let's look at some examples:

    NSArray *arrayOfNumbers = @[1, 2, 3, 4];
    NSLog(@"%i", array[0]);

Let's take a look at what's happening here:

    NSArray *arrayOfNumbers = @[1, 2, 3, 4];

In this line, we're creating a variable of class `NSArray`, with the name `arrayOfNumbers` and saving an array containing `1`, `2`, `3` and `4` in to it. 

The second line,

    NSLog(@"%i", arrayOfNumbers[0]);

outputs the first thing (or *element*) in the array to the console.

> **Why `array[0]`?! It's the first element, not the zeroth.**

> Arrays are '*zero-indexed*'. This means that they start at `0`. For example, if we wanted to get the 3rd element from the array, we would use `arrayOfNumbers[2]`.

Arrays can store **anything** in them and can *sometimes* store a mixture of things too! Let's try saving some words in to an array.

    NSArray *firstNames = @[@"Max", @"Ciara", @"Steve", @"Sam", @"Gareth"];

**Now write the second line to this code that will output the name `Steve`.**

Let's extend the last example, **add the following** line under your `firstNames` variable.

    NSArray *surnames = @[@"Smith", @"Evans", @"Costello", @"Jones"];

Now we have two arrays, `firstNames` and `surnames`. We can use `NSLog()` to output a first name and a surname to make up a name.

    NSLog(@"%@ %@", firstNames[0], surnames[3]);

Should output the name `Max Jones` to the console.