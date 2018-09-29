# gean-podcast-theme

Podcast theme for gean.

## Install

```bash
$ git clone git@github.com:yiqilai/gean-podcast-theme.git
$ npm install
$ npm start
```

## Wercker Integration

`wercker.yml` example:

```yml
box: node:latest
build:
  steps:
    - npm-install
    - arjen/hugo-build:
        version: "0.24.1"
    - code: npm run build
deploy:
  steps:
    - lukevivier/gh-pages@0.2.1:
        token: $GITHUB_TOKEN
        domain: yiqilai.github.io/gean-podcast-theme
        basedir: docs
```

## License

[MIT](https://1000ch.mit-license.org) © [Shogo Sensui](https://github.com/1000ch)