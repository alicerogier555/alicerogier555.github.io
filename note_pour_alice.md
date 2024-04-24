
## Installer Jekyll
On pensera à bien installer jupyter ou bien à systématiquement travailler dans un environnement dans lequel il est défini.
Je suis la [procédure d'installation](https://jekyllrb.com/docs/installation/ubuntu/) qui est la suivante:
```
sudo apt-get install ruby-full build-essential zlib1g-dev

echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

gem install jekyll bundler
```
puis je vais dans le dossier de mon site web et j'éxecute
```
bundle install
```
Pour lancer le serveur et faire tourner le site et le modifier
```
bundle exec jekyll serve --lsi
```

## Publication
The publication database is the bib file located in _bilbiography/papers_alice. This was set in the _config file. 
When you add ajournal, you should add its nice title in the 
abbr bibtex entry and then configure the color and url in _data/venues.yml so that it displays on the left !

## Notes pour moi même

Il faut toujours bien se mettre à jour pour éviter des galères. 
La branche victor_master est ma branche par défaut et est systématiquement poussée sur mon repo git perso. via la commande `git push personnal_repo victor_master`.

Dans le fichier de config, je modifie :
include: ["_victor_pages"] # à la place de ["_pages"]
De cette manière, je garde à jour les propositions dans _pages et je ne modifie que mes pages personnelles. 

Je définis donc toutes mes pages dans _victor_pages
Par ailleurs, je rajoute dans la liste des fichiers à exclure _pages, _posts.


## Modifications apportées:
*  Dans le fichier News.liquid, je change le format de la date
*  Dans les fichier project.liquid, j'enlève le text-lowercase
*  Dans les fichiers de configuration scss, je modifie la couleur de base du thème

## Web
Pour se connecter en ssh
`ssh gondret@phare.normalesup.org`

Pour supprimer tous les fichiers /dossier d'un dossier
`rm -rf folder_name`
`exit`

Pour transférer tous les dossiers d'un répertoire en scp
`scp -r * gondret@phare.normalesup.org:WWW`

