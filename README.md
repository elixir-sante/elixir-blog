# Elixir blog


## CONTENT / Comment éditer le blog

### Article

Les posts sont dans le repertoire `_posts` au format Markdown.
Ils doivent respecter le format 2021-02-04-titre-au-format-slug.md
Une feature de brouillon va être ajoutée bientôt :)

### Auteurs
Les données des auteurs sont dans `_data/authors.yml`

### Tags
Les données des tags sont dans `_data/tags.yml`


## DEV / Comment déployer

### Fork original Jasper2

[Forked repo](https://travis-ci.org/jekyller/jasper2)
[Original README.md](https://travis-ci.org/jekyller/jasper2)

### Dev local

* Cloner le repo
* Run `bundle exec jekyll serve --livereload`
* Go to [local server](https://127.0.0.1:4000/)

### Style

Le style CSS doit être recompilé après modification.
Editez `/assets/css/` qui seront compilé dans `/assets/built/`.

Depuis la racine :

```bash
$ npm install
$ 
$ # Pour un livereload
$ gulp
$
$ # Pour un build CSS onshot
$ gulp css
```

### Déploiement

* Commit sur la branch master (soit via Git, soit via l'interface [Github](https://github.com/elixir-sante/elixir-blog))
* Lancer un build sur le job Jenkins [deploy-blog](https://jenkins.elixir-sante.fr/job/deploy-blog/)
* TOUJOURS vérifier le résultat du build. Jenkins publie le résultat dans Slack.
* C'est en ligne !
