## Custom Packages

### `mathmacros.sty`

The `mathmacros.sty` file contains all of my universal commands that make sense to use on any document. The most important ones being brackets.

```tex
\newcommand{\ba}[1]{\left< #1 \right>} % brackets angled
\newcommand{\bs}[1]{\left[ #1 \right]} % brackets square
\newcommand{\br}[1]{\left( #1 \right)} % brackets round
\newcommand{\bc}[1]{\left\{ #1 \right\}} % brackets curly
```

Or bra's and ket's

```tex
\newcommand{\bra}[1]{\left< #1 \right|} % bra
\newcommand{\ket}[1]{\left| #1 \right>} % ket
\newcommand{\braket}[2]{\left< #1 \middle| #2 \right>} % bra|ket
```

Or my fraction command

```tex
\newcommand{\f}[2]{\frac{#1}{#2}} % fraction shorthand
```

### `draft.sty`

The `draft.sty` file is a package used for leaving comments and todos on documents with multi collaborators. For example, to leave a comment to be printed in the document use the following command.

```tex
\comment{<insert comment text here>}
```

Or to leave a todo,

```tex
\todo{<insert todo text here>}
```

Now if you want to assign your name to the command, at the top of the document put,

```tex
\draftprofile{<id>}{<insert color>}
```

And then apply your id as an optional parameter to either comment or todo.

```tex
\todo[<id>]{<insert todo text here>}
\comment[<id>]{<insert comment text here>}
```

You can also change the name that is displayed in the actual file using an optional flag in draft profile.

```tex
\draftprofile[<person's name>]{<id>}{<insert color>}
```


