# Template asciidoctorj

Le point d'entrée de la ressource est `index.adoc`, et ne doit pas être renommé.

Les autres fichiers devront commencer par un `_` (_underscore_) si inclus dans `index.adoc`. 
Ainsi ils ne  feront pas l'objet d'une transformation à part, mais considérés comme des *chapitres* 
du document principal `index`.

L'arborescence du projet :

````.
├── docs\
├── pom.xml
├── README.md
├── src
   ├── docs
   │   ├── asciidoc
   │   │   ├── images\
   │   │   ├── _doc1.adoc
   │   │   └── index.adoc
   │   └── assets\
   └── theme
       ├── logo.png
       └── x-theme.yml
````


# Github

* Déclarer `docs/` comme github pages (project settings)
* Lancer la commande `mvn` à la racine du projet (ou via votre IDE) **avant** de _commit_ et _push_.
 Ce qui aura pour effet de placer le build html (`target/generated-docs/*`) dans le dossier `docs/` (inclus dans
  le commit), en plus de génrer une version pdf (`index.pdf`) - TODO rename index.pdf to `project-name.pdf`.

Le résultat sera accessible : _https://<\<user>>.github.io/<\<project-name>>_

# Ressources

* https://asciidoctor.org/docs/asciidoctor-maven-plugin/
* https://github.com/asciidoctor/asciidoctor-maven-examples
