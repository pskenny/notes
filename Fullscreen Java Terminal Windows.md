---
title: Fullscreen Terminal Windows In Java Using Lanterna
tags:
  - Code_Snippet
  - Command-line
  - Programming_Language/Java
  - Terminal
  - TUI
type:
  - Blog
  - Blog/Post
creationDate: 2021-01-06
modifiedDate: 2025-12-09
published: 2021-01-06
access: Public
description: Code snippet for writing a TUI in Java using Lanterna
digitalGarden: Evergreen
---

> [!WARNING] Hey, it's you from 2025
> Don't do this. Don't hurt yourself. You want to write a [TUI](https://en.wikipedia.org/wiki/Command-line_interface)? Don't use Java. Use Python or Rust. That summer when you thought it was a fun idea is over.

_tldr:_ Here's a code snippet of a fullscreen terminal window using Lanterna.

[Lanterna](https://github.com/mabe02/lanterna) is an easy way to make text only user interfaces in Java that I highly recommend. One thing that took me too long to find was how to make a window fullscreen. Add:

```java

yourWindow.setHints(java.util.Collections.singleton(Window.Hint.FULL_SCREEN));

```

Here's it in a minimal example:

```java
import java.io.IOException;
import com.googlecode.lanterna.gui2.*;
import com.googlecode.lanterna.screen.*;
import com.googlecode.lanterna.terminal.*;

public class TUI {
  public static void main(String[] args) {
    MultiWindowTextGUI gui;
    Screen screen;
    BasicWindow window;

    try (Terminal terminal = new DefaultTerminalFactory().createTerminal()) {
      screen = new TerminalScreen(terminal);
      screen.startScreen();

      gui = new MultiWindowTextGUI(screen);
      window = new BasicWindow();
      window.setComponent(new Label("Hello, fullscreen!"));
      // Set window to use fullscreen hint
      window.setHints(java.util.Collections.singleton(Window.Hint.FULL_SCREEN));
      gui.addWindowAndWait(window);
    } catch (IOException ex) {
    }
  }
}
```

_Note:_ There are other hints you can use in `Window.Hint` you can use. Put them in a collection and pass them to the `setHints` method. I like `Window.Hint.NO_DECORATIONS`.

_Note: Note:_ As told in the documentation, _"Please note that it's up to the window manager if these hints will be honored or not."_

## Resources

- [Github repo](https://github.com/mabe02/lanterna)
- [Maven repo](https://mvnrepository.com/artifact/com.googlecode.lanterna/lanterna)
- [Official docs](https://github.com/mabe02/lanterna/tree/master/docs)
- [Official tutorial](https://github.com/mabe02/lanterna/blob/master/docs/tutorial/Tutorial01.html)
