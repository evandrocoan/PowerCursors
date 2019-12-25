PowerCursors
==================

PowerCursors is a Sublime Text 3 package that makes the add/remove/select of multiple cursors more convenient with keyboard.

You can easily add a cursor and move it around while keeping all other cursors static. You can also choose between these cursors and remove them. When you are done putting cursors in positions, you can activate them and start moving and editing with all of them.


Demos:
------------------

### Multiple Cursors
![Demo 1 of PowerCursors](https://raw.github.com/MaokaiLin/PowerCursors/screencast/demo1.gif "PowerCursors Screencast 1")

### Multiple Selections
![Demo 2 of PowerCursors](https://raw.github.com/MaokaiLin/PowerCursors/screencast/demo2.gif "PowerCursors Screencast 2")


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
   wait few seconds until the installation finishes up
1. Now,
   Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   input the following address and press <kbd>Enter</kbd>
   ```
   https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
   ```
1. Go to the menu **`Tools -> Command Palette...
   (Ctrl+Shift+P)`**
1. Type **`Preferences:
   Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   find the following setting on your **`Package Control.sublime-settings`** file:
   ```js
       "channels":
       [
           "https://packagecontrol.io/channel_v3.json",
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
       ],
   ```
1. And,
   change it to the following, i.e.,
   put the **`https://raw.githubusercontent...`** line as first:
   ```js
       "channels":
       [
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
           "https://packagecontrol.io/channel_v3.json",
       ],
   ```
   * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
     you will not install this forked version of the package,
     but the original available on the Package Control default channel **`https://packagecontrol.io...`**
1. Now,
   go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
search for **`PowerCursors`** and press <kbd>Enter</kbd>

See also:

1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


How to use
-------------------
There are 6 commands in **PowerCursors**:

* ### Add cursor

    `ctrl+=` in OSX, `alt+=` in Linux and Windows.

    It adds a cursor and enters a transition mode where you can move the active cursor around without affecting the position of the cursor you just added.

    The command is `power_cursor_add`.

* ### Remove current cursor

    `ctrl+-` in OSX, `alt+-` in Linux and Windows.

    It removes the currently active cursor and activates the cursor right before the current cursor (position-wise).

    The command is `power_cursor_remove`.

* ### Select previous/next cursor

    `ctrl+[`/`ctrl+]` in OSX, `alt+[`/`alt+]` in Linux and Windows.

    It makes the currently active cursor static and activates the cursor right before/after the current cursor (position-wise).

    It also works when you already have multiple cursors. It makes all cursors static and activates only the last/first cursor. Now you are free to move only one of the cursors, or remove some of them without affecting the rest.

    The command is `power_cursor_select`, with an argument "forward" being either `true` or `false`.

* ### Activate all cursors

    `ctrl+a` in OSX, `alt+a` in Linux and Windows.

    It activates all cursors. Now when you move or edit, all cursors will respond, just like how the native multiple-cursor works in Sublime Text.

    The command is `power_cursor_activate`.

* ### Exit

    `ESC` in OSX, Linux and Windows.

    It exits the cursor transition status. All cursors you added will be removed and the normal cursor mode is resumed.

    The command is `power_cursor_exit`.

### Note

All the commands above also work for selections. For example, after selecting one region, you can add a new cursor and select a different region while keeping the one you chose before intact. You can select multiple regions this way, then activate all and replace texts in them. Feel free to explore more usage of the commands. They are quite robust and adaptable.


License
-------------------

This software is released under the terms of the MIT license.
