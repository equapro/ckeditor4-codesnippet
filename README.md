equapro/ckeditor4-codesnippet
=============================

Custom build réalisé à partir de la version 11.2.0 de highlight.js

``` bash
codesnippet
|_ dialogs
   |_ codesnippet.js         # modifié
|_ lib
   |_ highlight
      |_ styles              # copié depuis les sources
      |_ highlight.pack.js   # custom build
```

Récupération des sources

    git clone https://github.com/highlightjs/highlight.js.git --branch 11.2.0 --single-branch

Build

    node tools/build.js -n apache c cpp coffeescript css less scss diff http ini java javascript json markdown nginx perl php  python ruby sql twig xml yaml

Le build génére un fichier `highlight.js` qui a été renommé `highlight.pack.js` pour la compatibilité avec le plugin.

Le dossier `styles` du plugin provient du dossier `src/styles` du dépôt

Le fichier `dialogs/codesnippet.js` a également été modifié. Les langues disponibles ont été déclarées directement.

``` javascript
    var snippetLangs = {
        apache: "Apache",
        bash: "Bash",
        coffeescript: "CoffeeScript",
        c: "C",
        cpp: "C++",
        css: "CSS",
        diff: "Diff",
        xml: "HTML, XML",
        http: "HTTP",
        ini: "INI",
        java: "Java",
        javascript: "JavaScript",
        json: "JSON",
        less: "Less",
        markdown: "Markdown",
        nginx: "Nginx",
        perl: "Perl",
        php: "PHP",
        python: "Python",
        ruby: "Ruby",
        scss: "SCSS",
        sql: "SQL",
        twig: "Twig",
        yaml: "Yaml"
    }
```
