## Réunion GETALP - 15/01/2026

## Ordre du jour : point soutenance janvier et clarification code GenderedNews 

### Objectif stage : mise à jour des scrappers 

#### Problèmes indentifiés : 
- Changements de structures des sites non anticipés : voir pour trouver des libs plus flexibles
- Certains sites luttent contre le scrapping
- Lib Beautifulsoup a réglé certains soucis, mais pas idéal car décrochage de versions, problème de compatibilité avec "Newspaper3k".

#### Changements à faire 

- Etudier le code existant pour voir si changements possibles
- Les scrappers se trouvent dans le dossier ```gn_modules```
- Sinon voir pour trouver des libs plus flexibles et maintenues 
- Pouvoir faire en sorte que le programme détecte des anomalies s'il en trouve pendant le process du scrapping 
- Implémenter de nouveaux tests unitaires : les faire pour des analyse par période. 

#### Stratégies de scraping 
- Scraping par URL : rentre des batteries d'URL. Si une URL y est déjà, on ne fait rien, sinon on l'ajoute
Par lot, donc rapide, mais beaucoup de boucles à gérer, et compliqué à débugger. 
- Flux RSS : restent utile à gérer, car encore utilisé

### Refacto code projet 

- Réorganiser l'architecture du projet : voir avec Patrick et Ange qui ont l'historique du projet 
- Déterminer l'utilité de chaque module, classe ou fichier
- Exclure ce qui ne marche plus, n'est plus d'actualité (Twitter, ...)
- Au départ, le projet était dit comme étant un "aspirateur web"
- Configuration trop éparpillée dans le projet -> la centraliser 
- En cas de soucis, reprendre dans les archives les articles, URLs, les remmettre dans la base. 

### Points soutenance 

- Faire un schema de l'achitecture : scrapping, processing, storage, etc...
- Valoriser l'aspect industriel : ce n'est pas un projet du monde universitaire, mais un projet qui est censé basculer vers le monde industriel. L’AFP est présente pas sur la partie web, mais sur la partie traitement, ce site est censé être bien diffusé.

### Organisation de travail 

- Mise à disposition probable d'une VM dédiée pour notre code 
- Requêtes MongoDB doivent passer par index.
- Produire des schéma un max pour expliquer les travaux
- Toutes les propositions d'amélioration sont encouragées et bien accueillies





