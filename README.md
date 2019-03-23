# cs1302-ce22 Loading...

> Loading...
>
>
> - Loading...

It is important that graphical applications remain responsive while time-consuming tasks
are being performed. Imagine an mp3 player application that didn't allow you to interact
with the GUI while the current song was playing. That would mean you couldn't pause,
change songs, minimize the app, etc until the song ended. This problem is solved by using
multiple threads of execution. This class exercise introduces the reader to the use of
Java threads to allow seemingly simulataneous actions within an application.

## References and Prerequisites

* [CSCI 1302 JavaFX 8 Bookmarks and Notes](http://cobweb.cs.uga.edu/~mec/cs1302/gui/)
* [CSCI 1302 JavaFX Tutorial](https://github.com/cs1302uga/cs1302-tutorials/blob/master/javafx/javafx.md)

## Questions

In your notes, clearly answer the following questions. These instructions assume that you are 
logged into the Nike server. 

**NOTE:** If a step requires you to enter in a command, please provide in your notes the full 
command that you typed to make the related action happen. If context is necessary (e.g., the 
command depends on your present working directory), then please note that context as well.

### Getting Started

1. Use Git to clone the repository for this exercise onto Nike into a subdirectory called `cs1302-ce22`:

   ```
   $ git clone --depth 1 https://github.com/cs1302uga/cs1302-ce22.git
   ```

1. Change into the `cs1302-ce22` directory that was just created and look around. There should be
   multiple Java files contained within the directory structure. To see a listing of all of the 
   files under the `src` subdirectory, use the `find` command as follows:
   
   ```
   $ find src
   ```
### Exercise Steps

1. **Compile and run the starter code without any errors or warnings.**
   Specify `bin` as the default package for your compiled code.
   
   * If you have trouble running the starter code, then consult the 
     [CSCI 1302 JavaFX Tutorial](https://github.com/cs1302uga/cs1302-tutorials/blob/master/javafx/javafx.md).
     
An example image and the overall contaiment heirarchy for this app can be seen below:

<table>
   <tr>
      <td><img src="https://github.com/cs1302uga/cs1302-ce19/blob/master/ScreenShot.png?raw=true" width=300>
</td>
      <td><pre><code>                                        --|
                         Stage            |
                           |              |
                         Scene            |
          |--              |              |
          |               VBox            | Overall
          |               / \             | Containment
   Scene  |              /   \            | Hierarchy
   Graph  |            HBox  ImageView    |
          |            / \                |
          |           /   \               |
          |    TextField  Button          |
          |--                           --|
   </code></pre></td>
   </tr>
   </table>

1. There's one small difference between this app and the original `ImageApp`: we have 
   introduced an intentional 5 second delay to the starter code. Load one of the following
   URLs to see the delay:
     * `http://cobweb.cs.uga.edu/~mec/cs1302/gui/pikachu.png`
     * `http://cobweb.cs.uga.edu/~mec/cs1302/gui/brad.jpg`
     * `http://cobweb.cs.uga.edu/~mec/cs1302/gui/SuccessKid.jpg`
 
While our delay is artificial, time-consuming code is common in the real world (as in the mp3 app 
discussed earlier). In this exercise, we will modify the app so that it remains responsive to user
actions while loading the image and also indicates to the user via a `Text` object that the image is
loading.

1. Modify the app by adding an `HBox` object which will contain a `Text` object as seen in the
   containment heirarchy below. We will use this `Text` object to indicate when an image is loading.
   
   ```                                            --|
                         Stage                    |
                           |                      |
                         Scene                    |
          |--              |                      |
          |               VBox                    | Overall
          |               / \  \___________       | Containment
   Scene  |              /   \             \      | Hierarchy
   Graph  |            HBox  ImageView    HBox    |
          |            / \                  |     |
          |           /   \                 |     |
          |    TextField  Button          Text    |
          |--                                   --|        
   ```          

1. Set your `HBox` container to have a preferred width of 20.
   
1. **Recompile and run.**

1. Stage and commit your changes.

**CHECKPOINT**

1. Now that you have your app looking good, let's make it do stuff. 

1. In the `start` method of your `ImageApp` class, declare a variable
   of type `EventHandler<ActionEvent>` called `loadHandler`, then assign
   to it, using a lambda expression, an implementation of
   `EventHandler<ActionEvent>` that prints out the text of the
   `TextField` to standard output (i.e., the terminal).
   **Recompile before continuing.**
   
   * Take special care that you import the correct `ActionEvent` class,
     as a quick Internet search may recommend the wrong one!
     Consult the 
     [API Documentation](https://docs.oracle.com/javase/8/javafx/api/toc.htm) and 
     [referenced bookmarks](http://cobweb.cs.uga.edu/~mec/cs1302/gui/)
     to determine the import statements that are needed.
     
1. Once your app is able to print the text from the `TextField` to 
   standard output, ammend the code that is also creates an `Image`
   object using the supplied URL, then sets the `image` propery of
   the `ImageView` using the appropriated setter method.
   **Recompile before continuing.**
   
   * Here are some URLs to try when testing your program:
   
     * `http://cobweb.cs.uga.edu/~mec/cs1302/gui/pikachu.png`
     * `http://cobweb.cs.uga.edu/~mec/cs1302/gui/brad.jpg`
     * `http://cobweb.cs.uga.edu/~mec/cs1302/gui/SuccessKid.jpg`
   
   * Your program should not crash when supplied invalid input. Use
     exception handling, as needed, to make the experience nicer
     for the user. While we will explore creating popup windows
     and dialogs in the future, it is sufficient to print a friendly
     error message to standard output instead of letting the
     program crash or display a stack trace.
     
1. Stage and commit your changes.

1. If you completed the steps correctly, your app should not only look 
   similar to the screenshot provided above, but it has the desired
   functionality. Congratulations on a good looking, functional app!
        
**CHECKPOINT**
   
<hr/>

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-nd/4.0/)

<small>
Copyright &copy; Michael E. Cotterell, Brad Barnes, and the University of Georgia.
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a> to students and the public.
The content and opinions expressed on this Web page do not necessarily reflect the views of nor are they endorsed by the University of Georgia or the University System of Georgia.
</small>
