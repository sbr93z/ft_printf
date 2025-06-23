# ft_printf

Le projet ft_printf consiste à implémenter une version simplifiée de la fonction `printf` en C. Cette fonction doit permettre d'afficher différents types de données (int, char, string, etc.) tout en respectant un format spécifique, similaire à celui de la fonction standard.

## Description

- **Formatage** : La fonction `ft_printf` doit gérer divers types de formatage, comme les entiers (`d`), les caractères (`c`), les chaînes de caractères (`s`), et les pointeurs (`p`).
- **Variadic Function** : `ft_printf` est une fonction variadique, ce qui signifie qu'elle peut accepter un nombre variable d'arguments.
- **Conversion** : Elle convertit les arguments selon le format spécifié et les affiche.

## Installation

```bash
git clone git@github.com:sferrad/ft_printf.git
cd ft_printf
make
```
## Utilisation

Appel de la fonction ft_printf dans votre code pour afficher des données formatées :
```C
#include "ft_printf.h"

int main() {
    ft_printf("Hello, world! %d %s\n", 42, "Test");
    return 0;
}
```
## Exemple de sortie :
```bash
Hello, world! 42 Test
```
## Fichiers

ft_printf/ft_conv2.c : Fonctions de conversion pour certains types de données (par exemple, les unsigned int, etc.).

ft_printf/ft_conv.c : Fonctions de conversion principales (pour les types de base comme int, char, etc.).

ft_printf/ft_printf.c : Fonction principale qui implémente `ft_printf` et gère le formatage.

ft_printf/ft_printf.h : Header principal contenant les déclarations des fonctions et des macros nécessaires.

Makefile : Fichier pour compiler et nettoyer le projet.

## Commandes Makefile
```bash
make : Compile les programmes.

make clean : Supprime les fichiers objets.

make fclean : Supprime les fichiers objets et les exécutables.

make re : fclean puis make.
```
## Fonctionnement

La fonction ft_printf accepte un format spécifié sous forme de chaîne et des arguments variables. Elle parcourt la chaîne et, selon les spécificateurs de format (comme %d, %s), elle convertit et affiche les arguments correspondants. Les types pris en charge incluent les entiers, les caractères, les chaînes de caractères, et plus encore.

Le projet implémente une gestion complète des conversions et des flags pour fournir une expérience de formatage similaire à la fonction printf standard du C.
