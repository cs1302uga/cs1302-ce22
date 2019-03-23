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

1. Modify the app to look and function like app in the video below.
   
   <a href="https://i.imgur.com/hjbuSHR.gifv">
   <img alt="brad video" src="https://i.imgur.com/hjbuSHR.jpg?play" width="300">
   </a>
   
   The app should do the following while loading an image:
     
   * Display `"Loading..."` while the image app.
   * Diable the button.
   * Not freeze / hang! 
   
1. **Compile and run your code without any errors or warnings.**
   Also stage and commit your changes.
   
1. Tag your commit so that it's easier to checkout at a later
   point in time:
   
   ```
   $ git tag loading
   ```

**CHECKPOINT**
   
<hr/>

[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-nd/4.0/)

<small>
Copyright &copy; Michael E. Cotterell, Brad Barnes, and the University of Georgia.
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-nd/4.0/">Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License</a> to students and the public.
The content and opinions expressed on this Web page do not necessarily reflect the views of nor are they endorsed by the University of Georgia or the University System of Georgia.
</small>
