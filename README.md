# Typing-Master-using-python
A Python Typing Speed Test is good for the student or beginners to improve their typing test skills, and also in this Python Typing Game is good for the beginners in python programming world, because the syntax is easy to learn and to understand.


PYTHON 

Python Language Introduction 

Python is a widely used general-purpose, high level programming language. It was initially designed by Guido van Rossum in 1991 and developed by Python Software Foundation. It was mainly developed for emphasis on code readability, and its syntax allows programmers to express concepts in fewer lines of code.

Python is a programming language that lets you work quickly and integrate systems more efficiently. 

Python is a high-level, interpreted, interactive and object-oriented scripting language. Python is designed to be highly readable. It uses English keywords frequently where as other languages use punctuation, and it has fewer syntactical constructions than other languages.

 • Python is Interpreted − Python is processed at runtime by the interpreter. You do not need to compile your program before executing it. This is similar to PERL and PHP.

 • Python is Interactive − You can actually sit at a Python prompt and interact with the interpreter directly to write your programs. 

• Python is Object-Oriented − Python supports Object-Oriented style or technique of programming that encapsulates code within objects. 

• Python is a Beginner's Language − Python is a great language for the beginner-level programmers and supports the development of a wide range of applications from simple text processing to WWW browsers to games.

 History of Python

Python was developed by Guido van Rossum in the late eighties and early nineties at the National Research Institute for Mathematics and Computer Science in the Netherlands. Python is derived from many other languages, including ABC, Modula-3, C, C++, Algol-68, Small Talk, and Unix shell and other scripting languages

Python is copyrighted. Like Perl, Python source code is now available under the GNU General Public License (GPL). Python is now maintained by a core development team at the institute, although Guido van Rossum still holds a vital role in directing its progress.

Python Features 
Python's features include – 
• Easy-to-learn − Python has few keywords, simple structure, and a clearly defined syntax. This allows the student to pick up the language quickly. 

• Easy-to-read − Python code is more clearly defined and visible to the eyes.

 • Easy-to-maintain − Python's source code is fairly easy-to-maintain. 

• A broad standard library − Python's bulk of the library is very portable and crossplatform compatible on UNIX, Windows, and Macintosh.

 • Interactive Mode − Python has support for an interactive mode which allows interactive testing and debugging of snippets of code.

 • Portable − Python can run on a wide variety of hardware platforms and has the same interface on all platforms. 

• Extendable − You can add low-level modules to the Python interpreter. These modules enable programmers to add to or customize their tools to be more efficient.

 •Databases − Python provides interfaces to all major commercial databases.

 • GUI Programming − Python supports GUI applications that can be created and ported to many system calls, libraries and windows systems, such as Windows MFC, Macintosh, and the X Window system of Unix. 

• Scalable − Python provides a better structure and support for large programs than shell scripting. Apart from the above-mentioned features, Python has a big list of good features, few are listed below – 

• It supports functional and structured programming methods as well as OOP.

• It can be used as a scripting language or can be compiled to byte-code for building large applications. 

• It provides very high-level dynamic data types and supports dynamic type checking. 

• IT supports automatic garbage collection. 

• It can be easily integrated with C, C++, COM, ActiveX, CORBA, and Java. Python graphical user interfaces (GUIs).

• Tkinter − Tkinter is the Python interface to the Tk GUI toolkit shipped with Python. We would look this option in this chapter. 

• wxPython − This is an open-source Python interface for wxWindows http://wxpython.org. 

• JPython − JPython is a Python port for Java which gives Python scripts seamless access to Java class libraries on the local machine http://www.jython.org. There are many other interfaces available, which you can find them on the net.

PYTHON PYGAME:-

Python is the most popular programming language or nothing wrong to say that it is the next-generation programming language. In every emerging field in computer science, Python makes its presence actively. Python has vast libraries for various fields such as Machine Learning (Numpy, Pandas, Matplotlib), Artificial intelligence (Pytorch, TensorFlow), and Game development (Pygame,Pyglet).
 
PYGAME:-
o	Pygame is a cross-platform set of Python modules which is used to create video games.
o	It consists of computer graphics and sound libraries designed to be used with the Python programming language.
o	Pygame was officially written by Pete Shinners to replace PySDL.


o	Pygame is suitable to create client-side applications that can be potentially wrapped in a standalone executable.
Install pygame in Windows:-


Python should be installed in the system, and it is good to have 3.6.1 or above version because it is much friendlier to beginners, and additionally runs faster. There are mainly two ways to install Pygame, which are given below:
Installing through pip: The good way to install Pygame is with the pip tool (which is what python uses to install packages). The command is the following:
py -m pip install -U pygame –user
  
BASIC SYSNTEX:-

import pygame - This provides access to the pygame framework and imports all functions of pygame.
pygame.init() - This is used to initialize all the required module of the pygame.
pygame.display.set_mode((width, height)) - This is used to display a window of the desired size. The return value is a Surface object which is the object where we will perform graphical operations.


pygame.event.get()- This is used to empty the event queue. If we do not call this, the window messages will start to pile up and, the game will become unresponsive in the opinion of the operating system.
pygame.QUIT - This is used to terminate the event when we click on the close button at the corner of the window.
pygame.display.flip() - Pygame is double-buffered, so this shifts the buffers. It is essential to call this function in order to make any updates that you make on the game screen to make visible.


Pygame Surface:-
The pygame Surface is used to display any image. The Surface has a pre-defined resolution and pixel format. The Surface color is by default black. Its size is defined by passing the size argument.
Surfaces can have the number of extra attributes like alpha planes, color keys, source rectangle clipping, etc. The blit routines will attempt to use hardware acceleration when possible; otherwise, they will use highly enhanced software blitting methods.



Pygame Clock:-
Times are represented in millisecond (1/1000 seconds) in pygame. Pygame clock is used to track the time. The time is essential to create motion, play a sound, or, react to any event. In general, we don't count time in seconds. We count it in milliseconds. The clock also provides various functions to help in controlling the game's frame rate. The few functions are the following:
tick()
This function is used to update the clock. The syntax is the following:


1.	tick(framerate=0)  
This method should be called once per frame. It will calculate how many milliseconds have passed since the previous call. The framerate argument is optional to pass in the function, and if it is passed as an argument then the function will delay to keep the game running slower than the given ticks per second.


tick_busy_loop()
The tick_busy_loop() is same as the tick(). By calling the Clock.tick_busy_loop(20) once per frame, the program will never run at more than 20 frames per second. The syntax is the following:


1.	tick_busy_loop()  
get_time()
The get_time() is used to get the previous tick. The number of a millisecond that isdra passed between the last two calls in Clock.tick().
	get_time()
  
  
Pygame Blit:-
The pygame blit is the process to render the game object onto the surface, and this process is called blitting. When we create the game object, we need to render it. If we don't render the game objects and run the program, then it will give the black window as an output.


Blitting is one of the slowest operations in any game so, we need to be careful to not to blit much onto the screen in every frame. The primary function used in blitting is blit(), which is:
blit()
1.	blit(source,dest,area=None,special_flags=0)  
This function is used to draw one image into another. The draw can be placed with the dest argument. The dest argument can either be a pair of coordinates representing the upper left corner of the source.


Pygame Adding Image:-

To add an image on the window, first, we need to instantiate a blank surface by calling the Surface constructor with a width and height tuple.
1.	surface = pygame.Surface((100,100))  
The above line creates a blank 24-bit RGB image that's 100*100 pixels with the default black color.
For the transparent initialization of Surface, pass the SRCALPHA argument.
1.	surface = pygame.Surface((100,100), pygame.SRCALPHA)  

Pygame Rect:-

Rect is used to draw a rectangle in Pygame. Pygame uses Rect objects to store and manipulate rectangular areas. A Rect can be formed from a combination of left, top, width, and height values. It can also be created from Python objects that are already a Rect or have an attribute named "rect".


Pygame Keydown:-

Pygame KEYDOWN and KEYUP detect the event if a key is physically pressed and released. KEYDOWN detects the key press and, KEYUP detects the key release. Both events (Key press and Key release) have two attributes which are the following:
o	key: Key is an integer id which represents every key on the keyword.
o	mod: This is a bitmask of all the modifier keys that were in the pressed state when the event occurred.


Pygame Draw:-

Pygame provides geometry functions to draw simple shapes to the surface. These functions will work for rendering to any format to surfaces. Most of the functions accept a width argument to signify the size of the thickness around the edge of the shape. If the width is passed 0, then the shape will be solid(filled).
All the drawing function takes the color argument that can be one of the following formats:


o	A pygame.Color objects
o	An (RGB) triplet(tuple/list)
o	An (RGBA) quadruplet(tuple/list)
o	An integer value that has been mapped to the surface's pixel format


Pygame Text and Font:-
Pygame also provides facilities to render the font and text. We can load fonts from the system by using the pygame.font.SysFont() function. Pygame comes with the built-in default font which can be accessed by passing the font name or None. There are many functions to help to work with the font.

The font objects are created with pygame.font.Font().The actual font objects do most of the works done with fonts. Font objects are generally used to render the text into new Surface objects

Pyglet:-
Python provide another game library named pyglet which is cross-platform windowing and multimedia library for Python. It is used to developing games and other visually rich applications. It supports user interface event handling, windowing, OpenGL graphics, loading images and videos, and playing sounds and music.

Few features of pyglet are the following:

o	No external installation requirements or dependencies.
o	Take benefit of multiple windows and multi-monitor.
o	It can load images, sound, music, and video in any format.
o	Pyglet is provided under the BSD open-source license.
o	It supports both Python 2 and 3.


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
