# Elixir blog


## CONTENT / Comment éditer le blog

### Article

Les posts sont dans le repertoire `_posts` au format Markdown.
Les brouillons sont dans le repertoire `brouillons` au format Markdown. Ils ne sont pas référencés.

Ils doivent respecter le format 2021-02-04-titre-au-format-slug.md

#### Rappel code markdown

##### Les images

```md
![Une image qui est dans asset]({{ site.baseurl }}assets/images/tube-lixi.png)
```

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
* Run `bundle install` pour installer les dépendances (voir Gemfile)
* Run `bundle exec jekyll serve --livereload`
* Go to [local server](https://127.0.0.1:4000/)

### Générer les pages HTML en local

```bash
$ # Dans ./_site/ (voir config.yml)
$ bundle exec jekyll serve
$ bundle exec htmlproofer --assume-extension ./_site --url-swap '^/blog/:/' --allow-hash-href
```

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
