<h1>Section 2 Project 1</h1>

<h2>Overview</h2>

In the [previous project](https://github.com/diycomputerscience/ExerciseMinesweeperSection1Project1), we created a ```Square``` class and a test case for it. Even though we got started thinking about the functionality and responsibilities of the Square class, we did not take it much further than adding an attribute and accessor methods. 

In this project, we will further examine the functionality a ```Square``` should provide to the rest of the system. The functionality of a class, or in other words it's public responsibility is represented by public methods of the class.

To really determine the functionality of a ```Square```, we need to take this discussion to a more concrete level. Let's relate a ```Square``` to an actual Minesweeper game, to understand the functionality of a Square class.

Figure 1, below shows an image of the Minesweeper game that we will make over the next few projects.

![Minesweeper Game Image](https://raw.github.com/diycomputerscience/MinesweeperImages/master/images/BasicDesktopGame.jpg)

_**Figure 1**_

This image helps in gaining a better understanding of what a ```Square``` represents in the MInesweeper game. What we see in the image is the front-end (user interface) representation of squares on a Minesweeper board. However, this UI Square also has a backend representation. That is what the ```Square``` class represents. 

Let's think in terms of the game once again. The functionality of any class is determined by asking relevant questions. Let's ask some questions:

  - _**(developer)** What are the responsibilities of a backend Square ? What can we do with it ?_
  - _**(customer)** We can uncover a Square, or we can mark it as a mine._
  - _**(developer)** Can we uncover the same Square twice ?_
  - _**(customer)** No we cannot._
  - _**(developer)** By the way, what is the initial state of all the Squares ?_
  - _**(customer)** Initially they are all covered._
  - _**(developer)** What happens if a user uncovers a Square which has been marked as a mine ?_
  - _**(customer)** Umm, well a user should be able to uncover a Square which has been marked as a mine. This essentially means they realize, this Square may not be a mine, and now want to uncover it. However, I would prefer this to be a two step transition. So the user does some action, which changes the Square's state from marked to covered, and then they uncover the Square like they would uncover any other Square._
  - _**(developer)** Ok that sounds fair. By the way, should we follow the standard convention and use the left mouse click for uncovering a Square and the right mouse click for marking it as a mine ?_
  - _**(customer)** Yeah,  that sounds great._
  - _**(developer)** Ok so a user will left click on a covered Square to uncover it, and right click on a covered Square to mark it as a mine. How does a user change the state of a marked Square to covered ?_
  - _**(customer)** If a user marks (by right clicking) a Square that is already marked, then the state of the Square changes to covered._
  - _**(developer)** And do we need to allow the user to play the game without using a mouse ? Just with a keyboard ?_
  - _**(customer)** Umm, no, not at the moment. We will do it later, if enough users ask for it._
  - _**(developer)** And I am assuming the game would end if a user uncovers a Square which is a mine ?_
  - _**(customer)** Yes, that's correct._
  - _**(developer)** Alright, I think I understand what we need to do. I am sure we probably need to talk about a lot of other things like how many mines we need to have on the Board, what sort of information we need to show the user as they are playing the game, and several other things. But I suggest that we get started with the simplest thing that works, We would love the get your feedback on every iteration and proceed accordingly. If it's alright with you, I would like to make a small table which shows things a user can do with a Square on the Board and how the Square should react. It's just to make sure I understand what you want us to develop._
  - _**(customer)** Sure that sounds like a great idea._

The developer makes this table which shows the initial state of a Square on the x-axis and actions on the y-axis. The cells show the resulting state of a Square after an action has been performed.

![Minesweeper Game Image](https://raw.github.com/diycomputerscience/MinesweeperImages/master/images/SquareStateChanges.jpg)


The customer is pretty happy with this table. It correctly reflects how a Square should behave when an some action is performed on it.

In the previous project, we have already provided a ```mine``` attribute to the Square. Therefore a Square object knows through the value of the ```mine``` variable, whether it is a mine. To support various states of a Square, we also need to add an attribute called ```state``` which will hold the current state of the Square.


<h2>Steps For This Activity</h2>
We have implemented several test methods in ```SquareTest```, that verify the proper working of the methods that square should have. However, we have not implemented any methods in ```Square```. You have to implement them as described below.

 1. Run SquareTest and notice that there are eight failing test cases. Each test case verifies one distinct functionality of the Square class.
 1. Add code to the Square class to get all these test cases to pass, starting with the first one and going in order.

<h2>Questions to ponder</h2>
 - How should we represent the state of a Square ?
 - Can you figure what the ```setUp``` and ```tearDown``` do in ```SquareTest```

<h2>Learning Goals</h2>
 - How to work with enum types in Java 
 - How to throw an Exception
 - How to declare an Exception in the method
 - How to create a method

