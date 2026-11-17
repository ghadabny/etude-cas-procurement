# Étude de cas Achats - mode d'emploi

## Contenu
- `analyse_achats.ipynb` : notebook complet, résultats et graphiques inclus. Sections 1 à 3 conservées avec corrections de reproductibilité et de réserves ; partie 4 révisée ; parties 5 à 8 ajoutées.
- `synthese_direction.pdf` : recommandations et chiffrage, une page.
- `journal_decisions.pdf` : hypothèses, arbitrages, pistes abandonnées et limites, une page.
- `requirements.txt` : dépendances d'exécution.

## Reproduire
Python 3.12 recommandé. Dans un environnement virtuel :

```bash
python -m pip install -r requirements.txt
jupyter lab analyse_achats.ipynb
```

Déposer `purchase-order-data-2012-2015-.csv` à côté du notebook, dans `data/` ou dans `../data/`. Autre possibilité : définir `ACHATS_CSV` avec son chemin. Le CSV original n'est pas inclus dans l'archive, conformément aux consignes. Les fichiers du dictionnaire et des modes d'achat sont les documents fournis avec l'énoncé ; aucune requête externe n'est nécessaire.

Dans Jupyter : redémarrer le noyau, puis exécuter toutes les cellules dans l'ordre. Le notebook ne modifie pas le CSV. Une ligne correspond à un article de commande. Les contrôles portent notamment sur la réconciliation des montants, le maintien des lignes, l'affectation unique des commandes et l'ordre des scénarios.

## Lecture des résultats
Tous les montants sont en dollars historiques. « Dépense » est un raccourci pour montant net de commandes ; les paiements et la ventilation pluriannuelle ne sont pas disponibles. La moyenne de trois exercices est un proxy, pas une prévision. Les taux des scénarios sont des hypothèses métier modifiables dans la section 7.1. Les écarts de prix en section 6 sont des signaux distincts, jamais ajoutés aux scénarios.

Les synthèses PDF sont une photographie des résultats du notebook livré : les mettre à jour si les données ou paramètres changent. Le fichier ne permet aucune projection fiable sur un budget actuel à partir des années 2012–2015.