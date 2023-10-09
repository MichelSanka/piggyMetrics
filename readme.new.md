Préambule
--
Piggy est une application très lourde à déployer. Elle nécessite environ 15G de mémoire. 
Seuls les services nécessaires aux tests qu'on veut réaliser et qui \
concernent la partie microservice de Nudge, sont déployés par le fichier docker-compose. Les autres services, `notification-service`, \
et sa base mongo associé `notification-mongodb`, `rabbitmq`, `turbine-stream-service` et `monitoring-service` sont désactivés \
dans le docker-compose. Vous pouvez les activer juste en enlevant les commentaires sur les parties correspondantes. 

Etapes de déploiement
--
1. Packager les différents services : `mvn clean install -DskipTests`
2. Créer toutes les applications correspondantes aux services sur le server NudgeAPM
3. Dans chaque service à instrumenter, ouvrir le fichier `java-agent/nudge.properties` et remplir les champs app_id et server_url
4. lancer le docker-compose : `docker-compose up -d`

Erreur lors du lancement
-- 
Il peut arriver que lors du lancement, il y ait des problèmes de connexion des services avec `config-service`, dans ce \
cas, stopper le conteneur et relancer le.
Il se peut aussi que les problèmes les erreurs de lancements soient dues à un manque d'espace, dans ce cas, il faudra \
désactiver certains services et relancer le docker-compose 