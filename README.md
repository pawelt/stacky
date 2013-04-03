[Stacky](http://justafewlines.com/2013/04/stacky/) - Simple icon stacks solution for Windows
============================================================================================


What is it
----------

Stacky is a small program for Windows that displays contents of a given directory as a list of clickable, labled icons.


Installation
------------

There is no installation. Just download precompiled package from `binaries` directory (`stacky-x64.zip`, also contains CRT dependencies) and unzip.

Direct link to precominled binaries: https://github.com/pawelt/stacky/blob/master/binaries/stacky-x64.zip?raw=true


Compilation
-----------

You can build Stacky with free Microsoft tools, using solution file in the `vsproj` directory.

Full source code (about 500 lines of C++ code) is available in `src` directory.


How to use it
-------------

1. Create a regular windows shortcut to `stacky.exe`.
2. Create a folder and put shortcuts to your programs there.
3. Edit the shortcut and add the folder's path to the `Target` field, so it looks something like this:

      `D:\pawel\Programs\Stacky\stacky.exe  D:\pawel\Stacks\Games`
      
4. Drag the stack shortcut to your taskbar.

That's all. You can click the Stacky shrotcut on the taskbar to open the new stack.


Why is it useful
----------------

You can replace a bunch of icons on your taskbar with one icon. 

Say you use Photoshop, Illustrator, Axure and couple other design-related programs. Instead of putting individual shortucts in your taskbar, you can create a folder called "Design", put all your design shortcuts there and create one shortcut on a taskbar.

Whenever you click on the icon, you will see all the icons you put in the folder, ready to launch.

If you have 30+ programs, it is really convenient to split them into couple groups, instead of squizing in all icons right in the taskbar.

Stacks with shortcuts to folders to your projects, movies, pictures and anything else work great too.


Why would you use Stacky instead of...
--------------------------------------

There are couple products on the market that do similar thing, like [RocketDock](http://rocketdock.com/) or [7stacks](http://alastria.com/software/7stacks/). In fact, I used 7stacks for quite some time. These are fine products, but stacky has some unique features that you may like:

- it is open source and 100% free
- it does one thing and does it well
- it's very small, requires no installation, no external configuration etc.
- but most of all, it's the fastest available solution


Why is it so fast?
------------------

Because Stacky caches stacked icons. Instead of reading and analyzing `.lnk` files (Windows shortcuts), and then fetching icons from corresponding executables every time you open a stack, Stacky stores all icons in one small file in the stack folder. When user opens a stack, no `.lnk` file nor `.exe` files are touched. Only Stacky cache file.

Any time the shortcuts folder is modified (new shrtcut is added etc.), the cache is rebuilt.

7stacks every now and then makes you wait good couple seconds, before it renders the stack. Stacky never, ever does it. Stacks are displayed immediately, every time.

That's why stacky is faster than anything I've seen so far.


