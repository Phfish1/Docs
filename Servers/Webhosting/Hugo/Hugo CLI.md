## Must know

```
$ hugo version
```

Creates the hugo file structure
```
$ hugo new site NAME
```

Creates a first.md file in /content/posts/first.md
```
$ hugo new posts/first.md
```

Runs a test server
```
$ hugo server
```

Build your site to the `/public` directory 
```
$ hugo
```

**BUT YOU CAN CHANGE THE BUILD DIRECTORY**
using `--destination`
or `publishDir` in your config.toml eg( `publishDir = "/var/www/main"` )

>*Remember to clear your /public directory of unwanted files before each build*




