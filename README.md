# lorenz-wheels

This is some TikZ code I made to illustrate the wheels of a [Lorenz cipher machine], which was used by the German Army during World War II.

The machine had twelve wheels, each with a different number of "cams" (switches), and they were grouped into three sets by the British codebreakers: psi/ψ, chi/χ, and mu/μ wheels.

<table>
  <tr>
    <td>
      <img src="https://github.com/alexwlchan/lorenz-wheels/blob/main/images/wheels-1.png?raw=true">
    </td>
    <td>
      <img src="https://github.com/alexwlchan/lorenz-wheels/blob/main/images/wheels-8.png?raw=true">
    </td>
    <td>
      <img src="https://github.com/alexwlchan/lorenz-wheels/blob/main/images/wheels-10.png?raw=true">
    </td>
  </tr>
</table>

The diagrams are drawn using [TikZ], a library for creating graphics in LaTeX.
The ability to draw points using polar coordinates made it quite pleasant.

I never used the illustrations, but I kept the code as a useful example of how to do diagrams in TikZ that I could get into other places.

[Lorenz cipher machine]: https://en.wikipedia.org/wiki/Lorenz_cipher
[TikZ]: https://tikz.dev/

## To create the illustrations

To render as PDF:

```
$ pdflatex wheels.tex
```

To convert the PDF to a series of PNG images with transparent backgrounds, use ImageMagick:

```
$ convert -background none -density 500 wheels.pdf images/wheels.png
```

## Further reading

-   [Illustrating the cipher wheels of a Lorenz machine](https://alexwlchan.net/2022/04/lorenz-wheels/), a blog post I wrote that gives a bit more context and background
-   [Tony Sale's website](https://www.codesandciphers.co.uk/virtualbp/fish/fishindex.htm), which explains the Lorenz cipher and the British codebreaking response in more detail
