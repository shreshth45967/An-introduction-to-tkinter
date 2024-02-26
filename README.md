# An introduction to GUI development with tkinter

### The Tkinter module is the standard Python interface to Tk GUI toolkit from Scripts,both of Tk and Tkinter are available on most Unix platforms,as well as Windows and Macintosh systems. Starting with the 8.0 release,Tk offers native look and feel on all platforms.

### Tk interface module is located in a binary module named _tkinter present in  earlier versions.
### Two most important python gui modules are:- 
### 1. Tkinter module 
### 2. Tkconstants
### to get started you need to import the modules using

  ### by typing  "import Tkinter"  
  ### or by typing " from Tkinter import * "

### to initialize Tkinter we have to create the root widget,only one root widget should be created for each program, and it must be created before any other widget.

   ```python
   python root =Tk()
   w = Label(root,text='Hello world!)
   w.pack()
   ```

 ### A Label widget can display either text or an icon or other image. In this case, we use the text option to specify which text to display. Next, we call the pack method on this widget, which tells it to size itself to fit the given text, and make itself visible. But before this happens, we have to enter the Tkinter event loop:
 
```python root.mainloop()```

### The program will stay in the event loop until we close the window. The event loop doesn't only handle events from the user (such as mouse clicks and key presses) or the windowing system (such as redraw events and window configuration messages), it also handle operations queued by Tkinter itself. Among these operations are geometry management (queued by the pack method) and display updates. This also means that the application window will not appear before you enter the main loop.

### basic demonstration of tkinter program:


```python    
from tkinter import Tk, Frame, Button

class App:
    def __init__(self, master):
        frame = Frame(master)
        frame.pack()
        self.button = Button(frame, text='QUIT', fg="green", command=frame.quit)
        self.button.pack(side='left')

    def say_hi(self):
        print("hi there!")

root = Tk()
app = App(root)
root.mainloop()
```


   
   
   

      
      

      
        





  




