## API : Exposer son SI ??? Not really !!


Il est important de comprendre qu'une API RESTFULL n'est surement pas une simple exposition directe d'un SI. Il est necessaire de voir un peu plus loin ! Mais pourquoi et comment ?? 

Pourquoi ..
Alors les SI sont en générale vieux (Legacy) ! Il faut comprendre que la construictions d'un SI est long et laborieux. Et qu'aujourd'hui, les pauvre babasse arrive avec une complexité. Ne jugeons pas cela, je risque d'avoir une responsabilité la dedans !! J'ai le sentiment que des refontes par le bas ont maintes fois été tenté dans les grosses structures, ne se soldant que trop souvent par des résultats mitigés pour des coups pharaonique! DOnc soit, cette complexité est la, et semble faire parti du squelette de notre SI !! Et beh.. on n'est pas super fier, on veut pas se montrer comme ca (cf: Sécu, qualité .. )!! Du coup faisons lui non pas un maquillage, mais un exosquelette, un truc qui claque !

UN exosquelette.. C'est a dire .. Beh comment rendre beau et rutilent et comprehensible un SI sous jacent . POur cela il faut passer par une logique metier ! Votre SI il fait quoi ! Un SI c'est avant tout des informations metier de celui ci . 

Revenons à une explication : 

Prenons l'assurance !! Comment fais t on un devis !!! En generale on envoi a un truc plusieur chose, genre une personne, une voiture, et quelque info ( ou t habites ) Et paf on vous renvoi un tarif  (enfin plusieur avec different niveau de couverture, mais la OSEF). Donc on a une notion de Personnes ( avec antecédent), un voiture ( appelons ca un Risque) ! Et cela retourne un tarif ( devis ?? ). Voila on est dans le schwarz !!! On arrive sur la problèmatique d'un SI. Les truc que l'on se passe il serve a quoi ???  Et c'est la qu'arrive cette belle notion '...' . On va tenter de ne manipuler que ce type d'entite... Appelons cela des ressources !! Que des 'choses' qui ont un sens!  (Disclaimer: la difficulté est ICI)

Et a partir de cela je dois pouvoir retrouver  tel machin . le sauvegarder le modifier et le suppr... 




https://blog.octo.com/designer-une-api-rest/
