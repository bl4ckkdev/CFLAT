
![image](https://cdn.discordapp.com/attachments/910436116811878410/977341210228322324/textbutgray.png)

# WARNING: This language is in very early stage.

CFLAT is a simple programming language, it is a hobby of mine and was made with C.
The language is not ready to be released yet, which means that I can only give examples of what it will be like.

It is heavily inspired by C# and Swift too. It will also be used as a scripting system for my game "Rigid".

# Example code
Some important things to note:
- To use certain libraries, you need to use "open" and then specify them.
- "global" means public and "local" means private.
- OnStart() and OnNewFrame() are special methods which run at the start and at every frame.
- To make comments you use "**"

More info is coming soon, when I got more stuff done.

## Simple Calendar that prints the date (and refreshes it)

```swift
namespace ExampleProgram;

open system;
open cf.time;

global class Example
{
   *output to console current date at the start*
   global OnStart()
   {
      global nullable string Date = cf.time.date.ToString();
      system.output("Today's date is: " + Date);
   }
  
  *check if the date has become different since the start*
  global OnNewFrame()
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
     cf.output($"Today's date is: {Date}");
  }
}
```

## Hello World

```swift
namespace ExampleProgram;

open system;

global class HelloWorld
{
  local OnStart()
  {
      system.output("Hello World!");
  }
}
```
