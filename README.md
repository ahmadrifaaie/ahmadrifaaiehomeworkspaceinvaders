# Research on Python and Thonny IDE Tutorial Videos

Python Tutorial Video:

https://www.youtube.com/watch?v=woVJ4N5nl_s

* Very informative - includes set up of Python software, basic functions and slightly advanced function
* Provides walk through of example programs that can be done by the user
* One of the shortest videos that I can find that covers most of the Python software.

Thonny IDE:

https://www.youtube.com/watch?v=lWaCl0WjNZI

* Helps new users to set up the IDE.
* Covers slightly more advanced functions that can be still picked up by new users

https://www.youtube.com/watch?v=Z0AV6LhShHs

* Covers the most basic functions for new users to ensure easier familiarity with the program
* Very simplified for new users and allows them to be given a walk through as they do the program in the video together with the author. 

# Space Invaders Project on BBC: Microbit
The current coding below has only the basic functions of dodging the aliens but the missle function has yet to be completed.

    from microbit import *
    import random


    alien_x = random.randint(0,4)
    alien_y = 0
    missle = (spaceship_x,spaceship_x + 1)
    spaceship_x = 2
    random.seed()

    while True:
    
    display.clear()
    display.set_pixel(spaceship_x, 4, 9)
    display.set_pixel(alien_x, alien_y, 9)
    
    if button_a.was_pressed() and spaceship_x > 0:
        spaceship_x = spaceship_x - 1
    if button_b.was_pressed() and spaceship_x < 4:
        spaceship_x = spaceship_x + 1

    if alien_y < 4:
        alien_y = alien_y + 1
    else:
        if alien_x == spaceship_x: 
            break
        else:
            alien_y = 0
            alien_x = random.randrange(5)
            display.set_pixel(alien_x, alien_y, 9)
    if accelerometer.was_gesture("shake"):
        display.set_pixel(missle)
    
    if missle == alien_x and alien_7:
            display.clear()
            display.set_pixel(alien_x, alien_y, 9)
    
       
        
    sleep(500)
    
    display.scroll("GAME OVER!", loop=True)

- What were your problems and how did you remedy them (give at least 2)
1. I encountered issues in trying to set up the alien movement.
Remedy: 
2. I had troubles in trying to set up the missle system to shoot at the alien.
Remedy:

- What were your obstacles ?
1. The biggest obstacle for me was making the missle system which proved to be difficult to set up as most of the guides online use a more simplified 'block-type' coding.
2. Another was trying to overcome the issue of readibility, as my code was too long-winded and wordy, I have to simplify it which proved to be difficult due to my lack of experience in coding.

- Give a tip to readers on how to make your program succeed 
1. Always have a structure which acts as your step by step guide as you eventually code and execute.
2. Always do thorough research on possible functions that may help or simplify your program so it can be readable and easy to fix should you encounter issues. :)
