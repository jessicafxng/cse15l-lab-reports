# Welcome to Jessica's Lab 2 Report (:

## How to: Create a Search Engine on a Remote Server

* To create a Search Engine on a Remote Server, we start by implementing the code.

![Image](search-engine.png)

* Searching for a String (1st Block):
The `.getPath()` method takes in the URL that is passed from the paramter. The `url.getPath()` method checks to see if the URL has a `/`. If there is no backslash found, the string "String not found" will be prompted. `url.getPath()` continues to look through the URL until it finds the string `/search`. When the `/search` substring is found, the code will search for the string that will be added. There is a for-loop that loops through the ArrayList and adds a string if it meets the conditions. The `String.format()` returns the llist of the String.

* Adding a String (2nd Block):
To test the code implementation, you can try adding a string to the list. The `url.getPath()` method takes the path from the URL and checks to see if `/add` is in the path. If `/add` is in the path, the code can add the string is prompted. The `getQuery()` checks for the appearance of `?`. When `url.getQuery().split("=")` is activiated, the string will split into an array starting from the `=` sign. To utilize adding a string, the code checks for the word "start" on the left side of the `=` sign and a string on the right side. That said, if the URL does not have `/add` in its path, the string "404 Not Found" will be promoted to the user. 

* This is what the window looks like when the String is not found:

![Image](StringNotFound.png)

* This is what the window looks like when the code encounters an error

![Image](Error.png)

* This is what the window looks like when the String is successfully added:

![Image](StringAdded.png)

## How to: Find Bugs and Fix Them!

* This is the reverseInPLace method in ArrayExamples.java:

![Image](reverseInPlace-BugCode.png)