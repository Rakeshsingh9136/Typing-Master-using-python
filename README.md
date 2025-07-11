# Typing-Master-using-python


-:FUNCTION OF PROGRAM:-

The picture that will be used as a background in our software.
Icon.png — This is the icon that will be used as a reset button.
Sentences.txt - A list of sentences will be separated by a new line in this text file.
The main program file, speedtyping.py, includes all of the code.
Typing-speed-open.png – This is the picture that will appear when you first start the game.
To begin, we produced the sentences.txt file, which has various lines separated by a new line.
This time, we'll create the software using an object-oriented approach.


Import the libraries
For this project based on Python, we are using the pygame library. So we need to import the library along with some built-in modules of Python like time and random library.


import pygame
from pygame.locals import *
import sys
import time
import random


draw_text() method

The draw_text() method of Game class is a helper function that will draw the text on the screen. The argument it takes is the screen, the message we want to draw, the y coordinate of the screen to position our text, the size of the font and color of the font. We will draw everything in the center of the screen. After drawing anything on the screen, pygame requires you to update the screen.

show_results() method

The show_results() method is where we calculate the speed of the user’s typing. The time starts when the user clicks on the input box and when the user hits return key “Enter” then we perform the difference and calculate time in seconds.

run() method

This is the main method of our class that will handle all the events. We call the reset_game() method at the starting of this method which resets all the variables. Next, we run an infinite loop which will capture all the mouse and keyboard events. Then, we draw the heading and the input box on the screen.

We then use another loop that will look for the mouse and keyboard events. When the mouse button is pressed, we check the position of the mouse if it is on the input box then we start the time and set the active to True. If it is on the reset button, then we reset the game.

reset_game() method

The reset_game() method resets all variables so that we can start testing our typing speed again. We also select a random sentence by calling the get_sentence() method. In the end, we have closed the class definition and created the object of Game class to run the program.


# Project create Typing Master by using python
startingimage = 'C:\\Users\\rakes\\OneDrive\\Documents\\projectrakeshsingh\\backend.jpg'#'C:\\Users\\rakes\\OneDrive\\Documents\\projectrakeshsingh\\front.jpg'
backgroundimage ='C:\\Users\\rakes\\OneDrive\\Documents\\projectrakeshsingh\\front.jpg' #'C:\\Users\\rakes\\OneDrive\\Documents\\projectrakeshsingh\\backend.jpg'
essay = 'C:\\Users\\rakes\\OneDrive\\Documents\\projectrakeshsingh\\essay.txt'
icon = 'C:\\Users\\rakes\\OneDrive\\Documents\\projectrakeshsingh\\icon.png'


import sys
import time
import random
import pygame
from pygame.locals import *
 
class Test:
   
    def __init__(self):
        self.color_heading = (255,213,102)
        self.color_text = (255,0,0)
        self.color_results = (255,70,70)
        self.w=750
        self.h=500
        self.reset=True
        self.wpm = 0
        self.end = False
        self.active = False
        self.input_text=''
        self.word = ''
        self.results = 'Time:0 Accuracy:0 % WPM:0 '
        self.start_time = 0
        self.overall_time = 0
        self.accuracy = '0%'
        
        
       
        pygame.init()
        self.image_open = pygame.image.load(startingimage)
        self.image_open = pygame.transform.scale(self.image_open, (self.w,self.h))


        self.bg = pygame.image.load(backgroundimage)
        self.bg = pygame.transform.scale(self.bg, (500,750))

        self.screen = pygame.display.set_mode((self.w,self.h))
        pygame.display.set_caption('Typing Master')
       
        
    def draw_text(self, screen, message, y_val ,f_size, color):
        font = pygame.font.Font(None, f_size)
        text = font.render(message, 1,color)
        text_rect = text.get_rect(center=(self.w/2, y_val))
        screen.blit(text, text_rect)
        pygame.display.update()
        
    def get_challenge(self):
        return random.choice(open(essay).read().split('\n'))

    def results_show(self, screen):
        if(not self.end):
            # Calculate time ellapsed 
            self.overall_time = time.time() - self.start_time                
            count = 0
            for i,c in enumerate(self.word):
                try:
                    if self.input_text[i] == c:
                        count = count + 1
                except:
                    pass
            # count is the number of correct typed characters 
            # Calculate accuracy using given formula
            self.accuracy = (count*100)/len(self.word)
           
            #Calculate Words per Minute
            self.wpm = (len(self.input_text)*60)/(5*self.overall_time)
            self.end = True
            print(self.overall_time)
                
            self.results = 'Time:'+str(round(self.overall_time)) +" secs   Accuracy:"+ str(round(self.accuracy)) + "%" + '   WPM: ' + str(round(self.wpm))

            # Draw Icon image
            self.time_img = pygame.image.load(icon)
            self.time_img = pygame.transform.scale(self.time_img, (150,150))
            screen.blit(self.time_img, (self.w/2-75,self.h-140))
            self.draw_text(screen,"Reset", self.h - 70, 26, (255,0,0))
            
            print(self.results)
            pygame.display.update()

    def run(self):
        # everytime we run it should automatically reset the variables
        self.reset_game()
    
        # a variable which shows the state of game whether
        # it is running or not
        self.running=True
        
        # we will run an infinite loop till the running is True
        while(self.running):
            clock = pygame.time.Clock()
            self.screen.fill((0,0,0), (50,250,650,50))
            pygame.draw.rect(self.screen,self.color_heading, (50,250,650,50), 2)
            # Update the text of user input dynamically
            self.draw_text(self.screen, self.input_text, 274, 26,(250,250,250))
            pygame.display.update()
            for event in pygame.event.get():
                if event.type == QUIT:
                    self.running = False
                    sys.exit()
                elif event.type == pygame.MOUSEBUTTONUP:
                    # get the position of mouse pointer x,y
                    x,y = pygame.mouse.get_pos()
                    
                    # position of input box
                    # these x and y values should lie as 
                    # x = [50,650] and y = [250,300] because the timer 
                    # will start when user clicks the input box
                    
                    if(x>=50 and x<=650 and y>=250 and y<=300):
                        self.active = True
                        self.input_text = ''
                        self.start_time = time.time() 
                    
                    # position of reset box
                    if(x>=310 and x<=510 and y>=390 and self.end):
                        self.reset_game()
                        x,y = pygame.mouse.get_pos()
         
                        
                elif event.type == pygame.KEYDOWN:
                    if self.active and not self.end:
                        if event.key == pygame.K_RETURN:
                            print(self.input_text)
                            self.results_show(self.screen)
                            print(self.results)
                            self.draw_text(self.sc reen, self.results,350, 28, self.color_results)  
                            self.end = True
                        
                        # event handler for backspace
                        # i.e simply take the string upto the second last character
                        elif event.key == pygame.K_BACKSPACE:
                            self.input_text = self.input_text[:-1]
                        else:
                            try:
                                self.input_text += event.unicode
                            except:
                                pass
            
            pygame.display.update()
        # clock timer
        clock.tick(60)

    def reset_game(self):
        self.screen.blit(self.image_open, (0,0))

        pygame.display.update()
        time.sleep(1)
        
        # reset all the project variables.
        self.reset=False
        self.end = False

        self.input_text=''
        self.word = ''
        self.start_time = 0
        self.overall_time = 0
        self.wpm = 0
 
        self.word = self.get_challenge()
        if (not self.word): self.reset_game()
                   
        self.screen.fill((0,0,0))
        self.screen.blit(self.bg,(0,0))
        message = "Typing Master"
        self.draw_text(self.screen, message,80, 80,self.color_heading)  
        
        pygame.draw.rect(self.screen,(255,192,25), (50,250,650,50), 2)

        self.draw_text(self.screen, self.word,200, 28,self.color_text)
        
        pygame.display.update()

if __name__=='__main__':
    Test().run()
