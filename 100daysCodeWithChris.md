# 100 days Code with Chris

This is my journal and experience with [Code with Chris](https://codecrew.codewithchris.com/).  Bear in mind I have had about a year of me exploring swift using UIKit on and off.  I am switching over to swiftUI and decided to do a review from the beginning.

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

As I expected, Chris2 does say to make new lines for the modifiers in the project.  I mentioned before that this is my first exposure to SwiftUI and I find this method of

```
modifier.modifier.modier
```

To be very similar to Unix command line where we pipe commands from one thing to the next.

`ls -lha | awk '{print $NF}' | xargs -I xx echo xx`

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

modifier.modifier.modier`

To be very similar to Unix command line where we pipe commands from one thing to the next.

```
ls -lha | awk '{print $NF}' | xargs -I xx echo xx
```  

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

`Int.random(in: 1...100)`  That third `.` always seems to trip me up.


 I was hesitant to do the challenge because I thought it was going to be too easy so it felt dumb.  I did it anyway.  I wanted to see if it I really could do it as quickly as I thought I could.  It was good practice and I spent some extra time finding the SF symbols so I could use some of those as buttons.

I had originally thought I would use `arrow.up` and `arrow.down` but ultimately decided on `heart` and `heart.fill`.

You can download the SF Symbols app that makes it really easy to download from here
* [SF Symbols App](https://developer.apple.com/design/resources/)


![Screen Shot 2021-03-27 at 10.18.40 AM|259x500](https://codecrew.codewithchris.com/uploads/default/original/2X/b/b1d690287c089107964d9dfc6cf7c97b187fa48c.png)

Looks like there is a bonus challenge in the 14 Day Beginner Challenge.  That is all I have left before proceeding to Module 2 in IOSfoundations.

# iOS Foundations: Module 1 Completed!  Day 5 continued ...

* Mar 27, 2021
* 14 Day Beginner Challenge/Module 1

I just finished the slots game.  I was able to do it relatively quickly.  I used an array for the images even though we haven't learned it yet in this course.  I am really liking swiftUI for interface building. I am curious to see how more complicated apps with multiple viewControllers.

I added an if statement to keep the the player from going into negative credits.  It prints an "out of money" because I didn't look up how to form the alert object.   I might add that later.

Now on to iOS foundations Module 2 Recipe App.

![Screen Shot 2021-03-27 at 6.20.15 PM|247x500](https://codecrew.codewithchris.com/uploads/default/original/2X/9/9d0d1360a79c8460689a633f2e0a812d9b48cbd3.png)

# Day 6 M2:L1,L2

* Mar 28, 2021

## iOS Foundations: Module 2: Lesson 1 and 2
## Lesson 1 Overview
## Lesson 2 Arrays  
This was a good review of the possible arrays features.

## Lesson 2 Challenge

Not a bad challenge.  I would have liked to have displayed a card that was being drawn but realized that the assets we were provided doesn't include the full deck!  

**Question:**  Does anyone know if there are any playing card images that are free to use in our apps? Perhaps when we get to drawing shapes we can create them from scratch.

* Equatable was useful in the struct
* Enum for the suits
   * CaseIterable allows for getting a random case from the enum
      * `suit.allCases.randomElement()!)`

I realize we haven't learned enums yet but I had learned this before and it seemed like a logical place to put one but I had always struggled with the best way to use them.  Being able to grab a random element of an enum opens up lots of possibilities.

My code preference is to create functions for the button actions.  I think it looks cleaner.  These functions however, I think need to be inside the struct.  I will have to look into extensions again to see how or if it makes sense to have a separate file as the projects get more complicated for these types of functions. I suppose I could create a button class and call the functions as methods of the class.

```
        VStack {
            Text(text2Display)
                .padding()
            HStack{
                Spacer()
                Button(action: {create()}, label: {
                    Text("Create")
                })
                Spacer()
                Button(action: {draw()}, label: {
                    Text("Draw")
                })
                Spacer()
            }
        }
```

![Screen Shot 2021-03-28 at 10.03.26 AM|230x500](https://codecrew.codewithchris.com/uploads/default/original/2X/4/4c12dacad58f68ed2c8751afe7cee2df78dc7911.png)


# Day 7 M2: L3

This content is all new to me, but he introduces it pretty slowly.  

* NavigationView
* NavigationLink

```
 NavigationView {
            List(array, id: \.self) { arrayElement in
                NavigationLink(
                    destination: Text("Destination"),

                    label: {
                        Text(arrayElement)
                    })

            }.navigationTitle(Text("My List"))
```

## M2:L3 Challenge

This was a straight forward application of what we learned. Mostly cut and paste from the L3 project he showed us how to do.

Question: Is it possible to have the background of the Elements change color if the elements are color names?


# Day 8 IOS Foundation M2: L4

## Loops
* for
* for-in
* while
* repeat-while

Straight forward application in the challenge.  started by copying the code from the previous challenge and modifying accordingly.

I need to start an Array extension file on github to make my array manipulations easier.

# Day 8 iOS Foundation M2:  L5

## Classes

* super
* subclass
* protocol

Great little exercise to review classes.  Good to see the super used in the solution, I  haven't used that much yet in classes that I have made.  I used a switch which I am getting a better handle on how to use.

# Day 8 iOS Foundation M2:  L6

## Structs vs Classes

### Structs (value type)
* more lightweight
* better for read only
* swiftUI views

### Classes (reference type)
* better for read write
* modifying a single instance

Start with Struct then use class if needed.

# Day 8 iOS Foundation M2:  L7 MVVM

## Model
* structs and classes that represent data
   * recipes
   * Shape of the data

## View Model
 * manages state and data user sees
 * use class
 * actual data

## View
 * UI that the user sees


 # Day 9 iOS Foundations M2 L7 Challenge

 Great review of what we learned in lesson 7.  I keep feeling guilty for not being able to do it from scratch without looking for help from what was either covered in the lesson or online.  I suspect this is normal but not healthy.   From now on: **Use the tools at my disposal** .   Google is my best friend and has been for years!

 Also found a great new podcast: https://anchor.fm/sistercodes/episodes/S2-Episode-11-Mobile-Development-with-Mikaela-Caron-et1411 <- @mikaelacaron
 Follow her on twitter here -> [@mikaela_caron](https://twitter.com/mikaela__caron)


# Day 10 iOS Foundations M2 L8/Challenge

We learned
| | Where | description|
| -- | -- |-- |
| @ObservedObject|  View | listening to said Object |
| @ObservableObject|  ViewModel| makes object listenable |
| @Published | ViewModel | Object to update |

#### Challenge

Since the @Published variable is what is changing in the view, we want to make changes in the viewModel rather than inside the button.  Not sure what how Chris was expecting us to try to change the first topping (topping1) since it is inside of the array and that array changed everytime you added a new pizza.

Actually, as long as I refer to the model.array.topping1 I can still get it to change correctly even within the button function.  

I am kind of confused as to what Chris wanted us to do with this part `When this button is tapped, change the "topping1" property of each pizza instance in the ViewModel to "Pineapple".` Other than the correct solution, I am not seeing the way that wouldn't work. It would be nice if this was shown in the answer commented out with `// some code <- this doesn't work`


# Day 11 iOS Foundations M2 L9

#### Optionals

* `?` to declare an optional
* `!` to force unwrap an optional
* `if let a = b {}` to `optional bind` where b is define above as `var b:Int?`

If you declare an optional, you have to set it when you want use it.

```
// declare array is an optional array string
var array:[String]?

// I now want to use it based on some action user took so create an empty array. This is no longer nil but an empty array with an array.count == 0
array = [String]()
```

#### Simple buttons

If you just need a button with text then you can just use the following. It does not contain any formatting.

```
Button("test"){
    print("another Button with action after")
}
```

#### Not just a simple button
To format the button with color and shape or image etc, we need to use this button style.

```
Button(action: {
    array = nil
},label: {
    Text("Nil").foregroundColor(Color.green)
})
```

#### What is the `\.self` thing?

[From the Swift documentation](https://docs.swift.org/swift-book/ReferenceManual/Expressions.html#grammar_key-path-expression)

```
"The path can refer to self to create the identity key path (\.self). The identity key path refers to a whole instance, so you can use it to access and change all of the data stored in a variable in a single step. For example:"
```

oops, apparently, I missed seeing this used in lesson 3 `List Demo`


# Day 12 iOS Foundations M2 L10 Dictionaries

* Apr 4, 2021

#### Dictionaries

Create a dictionary
```
var a = [String:String]()
```

Add/update a key value pair
```
a["E1"] = "John"
```

Remove or unset a key value pair
```
a["E1"] = nil
```

Declaring and initializing key value pairs

```
var employees = ["E1":"John","E2":"Andy"]
```

Loop through dictionary

```
for employee in employees {
  print(employee.key,"",employee.value)
  print(employee.value)
}
```

Loop through dictionary using a tuple

```
for (id, name) in employees {
  print("\(id) \(employee)")
}
```

I had difficulty going through the challenge.  I understand the concepts but it is hard to make it work the way someone else has outlined.  Not sure why.  So I just going to move forward.


# Day 12 iOS Foundations M2 L11 Introduction to JSON

* Apr 4, 2021

#### JSON example
```
[
{
    "name":"Spaghetti",
    "cuisine":"Italian"
},
{
    "name":"Sushi",
    "cuisine":"Japanese"
}
]
```

### JSON Array

```
[
  "Pizza",
  "Sushi"
]
```

### Website where you can validate your JSON

[jsonlint.com](https://jsonlint.com)


# Day 12 iOS Foundations M2 L12 JSON Parsing

This was a great lesson on how JSON parsing works.  It also explains how to load any type of data from a file in the project.

* Apr 4, 2021

#### Grab data from path inside a project


```
let pathString = Bundle.main.path(forResource: "filename", ofType: "extension")
if let path = pathString { } // this block of code makes validates the optional.
let url = URL(fileURLWithPath: path)
let data = try Data(contentsOf: url) // <- this throws requires a do-try-catch block
//can call a decoder once we have the data -- see below  <- this also throws
```
#### do-try-catch block

* required for
  * grabbing contents of a url
  * parsing JSON data
  * any object that requires a throw
    * Error `Call can throw, but it is not marked with 'try' and the error is not handled`

```
do {
let data = try ...

} catch {
  print(error)
}
```

### JSONDecoder

* Create a class to pull in the json
* id should start out as optional
  * can assign ids after parsing (UUID())
* Make it decodable
* mark Decodable Protocal <- the class above with .self

```
let decoder = JSONDecoder()

                do {
                    try decoder.decode([Recipe].self, from: data)

                } catch {
                    print(error)
                }

            } catch {
                print(error)
            }
```

# Day 13 iOS M2L13 The Recipe List App

* Apr 5, 2021

This was a very satisfying tutorial,  So many concepts got consolidated for me.

### static func in a class

If you make a function static in a class you can call it directly without making an instance of it.

```
self.recipes = DataService.getLocalData()
```

### Guard let

This is how it was taught in the lesson.
```
guard pathString != nil else { return [Recipe]() }
```
This is how I have seen it in other tutorials.
```
guard let path = pathString else { return [Recipe]() }
```
A lot of the times it is just `{return}` as this would represent a major probleme and you want to know about it.

The benefit of the first is that you don't have to rename the variable. The benefit of the second is that it seems cleaner to write to me.

### Guard let vs if let

* [Stack Overflow Answer](https://stackoverflow.com/questions/32256834/swift-guard-let-vs-if-let)

The equivelent to the `guard let` statement above would be
```
if let path = pathString {

// code for url, decoder, id generation and then setting to a Published variable.

}
```
* `if let` **nests its scope** meaning that the path variable is only available within the scope of the `{...}`
* `guard let` **the else statement must exit the current scope**
  * So if you put a `guard let` statement at the top of a function you want to call you can verify that the optional you have is not nil before proceeding or otherwise return or set an empty variable.

### Debugging and break points

I never fully appreciated break points until this lesson.  The step-over and resume buttons above the debug console are awesome.

* `po objectname` can be used to printout objects as you step through a for loop or step through the code.
* drag a break point off the side to remove it

# Day14-iOS-M2L14-ForEach-ScrollViews

* Apr 6, 2021

### ForEach

* Used to generate UIView elements
* Written in the same way as List()
* Must be contained in a Stack or container

```
ForEach (array, id: \.self){ r in
  // this code is repeated for each element
  Text(r)
}
```

### ScrollView container

* container that scrolls



# Day14-iOS-M2L15-Recipe-DetailView

* Apr 7, 2021

Remember Navigation view from M2L3 where we only got a "Destination" string?

```
 NavigationView {
            List(array, id: \.self) { arrayElement in
                NavigationLink(
                    destination: Text("Destination"),

                    label: {
                        Text(arrayElement)
                    })

            }.navigationTitle(Text("My List"))
```

Turns out that the `destination:` part can specify an entire view to load instead of just text.  This implies there is a way to also point to different views say with a button.

```
List(model.recipes) { r in
  NavigationLink(
      destination: RecipeDetailView(recipe: r),
      label: {
          HStack(spacing: 20) {
              Image(r.image)
                  .resizable()
                  .scaledToFill()
              Text(r.name)
          }
      })
}
```

In this case we are passing a recipe variable into the destination view struct

Inside that view struct we define a variable to hold the recipe or whatever we decide to pass in and is used to create the view struct.

```
struct RecipeDetailView: View {

    var recipe:Recipe

    var body: some View {


}
```

#### Other useful concepts

* //MARK will create sections you can jump to by clicking on the struct name at the top
  * look for the `App > view > viewController > structName`
* Divider() will place a divider in your view
* .navigationBarTitle(recipe.name) after ScrollView

# Day15-iOS-M2L15-challenge.

* Apr 9, 2021


I was making the challenge, harder than it needed to be.  Inside the `ForEach(model.pizzas) { r in` statement it is possible to display views that take in the `r` variable in this case.  This could really make interpreting the ContentView if multiple subviews were created and then called and supplied the `r` data variable to populate the subviews.

# Day16-iOS-M2L16-finalChallenge

* Apr 10, 2021

**Spoiler Warning: This entry contains solutions to some of the challenges I faced while doing this challenge.  Not the complete code**

Learned today that `NavigationView` is just another container like `ScrollView` or `VStack`  Order of course is important for containers but I get the impression that NavigationView tends to be near or at the Base of a view or collection of containers.

The `NavigationLink` that is often associated with `NavigationView` can be used on any object not just inside a `List`.  In this way we can create a button that then takes you to a different view or text (as in a list) or an image.  This was not clear in tutorials up to this point and required that I google this and learn more about `NavigationView` and `NavigationLink`.  I can imagine this being very frustrating to new learners but an interesting approach to teaching as it forces us to find way to get the information we need to solve the challenge using whatever resource we can find, which is exactly what we will do when we have a project we want to start building and don't know where to start.

```

import SwiftUI

struct ContentView: View {
    var body: some View {
        NavigationView {
            ScrollView {

                NavigationLink(
                    destination: Text("Destination"),
                    label: {
                        Image("Leaf.png")
                            .resizable()
                            .scaledToFill()
                    })//NavigationLink

            }//ScrollView
        }//NavigationView
    }//Body
}//Struct End
```

#### Adding a json file.  

I tried just to create a new swift file and then change the file ending to `.json`.  This did not work.  My pathString always returned `nil`

**Solution**
* Make sure Target Membership is checked in `File inspector`
* Make sure Text encoding is `Unicode (UTF-8)`
* Verify it is listed in the bundle resources
  * main app (click top of the folder that is your app name)
  * Build phases tab
  * Copy Bundle Resources
    * click on the `+` to add it to the list.

This took me well over an hour to figure out.

#### Clearing the cache

Sometimes Xcode does not behave nicely or you don't know why code isn't working, try clearing the cache.

```
command, option, shift K
```

#### Previews are their own view struct

This should be obvious but it isn't always clear that extra code may be needed to make the preview struct to display in a manner that is similar to the ContentView struct if you move a chunk of code outside the content view.   In my case, I had moved most of the card code into its own view struct and the preview struct inside this view would only show one card at a time which skews what it looks like if I want to make additional edits.  So I can mimic what the app does by adding some of the missing components like `ScrollView` and `VStack`

```
struct Card_Previews: PreviewProvider {
    static var previews: some View {
        let model = QuoteModel()
        ScrollView{
            VStack {
            Card(q:model.quotes[0])
            Card(q:model.quotes[1])
            Card(q:model.quotes[2])
            Card(q:model.quotes[3])
            }
        }

    }
}
```
|  |  |  |
| -- | -- | -- |
| ![cards1](100daysCodeWithChris/iosFM2L16/cards1.png)| ![cards1](100daysCodeWithChris/iosFM2L16/cards2.png)| ![author](100daysCodeWithChris/iosFM2L16/author.png)|


# Day-17-TabView

* Apr 17, 2021
* iOS Foundations Module 4

I went through the git repo tutorials by @mikaelacaron and got i mostly working.  I had been version controlling by placing the contents into GitHubs Atom program.  Nice to find another way to do it.

Tab Views look pretty straightforward

1. Create a tab view and in it create the tabs
2. modify the starting page to be this new view controller in the WindoGroup container

```swift
@State var tabIndex = 0  // this will give the index tab value

TabView (selection: $tabIndex) {  //tabIndex requires the $ symbol in order for the State var tabIndex can send information back to this tabview
    //View Objects go in here (what is in the view)

     Text("tab1")
          .tabItem {
              // this is where you describe the tab (view contents)
              VStack {
              Image(systemName: "star")
              Text("tab 1")
            }//VStack
          }//tabItem
          .tag(1)
}
```
