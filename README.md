# 🎓 Maîtrisez les Expressions Régulières (Regex)

## 📚 Table des Matières

1. [Introduction aux Regex](#1-introduction-aux-regex)
2. [Syntaxe de Base](#2-syntaxe-de-base)
3. [Métacaractères Essentiels](#3-métacaractères-essentiels)
4. [Classes de Caractères](#4-classes-de-caractères)
5. [Quantificateurs](#5-quantificateurs)
6. [Ancres et Limites](#6-ancres-et-limites)
7. [Groupes et Captures](#7-groupes-et-captures)
8. [Assertions](#8-assertions)
9. [Techniques Avancées](#9-techniques-avancées)
10. [Exemples Pratiques](#10-exemples-pratiques)
11. [Outils et Ressources](#11-outils-et-ressources)

---

## 1. Introduction aux Regex

Les expressions régulières (regex) sont des séquences de caractères qui définissent un motif de recherche. Elles sont utilisées pour :

- 🔍 Rechercher du texte
- ✏️ Valider des formats
- 🔄 Remplacer du contenu

## 2. Syntaxe de Base

Une expression régulière est construite à partir de caractères littéraux et de métacaractères.

### Caractères Littéraux

Les caractères littéraux correspondent exactement à eux-mêmes. Par exemple, la regex `chat` trouvera le mot "chat" dans un texte.

## 3. Métacaractères Essentiels

Les métacaractères ont des significations spéciales dans les regex:

| Métacaractère | Signification                                       |
|---------------|-----------------------------------------------------|
| `.`           | N'importe quel caractère sauf nouvelle ligne        |
| `\d`          | Chiffre (0-9)                                      |
| `\w`          | Caractère de mot (a-z, A-Z, 0-9, _)                |
| `\s`          | Espace blanc (espace, tabulation, nouvelle ligne)  |

## 4. Classes de Caractères

Les classes de caractères permettent de spécifier un ensemble de caractères à rechercher :

- `[abc]` : Correspond à 'a', 'b', ou 'c'
- `[a-z]` : Correspond à n'importe quelle lettre minuscule
- `[^abc]` : Correspond à tout caractère sauf 'a', 'b', ou 'c'

## 5. Quantificateurs

Les quantificateurs spécifient combien de fois un élément doit apparaître :

| Quantificateur | Signification                   |
|----------------|----------------------------------|
| `*`            | 0 ou plus                       |
| `+`            | 1 ou plus                       |
| `?`            | 0 ou 1                          |
| `{n}`         | Exactement n fois               |
| `{n,}`        | Au moins n fois                 |
| `{n,m}`       | Entre n et m fois               |

## 6. Ancres et Limites

Les ancres définissent des positions dans le texte :

| Ancre   | Signification              |
|---------|----------------------------|
| `^`     | Début de la ligne          |
| `$`     | Fin de la ligne            |
| `\b`    | Limite de mot              |

## 7. Groupes et Captures

Les parenthèses `()` créent des groupes de capture, permettant d'isoler des parties du motif :

- `(abc)` : Groupe capturant 'abc'
- `(?:abc)` : Groupe non-capturant

## 8. Assertions

Les assertions permettent de définir des conditions sans consommer de caractères :

- `(?=abc)` : Assertion positive (suivi par 'abc')
- `(?!abc)` : Assertion négative (non suivi par 'abc')

## 9. Techniques Avancées

### Lookahead et Lookbehind

Ces techniques permettent d'affiner vos recherches :

- **Lookahead** : `(?=...)`
- **Lookbehind** : `(?<=...)`

### Modificateurs

Certains modificateurs peuvent changer le comportement d'une regex :

- `i` : Ignorer la casse
- `m` : Multiligne

## 10. Exemples Pratiques

1. **Trouver un nombre à 3 chiffres** : `\b\d{3}\b`
2. **Valider un email simple** : `^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$`
3. **Trouver des mots de 4 à 6 lettres** : `\b[a-zA-Z]{4,6}\b`

## 11. Outils et Ressources

- [Regex101](https://regex101.com/) : Testez vos regex en temps réel
- [RegexOne](https://regexone.com/) : Tutoriel interactif pour apprendre les bases
- [RegExr](https://regexr.com/) : Outil d'apprentissage et de test avec documentation intégrée
