**FastAPI sur Azure Container Instance : Implémentation de l'authentification AAD et du protocole TLS**
-

Nous verrons, dans un premier temps, comment mettre en place l'authentification Azure en local avec FastAPI. Dans un second temps, nous verrons comment implémenter le protocole TLS afin de pouvoir utiliser notre authentification dans le contexte d'une instance de conteneur Azure.

Les points de terminaison résultants ne pourront être utilisés que par un utilisateur authentifié et appartenant au locataire de l'API. Pour d'autres cas d'usages, se référer à la documentation fournie dans la section **Bibliographie**.

	Prérequis:
	* a
	* b
	* c
---
I - **Implémenter et utiliser l'authentification avec fastapi-azure-auth**

	Prérequis:
	* Python
	* Paquet fastapi-azure-auth

1.  **Configuration sur Azure** [1]

	1.1. **Côté Backend**
	
	**Inscrire l'application :** Head over to  [Azure -> Azure Active Directory -> App registrations](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ActiveDirectoryMenuBlade/RegisteredApps), and create a new registration.

Select a fitting name for your project; Azure will present the name to the user during consent.

-   `Supported account types`:  `Single tenant`  - If you want to create a multi-tenant application, you should head over to the  [multi-tenant documentation](https://intility.github.io/fastapi-azure-auth/multi-tenant/azure_setup)
-   `Redirect URI`: Choose  `Web`  and  `http://localhost:8000`  as a value

Press  **Register**
	1.2. **Côté Swagger**

2.  **Configuration sur FastAPI** [2]

3.  **Utilisation**

pas possible de l'utiliser sur azure parce que blabla, il faut https

---
II - **Implémenter le protocole TLS afin d'obtenir une adresse HTTPS**

	Prérequis:
	* a
	* b
	* c

bla

---
**Bibliographie**
[1] fastapi-azure-auth documentation: https://intility.github.io/fastapi-azure-auth/single-tenant/azure_setup/
[2] fastapi-azure-auth documentation: https://intility.github.io/fastapi-azure-auth/single-tenant/fastapi_configuration/
