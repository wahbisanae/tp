# Projet Java - Injection de dépendances via Réflexion

## Objectif
L'objectif de ce projet est de comprendre l'utilisation de la réflexion en Java pour instancier dynamiquement des classes, injecter des dépendances, et invoquer des méthodes. Le projet illustre l'usage de la programmation dynamique pour configurer une application sans dépendre d'une configuration statique.

## Structure du Projet

Le projet est structuré en trois packages principaux :
- `dao` : Contient l'interface `IDao` et son implémentation `DaoImpl`.
- `metier` : Contient l'interface `IMetier` et son implémentation `MetierImpl`.
- `presentation` : Contient la classe `Presentation2` qui utilise la réflexion pour charger et injecter dynamiquement les dépendances.

### Packages et Fichiers

#### 1. Package `dao`
- **`IDao.java`** : Interface qui déclare la méthode `getValue()` retournant un `double`.
- **`DaoImpl.java`** : Classe qui implémente l'interface `IDao` et retourne une valeur fixe `100.0` via `getValue()`.

#### 2. Package `metier`
- **`IMetier.java`** : Interface qui déclare la méthode `calcul()`.
- **`MetierImpl.java`** : Classe qui implémente l'interface `IMetier`. Cette classe dépend de `IDao` et effectue un calcul en doublant la valeur obtenue via `getValue()`.

#### 3. Package `presentation`
- **`Presentation2.java`** : Cette classe utilise la réflexion pour instancier dynamiquement `DaoImpl` et `MetierImpl`, injecter les dépendances et exécuter la méthode `calcul()`.

### Fichier de Configuration

Le fichier de configuration `config.txt` doit être placé à la racine du projet et contenir les noms des classes à charger via la réflexion. Exemple de contenu :

### video

https://github.com/user-attachments/assets/2b05fce8-e61e-47c2-b3d5-31b58b9fcf31

