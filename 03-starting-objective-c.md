# Starting Objective-C

Objective-C is the main programming language used to create apps for iPhone and iPad and what we will be focusing on in this book. There are *loads* of other ways to create apps for iOS now including Javascript frameworks and RubyMotion. But Objective-C is no more difficult than any of these languages, it just takes effort to learn it just like any other language.

```
Code samples will be presented like this in fixed-width font.
```
> Notes and Gotchas! Will be presented like this.

Objective-C is the language used to create iOS apps natively, but it by no means its only use. Objective-C is a multipurpose programming language that can be used to write Mac apps, iOS apps and even text-based (command line) applications. In this chapter we will learn how to write Objective-C applications that run in the command line. They will execute some commands and output a result in text. Learning how to do this is really important and will give you a grounding in the skills required to produce an app for iOS.

## Create a Command Line (CLI) Project

Click 'File', 'New' and select 'Project'. This time, instead of an 'Empty Project' select 'Command Line Tool' from the 'OSX > Application' group. Fill out the project information as you did and select 'Foundation' as the type.

![CLI Options](https://s3-eu-west-1.amazonaws.com/ios-book/03-starting-objective-c/cli-options.png)

The project navigator will present you with a much smaller group of files. For this chapter, all of our work will be done in `main.m`. Currently, there isn't much in this file:

    #import <Foundation/Foundation.h>

    int main(int argc, const char * argv[])
    {

        @autoreleasepool {
            
            // insert code here...
            NSLog(@"Hello, World!");
            
        }
        return 0;
    }

Let's go through the code so far and explain what's happening:

    #import <Foundation/Foundation.h>

The `#import` directive is something used a *lot* in Objective-C. If you split up your projects in to multiple files (and you will), the `#import` directive

> Lines that appear at the top of files, prefixed with a `#` symbol are called *compiler directives* or just *directives*.

Next...

    int main(int argc, const char * argv[]) {
        // Rest of the code here
    }

This is where the magic happens. This is a **function.** Don't worry about exactly how this works, but anything inside the `{ }` symbols here will be *executed* when the application starts.

Next...


    @autoreleasepool {
            
        // insert code here...
        NSLog(@"Hello, World!");
        
    }
    return 0;

We can safely ignore the `@autoreleasepool` block here as this will not apply to our iOS application. Just trust that it saves the computer from running out of memory! iOS deals with this for us, but command line applications do not. Inside that block is the following lines:

    // insert code here...
    NSLog(@"Hello, World");

In Objective-C, any line that begins with `//` is known as a **comment**. This is a line that is ignored by the machine. It can be helpful for annotating your code if you're working as part of a team. *Commenting code effectively is a skill. Do not underestimate it!*

The next line, `NSLog(@"Hello, World")` simply outputs the phase `Hello World`. Try it out now! Press the **Play** button in the top-left hand corner of XCode and see what is output.

> Every single command in Objective-C ends with a semicolon. This tells the computer that this is the end of the time.

![Debugger output](https://s3-eu-west-1.amazonaws.com/ios-book/03-starting-objective-c/debug-hello-world-output.png)

Using `NSLog(@"Some text...")` will output whatever is it inside the quotes to the console.

> *Why `NSLog`? Why not just `Log`?*
Remember back to when we had to set the 'Class Prefix' of our projects. `NSLog` is written by Apple, and the class prefix for most of their classes is `NS`. This stands for `NextStep` and is a nod to where Objective-C evolved from.

### Extending using Variables

So this is a very contrived example, time to make it a bit more complex by introducing a variable.

**Variables** are just a way of storing information in code to reuse it later. They're storage that can *vary*. They can be very helpful so that you don't have to repeat yourself. Take the following example. (Assume it's wrapped in an `@autoreleasepool` block as before.)


    NSLog(@"Hi there");
    NSLog(@"Hi there");
    NSLog(@"Hi there");

As you'd expect, this outputs the phrase `Hi there` three times. Not very interesting.

Now imagine, you want to change your code so that it outputs the phrase `Hello there`. You're going to have to go through and change the code to this.

    NSLog(@"Hello there");
    NSLog(@"Hello there");
    NSLog(@"Hello there");

That probably took you 10-20 seconds. Now pretend that your code is hundreds of thousands of lines of code, sprawled over hundreds of files. This sort of inefficiency just *isn't practical!* So let's use a *variable* to store the message so that if we need to change it again, we just need to change it in one place.

    NSString *message = @"Hello there";
    NSLog(message);
    NSLog(message);
    NSLog(message);

Cool, huh? Now, if you need to change the message that is output three times, change it in one place and you're finished.

So how did that work? We created a variable, and all variables look like this:

`TypeOfVariable *variableName = the value of the variable`

Remember this pattern, you'll use it a lot. 

Here, `TypeOfVariable` is an `NSString`. And `NSString` is just some words, letters of numbers. In Objective-C, `NSString`s are wrapped up in `@""`. Another word for `TypeOfVariable` is a `Class`. Remember this.

These are valid `NSString` objects:

1. `@"Hello"`
2. `@"12345"`
3. `@"ABZ£%^&$SHJKDUD"`

These are **not** valid `NSString` objects:

1. `23`
2. `180 / 2`

These are different types, we'll come to these later.

The `*variableName` is just the name you want to be able to refer to your variable as later. You should pick a sensible, descriptive name for your variables and it should be written in camel case. 

These are good names for variables:

1. `outputMessage`
2. `sendButton`
3. `dateOfBirth`

These are **bad** names for variables:

1. `button` - Not descriptive enough. Which button? What does it do?
2. `number` - Not descriptive enough. What number? What does it represent?
3. `PersonAge` - Not camel case. Should be `personAge`.
4. `date_of_birth` - Not camel case. Should be `dateOfBirth`.

> Noticed the `*` next to the variable? This is called a pointer. Don't worry about this yet, just remember the rule that most variables you create will be prefixed with an asterisk. You need it when you create a variable, but not when you're using it. Study the example carefully, variables and pointers are *really* important.

### Activities

1. Try changing the text that is output and running the application again.
2. Change the code so that it outputs several things.
3. Create several variables and output them.


