# Getting to know XCode

> You should have XCode installed by now. If not, download it from the Mac App Store. (It's free!)

Once XCode is installed on your Mac, **open it up** and you should be presented with a screen like this. Make sure you're running Version 5 or part of this book may be inaccurate.
![XCode Start Screen](https://s3-eu-west-1.amazonaws.com/ios-book/02-xcode/xcode-start.png)

We're not going to do any coding in this chapter. We're just going to understand how XCode works and try to understand how it can make iOS development a seamless process.

## Let's get started! Creating a Project

Firstly, **click on 'Create a new XCode project'**. This will bring up a list of templates we can use to start working on.

![List of templates](https://s3-eu-west-1.amazonaws.com/ios-book/02-xcode/xcode-templates.png)

For the purposes of learning how XCode works, we'll just create an empty project, since we're not writing any code just yet.

After **selecting 'Empty Project'**, enter some information about your app. 

* *Project Name* is simply the name of your application.
* *Organization Name* is the name of your company (or your name).
* *Company Identifier* is the identifier for your company (or you). It is usually comprised of a sort-of backwards URL. For example, if your website address is `http://supercoolwebsite.com` your identifier would be `com.supercoolwebsite.myawesomeapp`.
* *Class Prefix* is a (usually) two-letter code that will prefix every file in your project. This is to avoid namespacing issues. For personal projects, it will normally be your initials.
* *Devices* can be either iPhone, iPad or Universal. This is fairly self-explanitory.
* *Use Core Data* should be left unchecked for now. We'll come on to Core Data much later in this book.

![Project option list](https://s3-eu-west-1.amazonaws.com/ios-book/02-xcode/xcode-project-options.png)

**Clicking 'Next'** will let you choose where to save the project. **Save it** somewhere you'll be able to find it again.

## Navigating the Code View

XCode has three main views. the **Code View**, the **Interface Builder** (IB) and the **Settings View.**

This is the Code View
![Code View](https://s3-eu-west-1.amazonaws.com/ios-book/02-xcode/xcode-code-view-overview.png)

It has four main sections:

* The **Code Editor** is where we write our code. This is where the magic happens. We'll be getting to know the code editor very well, so get used to using it. You can edit the colour scheme in the XCode preferences. Many developers prefer certain colours when programming, you'll find your own preference over time.

* The **Sidebar**. This changes all the time depending on the context you're currently in. In the Code Editor it will give hints about various programming functions (methods) that you're using.

* The **Device Manager** is where you choose a device or iOS simulator to try our your app in. The big play button does what you think it does. Hit it now if you want and prepare to be amazed at your first app running in an iPhone simulator! *(Obviously, it won't actually do anything.)* 

* The **Project Navigator** on the left-hand side is our organiser. It keeps files tidy and in folders, just like anywhere else on your computer.

> **Gotcha!** The things that looks like folders in the Project Navigator are *not really folders!* If you look at your project folder in Finder, you'll see that all of these folders aren't really there. XCode just uses them to organise your files.
