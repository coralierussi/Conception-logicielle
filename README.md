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
    participant Utilisateur
    participant PGM
    participant Banque
    participant Base de Données
 
 
 
    Utilisateur->>PGM: Choisit de payer maintenant
    PGM->>PGM: Rediriger vers un lien paiement Paypal ou Visa
    Utilisateur->>PGM: remplir renseignement paiement
    PGM->>Banque: Envoie détails de transaction
    PGM->>Banque: Demande d'autorisation
    Banque->>PGM: Autorisation/Refus
    PGM->>Utilisateur: Confirmation de paiement
    PGM->>Base de Données: Met à jour informations utilisateur donnée bancaire
    Base de Données->>PGM: Confirmation de mise à jour
    PGM ->> Utilisateur: Acces au jeu
    PGM->>Utilisateur: Envoie email de confirmation d'achat et de création de compte
    Utilisateur ->> PGM: Completer compte
    PGM->>Base de Données: Met à jour informations utilisateur complet
    
``` 
#### Paiement plus tard

### Classe