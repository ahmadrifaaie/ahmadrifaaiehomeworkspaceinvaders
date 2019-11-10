# Research on Python and Thonny IDE Tutorial Videos

Python Tutorial Video:

https://www.youtube.com/watch?v=woVJ4N5nl_s

Thonny IDE:

https://www.youtube.com/watch?v=lWaCl0WjNZI

* Helps new users to set up the IDE.
* Covers slightly more advanced functions that can be still picked up by new users

https://www.youtube.com/watch?v=Z0AV6LhShHs

* Covers the most basic functions for new users to ensure easier familiarity with the program
* Very simplified for new users and allows them to be given a walk through as they do the program in the video together with the author. 

# Space Invaders Project on BBC: Microbit

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
* I had encountered issues regarding the coding of the alien which 
- What were your obstacles ?
