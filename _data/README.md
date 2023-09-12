Lancez la commande suivante
```bash
curl "https://api.archives-ouvertes.fr/search/LS2N-TALN/?q=*&rows=1000&wt=csv&fl=halId_s,uri_s,title_s,authFullName_s,producedDate_s,journalTitle_s,conferenceTitle_s,country_s&sort=producedDate_s%20desc" > hal.csv
```
ou bien naviguez à l'adresse et remplacez `hal.csv` par le fichier obtenu.

Documentation de l'API : https://api.archives-ouvertes.fr/docs/search

Cette requête:
- recherche tous documents `q=*`
- renvoie 1000 documents (a changer lorsqu'il y en aura trop ;) `rows=1000`
- retourne un csv `wt=csv`
- renvoie les champs utiles (voir `_pages/publications.markdown`) `fl=halId_s,uri_s,title_s,authFullName_s,producedDate_s,journalTitle_s,conferenceTitle_s`
- tri les résultats par date de publication `sort=producedDate_s%20desc`