# FutureBlitz

This is a FutureBlitz package. FutureBlitz is a compiled language in BASIC's family: `.fb` files,
keywords in title case (`Function`, `If`, `End If`), `//` comments, a name's type after it
(`Local count: Int = 0`), and a statement a line.

```fb
Import std.core

Function Square(n: Int): Int => n * n

For i = 1 To 5
    Print("{i} squared is {Square(i)}")
End For
```

- `fb run` builds and runs the package, `fb build` builds it, `fb test` runs its `@Test`s,
  `fb check` gives its errors without building it, and `fb fmt` formats its files.
- Its standard library is `std`: `Import std.core`, `std.collections`, `std.io`, `std.text`, and
  the rest.
- `fb mcp` is a Model Context Protocol server, over stdio, whose tools know FutureBlitz:
  `search_docs` searches the language's spec and std's reference, `lookup` finds a name's
  declarations, `check` checks code or a file and gives its errors, and `format` formats code.
  An assistant runs it as the command `fb mcp`, in the package's folder.
- FutureBlitz isn't Visual Basic or any other language: look a feature up with `search_docs`
  before using it, and `check` code before saying it works.
