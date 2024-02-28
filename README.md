# An introduction to GUI development with tkinter

 The Tkinter module is the standard Python interface to Tk GUI toolkit from Scripts,both of Tk and Tkinter are available on most Unix platforms,as well as Windows and Macintosh systems. Starting with the 8.0 release,Tk offers native look and feel on all platforms.

 Tk interface module is located in a binary module named _tkinter present in  earlier versions.<br><br> Two most important python GUI modules are:-<br><br>  1. Tkinter module<br>  2. Tkconstants<br><br> to get started you need to import the modules using<br> by typing  "import Tkinter"<br><br> or by typing " from Tkinter import * " <br><br> to initialize Tkinter we have to create the root widget,only one root widget should be created for each program, and it must be created before any other widget.

   ```python
   python root =Tk()
   w = Label(root,text='Hello world!)
   w.pack()
   ```

 A Label widget can display either text or an icon or other image. In this case, we use the text option to specify which text to display. Next, we call the pack method on this widget, which tells it to size itself to fit the given text, and make itself visible. But before this happens, we have to enter the Tkinter event loop:
 
```python
python root.mainloop()
```

The program will stay in the event loop until we close the window. The event loop doesn't only handle events from the user (such as mouse clicks and key presses) or the windowing system (such as redraw events and window configuration messages), it also handle operations queued by Tkinter itself. Among these operations are geometry management (queued by the pack method) and display updates. This also means that the application window will not appear before you enter the main loop.

#### basic demonstration of tkinter program:


```python    
from tkinter import Tk, Frame, Button

class App:
    def __init__(self, master):
        frame = Frame(master)
        frame.pack()
        self.button = Button(frame, text='QUIT', fg="green", command=frame.quit)
        self.button.pack(side='left')
        self.hi_there = Button(frame, text="Hello", command=self.say_hi)
        self.hi_there.pack(side=LEFT)

    def say_hi(self):
        print("hi there!")

root = Tk()
app = App(root)
root.mainloop()
```

 **_Class Creation:_** <br> We start by defining a class called App.The constructor (__init__ method) takes a parent widget (the master) as an argument.<br> Inside the constructor, we create a Frame widget to serve as a container for other widgets.**<br><br> _Adding Buttons:_** <br> Within the frame, we create two Button widgets.<br> The first button is labeled “QUIT” and appears in red.<br>The second button is labeled “Hello”.<br><br> **_Functionality:_** <br> The “QUIT” button is associated with the frame.quit function, which quits the application.<br> The “Hello” button triggers a custom method called say_hi.

-----------------------------------------------------------------------------------------------------------------------------------------------------
When working with Tkinter, you can name widgets using the following approach:<br><br>
**_Automatic Naming:_**<br>

In Tkinter, each widget is an object (an instance of a class) representing buttons, frames, and other GUI elements.
When you create a widget, you need to pass its parent as a parameter to the widget creation function.
Tkinter automatically assigns a unique name to each new widget.
For example, if you create a button within a frame, Tkinter assigns names like “.:1428748” for the frame and “.:1428748.1432920” for the button.<br>

**_Accessing Widget Names:_**<br>
To access a widget’s name within an event or function, use event.widget["text"].
For example, if you want to get the name of a widget during an event, use event.widget["text"] inside a function.
You can then print the widget’s name using print(event.widget["text"]).

Remember, widget names in Tkinter are automatically managed, making it easier to work with GUI elements

-----------------------------------------------------------------------------------------------------------------------------------------------------



























### Widget classes in Tkinter

| Widget | Description |
|---|---|
| Button | A simple button, used to execute a command or other operation. |
| Canvas | Structured graphics. This widget can be used to draw graphs and plots, create graphics editors, and to implement custom widgets. |
| Checkbutton | Represents a variable that can have two distinct values. Clicking the button toggles between the values. |
| Entry | A text entry field. |
| Frame | A container widget. The frame can have a border and a background, and is used to group other widgets when creating an application or dialog layout. |
| Label | Displays a text or an image. |
| Listbox | Displays a list of alternatives. The listbox can be configured to get radiobutton or checklist behavior. |
| Menu | A menu pane. Used to implement pulldown and popup menus. |
| Menubutton | A menubutton. Used to implement pulldown menus. |
| Message | Display a text. Similar to the label widget, but can automatically wrap text to a given width or aspect ratio. |
| Radiobutton | Represents one value of a variable that can have one of many values. Clicking the button sets the variable to that value, and clears all other radiobuttons associated with the same variable. |
| Scale | Allows you to set a numerical value by dragging a "slider". |
| Scrollbar | Standard scrollbars for use with canvas, entry, listbox, and text widgets. |
| Text | Formatted text display. Allows you to display and edit text with various styles and attributes. Also supports embedded images and windows. |
   
   
   

      
      

      
        





  




