My blog, developed using [blogdown](https://github.com/rstudio/blogdown)

## Environment setup

VSCode extension: [R](https://marketplace.visualstudio.com/items?itemName=Ikuyadeu.r)

Radian:

```sh
pipx install radian
```

Using `pipx` (https://pypa.github.io/pipx/) is recommended since it creates a dedicated virtual environment.

R packages:

```sh
install.packages('blogdown') # installs blogdown
install.packages('languageserver') # installs R language server, required if you are using VSCode
```
