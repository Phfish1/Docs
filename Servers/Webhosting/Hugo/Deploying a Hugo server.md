### What is Hugo

**Hugo is a open-source framwork for building static websites**
and its really easy to setup and use :)

### Prerequisites

- Git [Download](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- Go [Download](https://linuxhint.com/install-go-ubuntu-2/)

I recomend using **Vscode SSh** for easy management, if SSH is needed

## Download Hugo

**Easiest** way to do it
```
$ sudo apt install hugo
```

**Or** use docker. if you know what your doing
```
$ docker pull klakegg/hugo
```
for more including building it from source using git. see [hugo docs](https://gohugo.io/installation/) 

## Making a site

To make your new hugo site you must first create the hugo [**directory structure**](https://gohugo.io/getting-started/directory-structure/ )
```
$ hugo new site NAME-OF-DIR
```

Then Change Directory into it
```
$ cd NAME-OF-DIR
```

### installing the theme

Initialize a git repository
```
$ git init
```

Add your **Theme** "see [HugoThemes](https://themes.gohugo.io/)" as a git submodule. To the directory /themes
```
$ git submodule add https://github.com/USER/THEME /themes/THEME
```

*You dont need to add it as a submodule, you can use git clone. But using submodules makes it easier to edit in the future see [Using git submodule for hugo themes](https://www.andrewhoog.com/post/git-submodule-for-hugo-themes/) for more info*

### Config.toml

Then edit your config.toml to include
```
theme = "THEME"
```
THEME being the name of the directory you installed to /themes using *git submodule add*

## Deploying Locally

To deplay the static hugo site locally run
```
$ hugo server
```
It will then be accesible from localhost

## Deploying with NGINX



