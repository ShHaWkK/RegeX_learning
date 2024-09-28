# 📚 Guide des Expressions Régulières (Regex)

Les **expressions régulières** (regex) sont des outils puissants pour rechercher, manipuler et valider des chaînes de caractères. Ce guide vous apprendra les bases et vous guidera à travers des exemples pratiques.

## 🌟 Sommaire

- [Introduction aux Regex](#introduction-aux-regex)
- [Syntaxe de Base](#syntaxe-de-base)
- [Groupes de Captures et Références](#groupes-de-captures-et-références)
- [Assertions et Lookahead](#assertions-et-lookahead)
- [Exemples Courants](#exemples-courants)
- [Ressources et Outils](#ressources-et-outils)

---

## 🔍 Introduction aux Regex

Les **expressions régulières** (regex) sont une séquence de caractères qui forment un modèle de recherche. Elles sont utilisées pour effectuer des tâches comme :

- Valider des formats de texte (emails, numéros de téléphone, etc.)
- Trouver et remplacer du texte dans une chaîne
- Extraire des données spécifiques d'un texte

---

## 🔤 Syntaxe de Base

Voici quelques symboles de base utilisés dans les expressions régulières :

| Symbole   | Signification                                   | Exemple        |
|-----------|-------------------------------------------------|----------------|
| `.`       | Correspond à **n'importe quel caractère**       | `a.b` → "a9b"  |
| `^`       | Correspond au **début d'une ligne**             | `^Bonjour`     |
| `$`       | Correspond à **la fin d'une ligne**             | `monde$`       |
| `[]`      | **Classe de caractères**, correspond à l'un d'eux | `[abc]` → "a" ou "b" ou "c" |
| `|`       | **OU logique**                                  | `a|b` → "a" ou "b" |
| `*`       | 0 ou plusieurs occurrences                      | `ab*c` → "ac", "abc", "abbc" |
| `+`       | 1 ou plusieurs occurrences                      | `ab+c` → "abc", "abbc" |
| `{n}`     | Exactement n occurrences                        | `a{3}` → "aaa" |

### Exemple :

Pour capturer un email simple :
```regex
^[\w\.-]+@[\w\.-]+\.[a-zA-Z]{2,}$
```

## 🎯 Groupes de Captures et Références

Les groupes de captures permettent de capturer des sous-chaînes de caractères que vous pouvez réutiliser. Ils sont définis avec des parenthèses ().

Syntaxe :
(abc) : Capture "abc"
\1 : Référence au premier groupe capturé
Exemple :
Pour capturer un domaine et le réutiliser :
```regex
(\w+)\.com
```
Résultat : Capture le domaine et peut être référencé plus tard.

## 🛠 Assertions et Lookahead

Les assertions sont des conditions qui doivent être vraies pour une correspondance, mais qui ne capturent pas de texte. Il y a deux types principaux d'assertions :

Lookahead positif : (?=...)
Vérifie qu'une certaine séquence suit sans la capturer.
Exemple : Trouver un chiffre suivi de "€" :

```regex
\d(?=€)
```
Lookahead négatif : (?!...)
Vérifie qu'une séquence n'est pas suivie d'une certaine chaîne.
Exemple : Un chiffre non suivi de "€" :

```regex

\d(?!€)
```
## 📌 Exemples Courants

Valider une adresse email
```regex

^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```
Trouver un numéro de téléphone
```regex
^(\+?\d{1,3}[-.\s]?)?\(?\d{1,4}\)?[-.\s]?\d{1,4}[-.\s]?\d{1,9}$
```
Capturer une URL
```regex
https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)
```
🧰 Ressources et Outils

Regex101 : Outil interactif pour tester et comprendre les regex.
RegExr : Un autre éditeur en ligne pour expérimenter avec les regex.
RegexOne : Un excellent tutoriel interactif pour apprendre les regex étape par étape.
