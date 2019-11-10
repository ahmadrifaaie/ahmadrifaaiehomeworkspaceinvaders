# Research on Python and Thonny IDE Tutorial Videos

Python Tutorial Video:

https://www.youtube.com/watch?v=woVJ4N5nl_s

Thonny IDE:

https://www.youtube.com/watch?v=lWaCl0WjNZI

https://www.youtube.com/watch?v=Z0AV6LhShHs

# Space Invaders Project on BBC: Microbit

from microbit import *
import random

spaceship_x = 2
alien_x = random.randint(0,4)
alien_y = 0
missle = (spaceship_x,spaceship_x + 1)
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
