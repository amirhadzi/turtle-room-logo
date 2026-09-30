# Turtle Room — Logo computer lab

A browser-based Logo environment inspired by the BBC computers in the school computer room. The first example is a spinning 3D cube written entirely in Logo: routines rotate and project its vertices, and loops draw the twelve edges.

## Start coding

Open the GitHub Pages website linked from this repository, or download **[index.html](index.html)** and open the downloaded file in Edge, Chrome or Firefox. This single HTML file contains the complete app, readable JavaScript source, styles, interpreter, examples and licence notices. It needs no installation or internet connection.

The cube runs on your first visit. If a saved draft is restored, press **Run program**. Select an example and press **Load** to start again.

- **Ctrl+Enter / Run program:** run the editor program.
- **Pause / Resume:** freeze and continue execution.
- **Esc / Stop:** interrupt loops and waits.
- **Ctrl+S / Save .logo:** download your editor contents.
- **Open .logo:** load a Logo text file.
- **Save image:** download the drawing as PNG.
- **Keep offline:** download the complete app.
- **Quick guide:** learn commands, routines, variables and the cube's maths.

Use the command prompt for short commands. Full editor runs start fresh; prompt commands keep the current drawing and routines. Drafts are saved on your device when browser storage is available. Save `.logo` copies to keep your work independently of browser storage.

## Try a classic

```logo
TO SQUARE :SIDE
  REPEAT 4 [FD :SIDE RT 90]
END

SQUARE 100
```

The built-in examples include a square, squares in a circle, a rainbow spiral and a recursive tree. The [spinning cube source](cube.logo) is also available separately. It uses three Logo routines, `FOREVER`, `REPEAT`, lists, `SIN`, `COS` and ordinary 2D turtle commands. No JavaScript cube primitive is used.

## Compatibility

The engine is Joshua Bell's **jslogo**, a broad subset of UCBLogo, with a BBC-style colour palette. It supports turtle movement, procedures, variables, lists, recursion, arithmetic, conditions, loops and text I/O.

This is a modern Logo dialect, not an exact BBC Micro or Acornsoft emulator. Historical sound, hardware and disk commands are not emulated.

- Colours 0–7: black, red, green, yellow, blue, magenta, cyan, white.
- Names work too: `SETPC "cyan`.
- `SIN` and `COS` take degrees; `WAIT 60` waits one second.
- Multiple local variables use `(LOCAL "A "B)`, not `LOCAL [A B]`.
- `DRAW` resets the turtle and screen; `DOFOREVER` aliases `FOREVER`.

## Hosting and editing

The app is intentionally self-contained. Edit `index.html` to change it; no build system or npm packages are required. All five Logo example programs are embedded in its `LOGO_EXAMPLES` object.

For GitHub Pages, use **Settings → Pages → Deploy from a branch → main → / (root)**. The same file can also be hosted by any static web server.

## Credits and licence

Interpreter and turtle engine: © Joshua Bell and contributors, Apache License 2.0. Original attribution and modification notes are preserved in [NOTICE.txt](NOTICE.txt) and inside `index.html`. The full licence is in [LICENSE](LICENSE).

- [Upstream jslogo](https://github.com/inexorabletash/jslogo)
- [Full language reference](https://inexorabletash.github.io/jslogo/language.html)
