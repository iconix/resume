# resume

To re-build on a Windows PC, I...
- install [MiKTeX](https://miktex.org/download) to use `xelatex`
    - Preferred paper: Letter
- install the [LaTeX Workshop extension](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) on VSCode
    - LaTeX Workshop Settings:
        ```json
        [
            // ...
            "latex-preview.command": "xelatex",
            "latex-workshop.latex.recipes": [{
                "name": "xelatex",
                "tools": [
                    "xelatex"
                ]
            }],
            "latex-workshop.latex.tools": [{
                "name": "xelatex",
                "command": "xelatex",
                "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOC%.tex"
                ]
            }
        ],
        "latex-workshop.view.pdf.viewer": "tab",
        // ...
        ```
- using the Workshop extension, "Build LaTeX project" using the "Recipe: xelatex" command. Changes to `resume.tex` will modify `resume.pdf`.
