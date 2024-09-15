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