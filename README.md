# 📚 Guide des Expressions Régulières (Regex) pour Débutants

Les **expressions régulières** (regex) sont des outils puissants pour rechercher et manipuler du texte. Ce guide vous apprendra les bases essentielles pour comprendre et utiliser les regex efficacement.

## 🌟 Sommaire

- [Introduction aux Regex](#introduction-aux-regex)
- [Caractères Littéraux](#caractères-littéraux)
- [Métacaractères](#métacaractères)
- [Classes de Caractères](#classes-de-caractères)
- [Quantificateurs](#quantificateurs)
- [Ancres](#ancres)
- [Groupes et Captures](#groupes-et-captures)
- [Exemples Pratiques](#exemples-pratiques)
- [Ressources pour s'Entraîner](#ressources-pour-sentraîner)

## 🔍 Introduction aux Regex

Les expressions régulières sont des motifs de recherche utilisés pour trouver des séquences spécifiques dans du texte. Elles sont composées de caractères littéraux et de caractères spéciaux appelés métacaractères.

## 🔤 Caractères Littéraux

Les caractères littéraux correspondent exactement à eux-mêmes. Par exemple, la regex `chat` trouvera le mot "chat" dans un texte.

## 🔣 Métacaractères

Les métacaractères ont des significations spéciales dans les regex:

| Métacaractère | Signification |
|---------------|---------------|
| `.`           | N'importe quel caractère sauf nouvelle ligne |
| `\d`          | Chiffre (0-9) |
| `\w`          | Caractère de mot (a-z, A-Z, 0-9, _) |
| `\s`          | Espace blanc (espace, tabulation, nouvelle ligne) |

## 📊 Classes de Caractères

Les classes de caractères permettent de spécifier un ensemble de caractères à rechercher:

- `[abc]` : Correspond à 'a', 'b', ou 'c'
- `[a-z]` : Correspond à n'importe quelle lettre minuscule
- `[^abc]` : Correspond à tout caractère sauf 'a', 'b', ou 'c'

## 🔢 Quantificateurs

Les quantificateurs spécifient combien de fois un élément doit apparaître:

- `*` : 0 ou plus
- `+` : 1 ou plus
- `?` : 0 ou 1
- `{n}` : Exactement n fois
- `{n,}` : Au moins n fois
- `{n,m}` : Entre n et m fois

## ⚓ Ancres

Les ancres définissent des positions dans le texte:

- `^` : Début de la ligne
- `$` : Fin de la ligne
- `\b` : Limite de mot

## 🎯 Groupes et Captures

Les parenthèses `()` créent des groupes de capture, permettant d'isoler des parties du motif:

- `(abc)` : Groupe capturant 'abc'
- `(?:abc)` : Groupe non-capturant

## 📌 Exemples Pratiques

1. Trouver un nombre à 3 chiffres : `\b\d{3}\b`
2. Valider un email simple : `^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$`
3. Trouver des mots de 4 à 6 lettres : `\b[a-zA-Z]{4,6}\b`

## 🧰 Ressources pour s'Entraîner

- [Regex101](https://regex101.com/) : Testez vos regex en temps réel
- [RegexOne](https://regexone.com/) : Tutoriel interactif pour apprendre les bases
- [RegExr](https://regexr.com/) : Outil d'apprentissage et de test avec une documentation intégrée

En maîtrisant ces concepts de base, vous serez en mesure de construire des expressions régulières efficaces pour diverses tâches de manipulation de texte.
