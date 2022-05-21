
![cflatats](https://user-images.githubusercontent.com/72033313/169621673-f19a3a71-08bc-43fc-9737-8b22a4ad2651.png)

# WARNING: This language is in very early stage.

CFLAT is a simple programming language, it is a hobby of mine and was made with C.
The language is not ready to be released yet, which means that I can only give examples of what it will be like.

It is heavily inspired by C# and Swift too. It will also be used as a scripting system for my game "Rigid".

# Example code
Some important things to note:
- To use certain libraries, you need to use "need" and then specify them inside of the brackets.
- "global" means public and "local" means private.
- OnStart() and OnNewFrame() are special methods which run at the start and at every frame.
- To make comments you use "**"

More info is coming soon, when I got more stuff done.

## Simple Calendar that prints the date (and refreshes it)

```swift
namespace ExampleProgram;

need {
   cf.system;
   cf.time;
}

global class Example
{
   *output to console current date at the start*
   global OnStart Start()
   {
      global string(global, nullable) Date = cf.time.date.ToString();
      system.output("Today's date is: " + Date);
   }
  
  *check if the date has become different since the start*
  global OnNewFrame Update()
  {
      *if it has then update the date*
      if (Date != cf.time.date.ToString())
      {
          UpdateDate();
          return;
      }

      
  }
  
  global func UpdateDate()
  {
     *set the date to new date and output it*
     Date = cf.time.date.ToString();
     system.output($"Today's date is: {Date}");
  }
}
```

## Hello World

```swift
namespace ExampleProgram;

need {
  cf.system;
}

global class HelloWorld
{
  global OnStart Start()
  {
    system.output("Hello World!");
  }
}
```
