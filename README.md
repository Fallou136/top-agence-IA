# top-agence-IA — TOP BUSINESS, plateforme marketing multi-agent

Une équipe d'agence IA prête à l'emploi, au service de tout le monde : 6 sous-agents
Claude Code (Stratège, SEO Local, Créateur, Designer, Analyste, Présentateur) orchestrés
pour mener une campagne marketing de PME locale de bout en bout.

## Installation

1. Installe Claude Code si ce n'est pas déjà fait :
   ```bash
   curl -fsSL https://claude.ai/install.sh | bash        # Mac / Linux / WSL
   # ou, sur Windows PowerShell :
   irm https://claude.ai/install.ps1 | iex
   ```
2. Vérifie l'installation et connecte-toi :
   ```bash
   claude --version
   claude auth login
   ```
3. Clone ce dépôt où tu veux sur ta machine, puis ouvre-le avec Claude Code :
   ```bash
   git clone https://github.com/fallou136/top-agence-ia.git
   cd top-agence-ia
   claude
   ```
   Claude Code lit automatiquement `CLAUDE.md` à l'ouverture du projet.

## Premier lancement

1. Duplique `clients/exemple-client/` en `clients/{nom-du-vrai-client}/` et remplis
   `brand.md` (obligatoire — c'est le garde-fou de marque lu par tous les agents).
2. Lance une campagne complète :
   ```
   /campagne pour {client}, objectif : {ex: augmenter les prises de RDV}
   ```
3. Ou lance une étape isolée : `/brief`, `/seo-local`, `/post`, `/visuel`, `/analyse`, `/deck`.

## Structure

```
CLAUDE.md                 → instructions racine, lu automatiquement
.claude/agents/            → les 6 agents (Stratège, SEO Local, Créateur, Designer, Analyste, Présentateur)
.claude/commands/          → les 7 slash commands
clients/{client}/          → mémoire par client (brand.md, icp.md, historique.md)
briefs/ seo-local/ content/ prompts-images/ analytics/ decks/
                            → livrables générés par les agents, un dossier par type
```

## Ajouter un agent plus tard

Crée un fichier `.claude/agents/nom-agent.md` avec un frontmatter YAML
(`name`, `description`, `tools`, `model`) suivi du prompt système de l'agent, en
suivant le format des agents existants. Ajoute-le au tableau du roster dans
`CLAUDE.md`.
