# AGENTS.md

Instructions pour tout agent de code IA (Claude Code, Copilot, Codex...) qui travaille dans ce dépôt.

## Le projet

Liste « awesome » d'**outils techniques de mesure d'impact** (éco-conception, green IT), axés sur le développement et l'intégration. Pas de littérature ni d'articles : seulement des outils. L'ambition de zatsit est de les tester et d'en publier un REX ou un tutoriel sur le [blog](https://blog.zatsit.fr). Voir [README.md](README.md).

Il n'y a ni code, ni build, ni tests : tout le contenu est dans `README.md`.

## Structure

- `README.md` : la liste, en français. En tête de fichier, les définitions des badges de statut (liens de référence Markdown) ; puis l'introduction, puis une section `##` par catégorie.
- `CONTRIBUTING.md` : règles de contribution (en anglais), syntaxe des badges.
- `CODE_OF_CONDUCT.md`, `LICENSE` (MIT).

Catégories actuelles : `Général`, `Web`, `Kubernetes`, `Librairies`, puis `Autres dépots sur la thématique green` (autres listes awesome, pas des outils).

## Ajouter un outil

1. Vérifier que c'est bien un outil technique permettant de mesurer un impact, et qu'il n'est pas déjà listé.
2. Le placer dans la bonne catégorie. Les entrées ne sont pas triées alphabétiquement : jusqu'ici, chaque ajout a été placé en fin de catégorie. Ne créer une nouvelle catégorie `##` que si aucune ne convient, avant `Autres dépots sur la thématique green`.
3. Rédiger l'entrée sur une seule ligne, en français, au format :

```markdown
- [Nom](https://lien-vers-la-doc): Description claire de l'objectif de l'outil. <br/>![Techno](url-du-badge-techno) ![z-status][not_tested]
```

- Lien vers la documentation ou le site officiel de l'outil, puis `:` et la description. Mettre le nom de l'outil entre backticks dans la description quand il est cité (`` `IF` ``, `` `Ecograder` ``).
- Après `<br/>`, le badge de technologie (optionnel, quand c'est pertinent), puis le badge de statut zatsit (**obligatoire**).
- Badge de technologie : à copier depuis [markdown-badges](https://github.com/Ileriayo/markdown-badges), comme indiqué dans CONTRIBUTING.md.

## Badges de statut zatsit

Toujours utiliser les références définies en haut du README, avec le texte alternatif `z-status` :

| Référence | Quand l'utiliser |
|---|---|
| `![z-status][not_tested]` | outil proposé mais pas encore testé (cas par défaut d'un nouvel ajout) |
| `![z-status][in_progress]` | test en cours, quand il demande plusieurs semaines |
| `![z-status][tested]` | outil testé en profondeur, de quoi écrire un article |
| `[![z-status][rex]](lien-article)` | un REX existe sur le blog : le badge doit être cliquable vers l'article |
| `[![z-status][tutorial]](lien-tuto)` | un tutoriel existe sur le blog : badge cliquable vers le tutoriel |
| `[![z-status][project]](lien-repo)` | un dépôt open source zatsit existe : badge cliquable vers ce dépôt |

Ne jamais inventer de lien de blog ou de dépôt : si l'URL n'est pas fournie, demander.

## Conventions

- Contenu du README en français ; CONTRIBUTING.md en anglais.
- Messages de commit au format [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) (exigé par CONTRIBUTING.md). L'historique utilise `feat:` ou `docs:` pour un ajout d'outil (`docs: adds EcoLogits library`).

## Pièges connus

- **Ne pas modifier les définitions de badges** en tête du README : ce sont de longues URLs shields.io avec un logo en base64 sur une seule ligne. Un retour à la ligne ou une troncature casse tous les badges.
- Le badge `[project]` n'existe que dans le README, pas dans CONTRIBUTING.md, et les libellés diffèrent légèrement (`Testée` contre `Testé`). Le README fait foi.
- Écrire `<br/>` pour le saut de ligne (une entrée existante utilise `</br>`, à ne pas reproduire).
- Une modification de statut (par exemple `not_tested` vers `tested`) se fait sur l'entrée existante, sans la déplacer.
