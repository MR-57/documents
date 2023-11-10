**FastAPI sur Azure Container Instance : Implémentation de l'authentification AAD et du protocole TLS**
-

Nous verrons, dans un premier temps, comment mettre en place l'authentification Azure en local avec FastAPI. Dans un second temps, nous verrons comment implémenter le protocole TLS afin de pouvoir utiliser notre authentification dans le contexte d'une instance de conteneur Azure.

Les points de terminaison résultants ne pourront être utilisés que par un utilisateur authentifié et appartenant au locataire de l'API.

Prérequis:
* a
* b
* c
---
I - **Implémenter et utiliser l'authentification avec fastapi-azure-auth**

  

1.  **Configuration sur Azure** [1]

	1.1. **Côté Backend**
	
	1.2. **Côté Swagger**

2.  **Configuration sur FastAPI** [2]

3.  **Utilisation**
pas possible de l'utiliser sur azure parce que blabla, il faut https
---
II - **Implémenter le protocole TLS afin d'obtenir une adresse HTTPS**
bla

---
**Bibliographie**
[1] fastapi-azure-auth documentation: https://intility.github.io/fastapi-azure-auth/single-tenant/azure_setup/
[2] fastapi-azure-auth documentation: https://intility.github.io/fastapi-azure-auth/single-tenant/fastapi_configuration/
