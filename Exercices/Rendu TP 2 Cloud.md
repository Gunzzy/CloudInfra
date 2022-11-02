# Rendu TP 2 Cloud

# Infrastructure n°1 :

 ● 1 serveur avec les ressources suivantes : 

○ 16 Go de RAM minimum 

○ 4 vCPU 

○ 100 Go de stockage disque

# Infrastructure n°2

● 6 serveurs avec les ressources suivantes : 

○ 6 Go de RAM minimum 

○ 3 vCPU 

○ 20 Go de stockage disque par serveur

 ● Particularité : 3 serveurs sont éteints la nuit de 22h à 6h du matin


# Exercice 1,2,3 avec Scaleway

Lien vers lequel je me suis basé pour les tarifs de Scaleway:

       https://www.scaleway.com/fr/tarifs/?tags=available,manageddatabases-relationaldatabases-manageddatabaseforpostgresqlandmysql,manageddatabases-memorydatabases-manageddatabaseforredis



# Infrastructure n°1 :

 - calcul du prix du stockage par mois 

0.0127 /mois 
0.0127* 100 = 1.27 dollars/mois

- Calcul Serveur + Stockage / mois

0.11 / hour * 24 (pour la journée) = 2.64
2.64*31= 81,84

Stockage + Serveur = 83.11 dollars

# Infrastructure n°2

Pour le stockage: 

 16h actif dans la journée donc 0.11 * 16 = 1.76 
 la journée
24h actif dans la journée donc 0.11*24 = 2.64 la journée

1.76 * 31 (au mois)= 54.56 * 3= 163.68 (pour les 3 serveurs qui s’arrêtent)

2.64*31 = 81.84*3 = 245.52 ( pour les 3 autres )

163.68+245.52=409.2 dollars au total

Stockage+Serveur :
0.0127*20 = 0.254 *6 = 1.524
409.2+1.524=410.72

# Infrastructure n°3

 3 serveurs : 0.055/h 
0.055 * 24 = 1.32 (pour le prix de la journée)

1.32*31 (prix au mois) = 40.92 *3 = 122.76 (pour les 3 serveurs)

Stockage 50 gb chacun : 0.0127/mois
0.0127 * 50= 0.635*3=1.905 (pour les 3 serveurs)

Load balancer 200 (c’est le minimum) 0.014/h
0.014*24=0.336
0.336*31=10.416

Base de donnée	
0.1233*24=0.2466
0.2466*31= 7.6

122.76+1.905+10.416+7.6=142.681 dollars


# Exercice 1,2,3 avec Azure

Lien vers les calculs de prix sur Azure:

     https://azure.microsoft.com/fr-fr/pricing/calculator/


# Infrastructure n°1 :
1 instance à 4 processeurs virtuels, 16 Go de RAM, stockage de 100 Go : 163,57 dollars
# Infrastructure n°2 :
3 instances à 4 cœurs, 8 Go de RAM, stockage de 40 Go pendant 1 mois : 486,23 dollars

3 instances à 4 cœurs, 8 Go de RAM, stockage de 40 Go pendant 490 heures : 326,39 dollars

infra 2 : 486,23 + 326,39 = 812,62 dollars/mois

# Infrastructure n°3 :

3 instances à 2 processeurs virtuels, 4 Go de RAM, stockage 75 de Go : 202,63 dollars

1 Load balancer avec 1 règle : 23,25 dollars

1 base de données Azure pour MySQL à 2 vCore et 10 Go de stockage : 63,21 dollars
infra 3 : 202,63 + 23,25 + 63,21 = 289,09 dollars

# Exercice 1,2 et 3 avec AWS

Liens vers les calculs d'AWS: 

             https://calculator.aws/#/addService

# Infrastructure n°1:
● 1 serveur avec les ressources suivantes :
○ 16 Go de RAM minimum
○ 4 vCPU
○ 100 Go de stockage disque

AWS : 67,40 HT USD

# Infrastructure n°2:
● 6 serveurs avec les ressources suivantes :
○ 6 Go de RAM minimum
○ 3 vCPU
○ 20 Go de stockage disque par serveur
● Particularité : 3 serveurs sont éteints la nuit de 22h à 6h du matin

AWS : 214,79 + 146,46 = 301,04 USD HT

# Infrastructure n°3:
● 3 serveurs avec les ressources suivantes :
○ 4 Go de RAM minimum
○ 2 vCPU
○ 50 Go de stockage disque par serveur
● 1 load balancer qui répartit 5 Mb/s de données équitablement vers les 3 serveurs
ci-dessus
● 1 service de base de données managé
○ 8 Go de RAM minimum
○ 2 vCPU

AWS : 69.30+291.74+33.12 : 394,16 USD HT

# Exercices 1,2 et 3 avec GCP

Liens vers les calculs des tarifs de GCP: 

     https://cloud.google.com/products/calculator?hl=fr

# Infrastructure n°1:   
Type d’instance : n2d-custom-4-16384 (16Go de RAM + 4 vCPU)

Prix : 125€43/mois pour 1 serveur

Stockage disque : Standard Disk de 100 Go
Prix : 4€84/mois pour 1 serveur

TOTAL : 130€27/mois pour 1 serveur.

# Infrastructure n°2:
Type d’instance : n2d-custom-4-6144 (6Go de RAM + 4 vCPU car 3 vCPU impossible)
Prix : 294€22/mois pour 3 serveurs

Stockage disque : Standard Disk de 20 Go

Prix : 0€97/mois par serveur
Prix pour 3 serveurs : 2€90/mois pour 3 serveurs

TOTAL : 297€13/mois pour 3 serveurs (qui tournent 24/24).

Type d’instance : n2d-custom-4-6144 (6Go de RAM + 4 vCPU car 3 vCPU impossible)

Prix : 216€61/mois pour 3 serveurs

Stockage disque : Standard Disk de 20 Go

Prix : 0€97/mois par serveur
Prix pour 3 serveurs : 2€90/mois pour 3 serveurs

TOTAL : 219€51/mois pour 3 serveurs(qui tournent 16 heures car ont les éteints de 22 heures jusqu’à 6 heures du matin).

TOTAL FINAL pour 6 serveurs : 297€13 + 219€51 = 516€64/mois


# Infrastructure n°3:
Type d’instance : n2d-custom-2-4096 (4Go de RAM + 2 vCPU)

Prix : 155€32/mois pour 3 serveurs

Stockage disque : Standard Disk de 50 Go

Prix : 2€42/mois par serveur

Prix pour 3 serveurs : 7€26/mois pour 3 serveurs

TOTAL : 162€58/mois pour 3 serveurs.

Load balancer : avec 3 règles de transfert et 5 Mb/s

Prix : 22€28/mois pour 1 load balancer à 3 règles
Sachant que 5 règles coûtent 0€025/h et chaque règle supplémentaire coûte 0€01/h.

Prix : 0€/mois pour 5 Mb/s

Le prix de la donnée entrante par le load balancer se paie par Go utilisé et aucun frais supplémentaire pour le trafic sortant.

TOTAL : 22€28/mois pour 1 load balancer à 3 règles de transfert et à 5 Mb/s pour 1 mois.

Base de données : db-custom-2-10240 (8 Go de RAM + 2 vCPU)

Prix : 150€99/mois pour 1 serveur de base de données
Sachant que j’ai pris un disque de stockage HDD (et non SDD) de 150 Go.

Le prix pour 50 Go de stockage revient à 10€ de moins.

TOTAL : 150€99/mois pour 1 serveur de base de données.


TOTAL FINAL pour 3 serveurs, 1 load balancer et 1 serveur de base de données : 162€58 + 22€28 + 150€99 = 335€85/mois
