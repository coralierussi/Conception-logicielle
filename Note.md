# Diagram

## Séquence
*Code de diagramme de séquence*

``` ts
sequenceDiagram

    participant Prgm
    participant Animal

    Prgm->>Animal: créer (cat, Barsik)
    Animal ->> Prgm : cat Barsik
    Prgm->>Animal: transformToDog
    Animal->> Animal : changeToDog
    Animal ->> Prgm : Ok
    Prgm->>Animal: voice
    Animal->> Animal : Afficher (type + nom)
    Animal ->> Prgm : afficher (type + nom)
    Prgm->>Animal: ohnanaWhatsMyName ()
    Animal ->> Prgm : nom animal
    Prgm ->> Prgm : Afficher (name)
```


## Class
``` ts
classDiagram
    Animal
    Animal : +string name
    Animal : +String Type "Cat" | "Doggy"
    Animal: +transformToDog()
    Animal: +voice()
    Animal: +ohnanaWhatsMyName()
```