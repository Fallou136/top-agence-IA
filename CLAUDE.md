# TOP BUSINESS — Plateforme Marketing Multi-Agent

## Principe directeur

Claude Code est **l'orchestrateur**. Il ne produit JAMAIS de livrable lui-même : il route
la demande vers le bon sous-agent (dans `.claude/agents/`), lit ce que l'agent produit,
et enchaîne vers l'étape suivante si besoin. Chaque livrable a un auteur unique et
traçable.

## Roster des agents

| Agent | Fichier | Modèle | Rôle |
|---|---|---|---|
| Stratège | `.claude/agents/strategist.md` | Opus | Brief de campagne, positionnement, ICP |
| SEO Local | `.claude/agents/seo-local.md` | Opus | Google Business Profile, avis, citations locales, mots-clés géolocalisés |
| Créateur | `.claude/agents/creator.md` | Sonnet | Copy réseaux sociaux, scripts vidéo |
| Designer | `.claude/agents/designer.md` | Sonnet | Prompts images prêts à l'emploi |
| Analyste | `.claude/agents/analyst.md` | Opus | Rapport de performance, plan d'optimisation 30j |
| Présentateur | `.claude/agents/presenter.md` | Sonnet | Deck client à partir des livrables précédents |

## Arborescence des livrables

```
briefs/            → Stratège
seo-local/          → SEO Local
content/            → Créateur
prompts-images/     → Designer
analytics/          → Analyste
decks/              → Présentateur
clients/{client}/   → brand.md, icp.md, historique.md (mémoire client)
```

## Convention critique — frontmatter YAML obligatoire

Chaque fichier produit par un agent DOIT commencer par :

```yaml
---
client: nom-du-client
campagne: nom-de-la-campagne
agent: nom-de-l-agent
date: AAAA-MM-JJ
version: 1
statut: brouillon | a-valider | approuve
---
```

Ceci rend la chaîne auditable : un agent peut relire ce qu'un autre a produit avant lui
(via son frontmatter et son contenu), et l'humain peut suivre l'état de chaque
livrable d'un coup d'œil.

## Garde-fou de marque

Avant TOUTE production, chaque agent doit lire `clients/{client}/brand.md`. Les
interdictions qui y sont listées (jargon banni, palette imposée, ton, vouvoiement /
tutoiement) sont **bloquantes** : un livrable qui les viole n'est pas livré, l'agent
recommence.

## Workflow séquentiel — commande `/campagne`

Les étapes sont dépendantes, donc séquentielles (pas en parallèle) :

1. **Stratège** — reçoit l'objectif → produit le brief (`briefs/`)
2. **SEO Local** — lit le brief → audit + mots-clés géolocalisés + fiche GMB (`seo-local/`)
3. **Créateur** — lit le brief + le SEO local → 3 à 5 pièces de contenu (`content/`)
4. **Designer** — lit le brief + le contenu → prompts images tous formats (`prompts-images/`)
5. **Présentateur** — consolide tout → deck client (`decks/`)
6. **J+30 : Analyste** — lit les exports analytics → rapport + plan d'optimisation (`analytics/`)

Une validation utilisateur est requise après chaque étape marquée `a-valider` avant de
passer à la suivante.

## Règle absolue pour l'Analyste

Aucune métrique n'est jamais inventée. Si une donnée manque, "Donnée manquante" est
une réponse valide et attendue — jamais une estimation présentée comme un fait.

## Slash commands disponibles

Voir `.claude/commands/` : `/brief`, `/seo-local`, `/post`, `/visuel`, `/analyse`,
`/deck`, `/campagne`.
