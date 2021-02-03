# Elixir blog


## CONTENT / Comment éditer le blog

### Article

### Auteurs

### Tags


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
$ gulp
```

### Déploiement

* Commit sur la branch master (soit via Git, soit via l'interface [Github](https://github.com/elixir-sante/elixir-blog))
* Lancer un build sur le job Jenkins [deploy-blog](https://jenkins.elixir-sante.fr/job/deploy-blog/)
* Regarder le résultat du build
* C'est en ligne !
