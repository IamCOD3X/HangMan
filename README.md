# HangMan Game

In this project, we have created a Hangman game with the help of the “Pygame” module in Python language. Basically, it is a guessing game. The player tries to guess it by suggesting letters within a certain number of guesses. If the guessed word is correct within the given limit then the player got wins. If the player selects the wrong letter then every time the wrong selection one of the body parts of the hangman will appear and thus when the guessed limit is over the player will lose the game.

# Explanation:

Firstly, we will import the necessary libraries. So, for this project, we will make use of “Pygame”, “random”, “time” and “sys” module. If it’s not there in your system then install it by using the following command in your cmd: “pip install <library name>”. After importing the Pygame module the next step is to initialize the module and with the help of “.init()” we will do so.

To set the frames per second for our window will make use of “pygame.time.Clock()” of the “time” module. With that in the next step, we will define the width and height of our game window

Now, to fulfill the most basic need to develop the game, we will use “pygame. the display.set_mode((width, height))” to create the game window. After creating, the title and icon need to be added to make it user-friendly. So with the help of “pygame. display.set_caption()” and “pygame. display.set_icon()” will do so. To load the picture of the icon to this project we will use “pygame.image.load(‘image link’)”.

In the next step, we will declare some variables which will help us out while creating the buttons. Thus, we want 2 rows, and 13 columns, the gap between them should be 20 and the size is 40 since that will be a square. So, first of all, we will make the boxes and then we will place the letters inside the boxes. Now, for the box we will run a nested loop for rows and cols, under that we will mention the x and y position of the boxes. To make the box we will use “pygame. rect(x,y, size, size)”. This command will create a single box and to make sure to display all the boxes we will create an empty list of boxes under the loop after creating every box we will append that in the boxes list by the “.append()” function.

Since we know that, to display every functionality on the game window we have to create a game loop. For that, we have declared a running variable. Initially, the value assigned to the variable is False. With the help of the “while” loop, we will process our game loop. With the help of “pygame.event.get()” we will run a loop for the events. Under this event loop, we will process the type of the event under the if-else ladder with the help of “.type”.

Firstly, we will check for a quit event with the help of “pygame. QUIT” and to show every single thing on the screen we will make use of “pygame. display. update()”.

Under this loop, we will run one for loop of the boxes to be shown on the game window. So we will draw the boxes under that loop.

The next step is to place the letter in the box, for that we will create an empty list named buttons. Now, we will run a for loop for the index and box. Since we know that for ‘A’ the ASCII Code is 65 and if we will add 1 into that we will get the 26 letters of the alphabet. So under that loop, we will declare a variable letter under which with the help of ASCII code we will get our letters, and we will append every single button in the buttons list.

Since, we will need a font as well and with the help of “pygame.font.Sysfont(‘name’,’ size’)” will do so. In the game loop firstly we will render the font with the help of “.render()” and then we want the letter to be at the center of the box so for that we will use “.get_rect(center=(positions))” and after that, we will blit the font on the screen with the help of “.blit()” function.

After drawing the boxes now the next step is to play with words. For that firstly we will create an empty list named words. Now to display the text we will again run a for loop for letters in the word. We will also create another empty list named as guessed which will tell the letter that is guessed. Under the for loop, if the letter exists in the word then we want the string that will gonna appear to have that letter otherwise we will just add an underscore.

For the letters also we need to make a font and will do so with the same function as mentioned above, then we will render it and blit it on the screen. After doing so you will see that the game window will contain the dash spaces.

Now, for the buttons to be get clicked we will run an event loop under the game loop. First of all, we will check the event type as “MOUSEBUTTONDOWN”. If the event condition got satisfied then we want the mouse position, so with the help of “event. pos,” we will get the position. Now to check that the clicked position is in the button surface we will make use of ‘.collidepoint()” . If the clicked letter is not in word then we want our hangman status to be changed so for that we will initially declare a variable named as “hangman_status” and we will initialize it to 0. Now if that clicked letter is not in the word we will increase the hangman status by 1 and if the hangman_status reaches 6 we want the game to get over.

If the clicked letter is in the word then we will append that letter into the guessed list and we will remove that button from the buttons list by using the “.append()” and “.remove()” properties.

Now simultaneously when the user clicks the wrong letter we also want the hangman status to be shown on the game window via different stages of hangman. For that, we will run an if-else ladder for the same and we will load different images for different stages by using “pygame. image.load(‘image link’)” .

To state the win and lose condition we will declare a winning variable initialized as true. For every letter that is not guessed, we want the win to be false and if the win is true then the message is to be displayed stating the win for the user and if it is false then the message of getting lost should be displayed.

To display these messages again we will make use of the render and blit function under the game loop with the same steps.

For a user to guess different and random words, we will store some words in the words list, and with the help of the “random. choice()” of the “random” module, we will do so. So every time whenever a user will start the game a new random word will be there for the user to guess.

By Following all these steps accordingly you can easily make a Hangman game. Do the code and play!
