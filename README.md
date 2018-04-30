# Story: Calcul de taxes

## Enonc�

Une taxe sur la valeur ajout�e de 10% est appliqu�e sur chaque produit, � l'exception des livres, de
la nourriture et des m�dicaments, qui en sont exempt�s. Une taxe additionnelle de 5% sur les
produits import�s, sans exception.
Le montant de chacune des taxes est arrondi aux 5 cents sup�rieurs, selon la r�gle suivante :

### Taxe calcul�e Taxe imput�e
0.99 1.00
1.00 1.00
1.01 1.05
1.02 1.05

Lorsque l'on passe une commande, une facture est �mise listant chacun des produits ainsi que leur
prix TTC ; au bas de la facture figurent le montant total (TTC) ainsi que le montant total des taxes.
Le montant TTC est calcul� comme suit : Pttc = Pht + somme(arrondi(Pht*t/100)) Pttc: Prix TTC Pht :
Prix hors taxes t : taxe applicable

Ecrire une application, ex�cutable sur une JVM 1.8, qui imprime la facture d�taill�e pour chacun des
paniers suivants :

## INPUT

### Input 1
l 1 livre � 12.49
l 1 CD musical � 14.99
l 1 barre de chocolat � 0.85

### Input 2
l 1 bo�te de chocolats import�e � 10.00
l 1 flacon de parfum import� � 47.50

### Input 3
l 1 flacon de parfum import� � 27.99
l 1 flacon de parfum � 18.99
l 1 bo�te de pilules contre la migraine � 9.75
l 1 bo�te de chocolats import�s � 11.25

## OUTPUT

### Output 1
1 livre : 12.49
1 CD musical : 16.49
1 barre de chocolat : 0.85
Montant des taxes : 1.50
Total : 29.83

### Output 2
1 bo�te de chocolats import�e : 10.50
1 flacon de parfum import� : 54.65
Montant des taxes : 7.65
Total : 65.15

### Output 3
1 flacon de parfum import� : 32.19
1 flacon de parfum : 20.89
1 bo�te de pilules contre la migraine : 9.75
1 bo�te de chocolats import�s : 11.85
Montant des taxes : 6.70
Total : 74.68