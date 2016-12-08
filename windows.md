Windowing System
===

Rio is the name of the windowing system. Like other windows in other operating systems you can run different processes in different windows, moving and resizing them at will. Unlike other systems you can draw the window in the position and location that you want before you run the program inside it. Window controls are generally kept out of sight maximizing screen real estate.

To draw a new window on the screen you can right-click on an empty spot on the desktop and choose "New." You will see that the mouse cursor changes to a plus. As an aside, mouse cursor changes are fairly common in the system to signal mode changes or even ok/cancel prompt. Now, right-click and drag a reasonably sized window on the screen. The window has a command prompt called rc, not unlike Linux/Mac bash or even the command prompt in Windows.

From the rc shell prompt you can run commands that are text only or graphical. The "cd" command and "ls" commands are example of text only commands. You can try them now.

When you decide to run a graphical program they will usually assume control of the window rather than opening a new window. Try running the "games/mole" game in your new window. You can quit the game by typing "q" on the keyboard.

Graphical programs are able to customize the graphics within the window. They can also override the mouse cursor and present its own mouse click menus. A program is free to completely define its own UI within that window, acme being a good example of this. The manual pages are a good way to learn about how to use custom UI's.

In many ways a window appears to a program as having its own screen and mouse. The abstraction is so similar that it is possible to run another instance of the Rio window manager inside a window! Try running it now and then draw a new window inside the second Rio. That inner window is sandboxed within the rio window. There's no way that it can resize itself and escape. This is also how Plan 9 developers can test changes to Rio before deploying those changes to their system.

Each program has its own way to quit, exit and close its window. If the application is not responding or you forget how to quit a particular program you can right-click on the desktop, chose "Delete" and right click on the window you want to kill. Try right-clicking in your rio window and deleting the inner window now. Next, try right-clicking on your outer desktop and deleting the inner rio window.

Resizing windows works much like it does on other systems. When you hover the mouse over the window's edge you can see that the cursor changes shape. On the edges you can resize that edge either vertically or horizontally. On the corners you can resize both ways. There is no known shortcut to maximize a window automatically to cover the whole screen, Instead, it is a manual process.

There is another way to resize windows. You can right-click on the desktop, choose Resize, right-click on the window to resize and draw out the new location of your window.

