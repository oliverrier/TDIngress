# TD Ingress Kubernetes

## Fichiers de conf

Vous avez le fichiers de conf de chacun des modules de Kubernetes que l'on utilise pour ce TD dans le répertoire `conf`

## Lignes de commande

Vous allez devoir apply chacun des modules qui sont dans le dossier conf grâce à la commande `kubectl apply -f`

Voilà la liste des modules à apply :

- Le namespace : `kubectl apply -f conf/namespace.yml`
- Le RessourceQuota : `kubectl -n hello-world apply -f conf/ressourcequota.yml`
- Le deployment : `kubectl -n hello-world apply -f conf/deployment.yml`
- Le service : `kubectl -n hello-world apply -f conf/service.yml`

A partir de ce moment vous pouvez accéder à vos docker hello world qui ont été créés par le deployment via un adresse ip générée par le service grâce à la commande de port-forward :

Port forward : `kubectl port-forward service/hello-world-service 8080:80`
Ensuite go navigateur : localhost:8080

- L'Ingress : `kubectl -n hello-world apply -f ingress.yml`

Faites `kubectl -n hello-world get ingress`

Go fichier hosts :

- `/etc/hosts` sur Linux
- `C:\Windows\system32\drivers\etc\hosts`

Rajouter une ligne avec l'ip et le nom de domaine défini dans le fichier hosts

L'ip sera générée mais le nom de domaine est hello-world.ingress

Un beau Hello world vous attends.

GG WP
