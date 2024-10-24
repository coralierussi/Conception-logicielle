# Conception logiciel
## Sujet
Création d'un site / jeu vidéo pour une formation sur le DarkWeb avec un système d'abonnement de paiement.

On se concentre sur "Conclure" du tunnel d'achat.
## Cibles
Mineurs et étudiants (-25 ans)
## Diagramme
### Use case

### Séquence
#### Paiement maintenant

```ts
     participant PGM
    participant Banque
    participant Base de Données
    actor Utilisateur
 
    PGM->>Base de Données: Creation user anonyme (pseudo, mail)
    Base de Données->>PGM: id compte anonyme et adresse mail
    PGM->>PGM: Rediriger vers un lien paiement Paypal ou Visa
    PGM->>PGM: remplir renseignement paiement
    PGM->>Banque: Envoie détails de transaction + autorisation
    Banque->>PGM: Autorisation
    PGM->>PGM: Confirmation de paiement
    PGM->>Base de Données: Met à jour informations utilisateur donnée bancaire
    Base de Données->>PGM: Confirmation de mise à jour
    PGM ->> PGM: Acces au jeu
    PGM->>Utilisateur: Envoie email de confirmation d achat et de création de compte
    Utilisateur ->> PGM: Redirection page creation compte (id compte anonyme)
    PGM ->> PGM:  completer compte
    PGM->>Base de Données: Met à jour informations utilisateur complet (email?, mtp,id compte anonyme)
    Base de Données->>PGM: ok
    PGM ->>Utilisateur : Mail de confirmation creation du compte
```

![Img diagramme de séquence paiement now](image-3.png)
#### Paiement plus tard

### Classe