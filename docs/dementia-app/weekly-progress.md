# Weekly Progress

This section details my weekly progress on my app for those with dementia.

## 9/9 - 9/13

### General Plan

For this week, I wanted to develop the basis for my project, the image storing system. Rather than starting directly with that, I decided to implement the card game first so that I could store images best to accomodate for the different activities in the app. 

Thus, I created the base for a game where cards lay face down and the user selects 2 cards. Each card will have a family member, and the user picks 2 cards. If they match, then the match is collected.

Note that I did not fully implement the card game but rather the structure for it and a prototype for the image storing system.

### CardGame Class

Much of my work this week was done on the CardGame class, following the general plan. I created a method called "initializeGame", which performs the setup for a card game and starts the gameplay loop. Here is a snippet of the code:

```Java
public void initializeGame() {
    assignImages();
    shuffleCards();
    int attempts = 20;
    for (int i = 0; i < attempts; i++) {
        selectTwo();
    }
    scan.close();
}
```

The assignImages() method was very hard to make, as I had to mold the image system around that. shuffleCards required simply the Collections.shuffle() method to work, and selectTwo() was fairly easy to make given an ArrayList of cards.

### Card Class

I needed to define a Card class so that the ArrayList of cards could store individual objects with an image, the person's name, and the status of the card being flipped or not.

I created a boolean method matches() to return whether the Card has the same person as another. I also used Constructor overloading to make two possible card states:
- One constructor takes a BufferedImage for the image, a String for the person's name, and an int for the card number. This creates a card that can be flipped.
- The other constructor takes no argument and is solely for removed cards. This may not be necessary as of now.

### ImageLibrary Class

The ImageLibrary class is used to read a data file stored locally (to allow for data to be saved over multiple runs of the program) and the ability to read and store images on the computer. In the assignImages() method of ImageLibrary, the *data.txt* file is read. Note that ImageLibrary has an instance variable *people* which stores instances of **Person**. The Person class stores an ArrayList of BufferedImages, where each image for the respective person in *data.txt* are stored.

### data.txt

data.txt is formatted as follows:
- A line for a person's name is indicated by starting with **#**
- Other lines are the path to an image of that person
- The image paths for a person are directly under the heading for that person

Note that the user will not have to input this manually, as I will later make a system where images can be input and *data.txt* can be updated based on the user's input.

## 9/16 - 9/20

### General Plan

For this week, I wanted to primarily implement a GUI for the card game and have user interactability with that GUI, including clickable cards.

## CardGameGUI Class

I added a new class to the program which created a GUI for the card game. I used Swing and JFrame to make the GUI, with the Frame being stored as an instance variable (Note that the frame was later moved into a more general class). 

I made each of the cards buttons on one layer of a JLayeredPane, with the other layer displaying the information about a person when a match was made. I also created a class CardListener implementing the ActionListener class to tell what to do when a card was clicked. On the other layer of the JLayeredPane, I intended to display the information about a person when a match was made (added next week). Here is the temporary GUI:

![https://connor-cruz.github.io/images/CardBlank.jpg]

![https://connor-cruz.github.io/images/CardClicked.jpg]

Note that the front of the cards aren't fully finished, as I intend for the user to crop the image as desired to fit nicely on the card.

## 9/23 - 9/27

### General Plan

I planned for the game to check if the player won the game, as well as to display information and pictures of a person when a match is made. I also wanted to prevent the player from clicking the same card twice when matching.

## 10/7 - 10/11

## General Plan

I planned to create a class for inserting images and people into data.txt. If time permitted, I also wanted to create a GUI for inserting the images with the ability to let the user navigate their files and select certain images.