# 100 days Code with Chris

# Day 1

## Background

My coding experience comes from scripting in bash/unix and a little in python (~10 years) but no OOP.  Lot of the work I do involves learning how to run open source software to explore data and visualize it.

I have been on my iOS development learning journey since November of 2019.   Most of that journey was using @twostraws Hacking with Swift free series.  His stuff has been great but there are pieces in the material that seem to be missing like how to structure a project, how to connect multiple view controllers; how to pass/store variables between view controllers.   

To learn some of those aspects, I have scoured the web and have been working on several App ideas as learning projects.  I am no where near ready to publish anything.  How to publish is also missing in a lot of the free content out there.  When the spring sale came up, I checked it out and really liked the idea of having community and covering some of the topics missing from the free tutorials online.  

## Current problem

I have been playing with a photoApp idea I have and have been struggling with zoom and pan.  I found a really cool extension for UIimageView that I have expanded but haven't gotten it to work.  I plan on revisiting the scrollview method for doing this.  Why isn't zoom/pan a standard library?

I will post more on this with code as I explore it.  Right now I am just getting familiar with this forum and deciding where I want to start with @Chris2's tutorials.

# Day 1 continued...

* Mar 23, 2021
* 14 Day Beginner Challenge

Decided to start with the Beginner challenge.  My initial foray into swift was using UIKit as swiftUI was still fairly new a year ago and most of the tutorials and solutions you can find online were for UIKit and old versions of swift.  So I am exploring the Beginner's challenge to learn swiftUI fundamentals.

#### Lesson's 1 and 2
The first few lessons are about Apple development and Xcode, which I was mostly already familiar with.  
#### Lesson 3
The third lesson is a remake of the classic "Hello, world" coding problem.  What I found really interesting here is the `command` click of a method to show the swiftUI inspector.  If you are new to swift you will not realize just how powerful a feature this is!  To be able to look at all of the possible ways you can modify the object in a fairly organized manner.  This is a huge advancement over UIKit coding where you are basically at the whim of the apple documentation.

I am anticipating that how you organize your methods will be really important for readability.

Consider making the following

![image|131x75](https://codecrew.codewithchris.com/uploads/default/original/2X/5/54d40e687533bc30c607bb4288186725f3da47ea.png)

* This is much harder to read
```
            Text("Hello, World").padding().background(Color.green).padding().background(Color.yellow)
```
Than
* This is
```
            Text("Hello, World")
                .padding()
                    .background(Color.green)
                .padding()
                    .background(Color.yellow)
```

I will be interested to see what @Chris2 recommends to code formatting in later tutorials.

# Day 2

* Lesson 4 and challenge
* Mar 24, 2021

As I expected, @Chris2 does say to make new lines for the modifiers in the project.  I mentioned before that this is my first exposure to SwiftUI and I find this method of

```modifier.modifier.modier ```

To be very similar to Unix command line where we pipe commands from one thing to the next.

```ls -lha | awk '{print $NF}' | xargs -I xx echo xx```  

I will have to see how well that analogy holds up but if it does then I am going to really enjoy coding in swiftUI.

## Notes from Lesson 4

I have decided to use this forum to take notes as I progress.  I will avoid posting any answers to challenges but will include the modifiers I found useful from the lesson.   I made the challenge much more complicated because I didn't take notes from the lesson and didn't use what he taught. :(

### Objects

* Text("text")
* Image("name")

As of now we can only call images that are in the assets folder of the project, at some point I will want to know how to display it from the phone or the photo's library.

### Stacks

This is how we are organizing content in swiftUI,  Stacks have parameters that can be used to specify alignment and other properties (I haven't looked them up yet), for now I just want to remember that those properties may be easier to accomplish a look than a modifier.

| Stack | Description|
| -- | -- |
|VStack| Vertical stack of Objects|
|HStack | Horizontal Stack of Objects|
|ZStack| Perpendicular Stack of Objects |


### Modifiers

These can be applied to Objects or Stacks.

| Modifier | Description| Other |
| -- | -- | -- |
|.resizable()|Allow resizing| |
|.aspectRatio()|Keep Width and Height Fixed |.fit |
|.cornerRadius()|Modify object corners| |
|.font()| Modify the font size/type| .caption, .largeTitle|
|.padding()| White space around object|.trailing, leading, .top, .bottom|
|.opacity()|Make an object more see through |
|.background()| Can change the color of the background| |
| .foregroundColor()| Change the color of the foreground text/object| |
|.scaleEffect()| You can increase or decrease the size of the Object|
|.frame() | Add a frame around an object| |

FYI: the last two were modifiers I found trying to complete the challenge the hard way. :)


#### Colors
You can probably just name any color after the `Color.` and use it.  There will likely also be a way to include Hex colors. Wonder if I could extend Color to allow that.  That might be fun.

```
Color.white
```

So far so good. On to Lesson 5


# Day 2

* Lesson 4 and challenge
* Mar 24, 2021

As I expected, @Chris2 does say to make new lines for the modifiers in the project.  I mentioned before that this is my first exposure to SwiftUI and I find this method of

```modifier.modifier.modier ```

To be very similar to Unix command line where we pipe commands from one thing to the next.

```ls -lha | awk '{print $NF}' | xargs -I xx echo xx```  

I will have to see how well that analogy holds up but if it does then I am going to really enjoy coding in swiftUI.

## Notes from Lesson 4

I have decided to use this forum to take notes as I progress.  I will avoid posting any answers to challenges but will include the modifiers I found useful from the lesson.   I made the challenge much more complicated because I didn't take notes from the lesson and didn't use what he taught. :(

### Objects

* Text("text")
* Image("name")

As of now we can only call images that are in the assets folder of the project, at some point I will want to know how to display it from the phone or the photo's library.

### Stacks

This is how we are organizing content in swiftUI,  Stacks have parameters that can be used to specify alignment and other properties (I haven't looked them up yet), for now I just want to remember that those properties may be easier to accomplish a look than a modifier.

| Stack | Description|
| -- | -- |
|VStack| Vertical stack of Objects|
|HStack | Horizontal Stack of Objects|
|ZStack| Perpendicular Stack of Objects |


### Modifiers

These can be applied to Objects or Stacks.

| Modifier | Description| Other |
| -- | -- | -- |
|.resizable()|Allow resizing| |
|.aspectRatio()|Keep Width and Height Fixed |.fit |
|.cornerRadius()|Modify object corners| |
|.font()| Modify the font size/type| .caption, .largeTitle|
|.padding()| White space around object|.trailing, leading, .top, .bottom|
|.opacity()|Make an object more see through |
|.background()| Can change the color of the background| |
| .foregroundColor()| Change the color of the foreground text/object| |
|.scaleEffect()| You can increase or decrease the size of the Object|
|.frame() | Add a frame around an object| |

FYI: the last two were modifiers I found trying to complete the challenge the hard way. :)


#### Colors
You can probably just name any color after the `Color.` and use it.  There will likely also be a way to include Hex colors. Wonder if I could extend Color to allow that.  That might be fun.

```
Color.white
```

So far so good. On to Lesson 5

# Day 3 Continued ...

* Mar 25, 2021
* 14 Day Beginner Challenge

## Lesson 8 Structures

Good review of terminology.  Wonder where modifiers fit in this.

* Structure
   * properties = variables
   * methods = functions

I had not heard of `computed properties` yet.  It looks like an enclosure.

# Day 4

* Mar 26, 2021
* 14 Day Beginner Challenge

## Lesson 9 Instances

Course covered the concept of an instance and covered how structs are used within the SwiftUI App

Also discovered that in the CWC+ courses module 1 is the same as the 14 Day Beginner Challenge. Oops.  I could have just started with Module 1. Oh well.

**Question:** Can extend the contenView.swift and add contentViews in a separate file so that the original file doesn't get too long.

## Lesson 10 Buttons

It was nice discussion of Buttons with and without trailing enclosures, text vs images.


# Day 5

* Mar 27, 2021
* 14 Day Beginner Challenge/Module 1

# Module1:Lesson 11 State Properties

State properties seem great.  It is a simplification of coding compared to UIKit.  I went ahead and created a function named `draw()` and put all the commands that occur during the button press into that function. and placed it just below the `@State` declarations.  It works great and keeps the viewController code clean.

# Module 1: Lesson 12 If/else Statements

This was a review for me as they are common in all programming languages. Though I had forgotten how to make random integers so that was nice.

```Int.random(in: 1...100)```  That third `.` always seems to trip me up.


 I was hesitant to do the challenge because I thought it was going to be too easy so it felt dumb.  I did it anyway.  I wanted to see if it I really could do it as quickly as I thought I could.  It was good practice and I spent some extra time finding the SF symbols so I could use some of those as buttons.

I had originally thought I would use `arrow.up` and `arrow.down` but ultimately decided on `heart` and `heart.fill`.

You can download the SF Symbols app that makes it really easy to download from here
* [SF Symbols App](https://developer.apple.com/design/resources/)


![Screen Shot 2021-03-27 at 10.18.40 AM|259x500](https://codecrew.codewithchris.com/uploads/default/original/2X/b/b1d690287c089107964d9dfc6cf7c97b187fa48c.png) 

Looks like there is a bonus challenge in the 14 Day Beginner Challenge.  That is all I have left before proceeding to Module 2 in IOSfoundations.
