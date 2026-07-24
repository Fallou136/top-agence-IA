---
client: teranga-beach
campagne: lancement-digital-2026
agent: designer
date: 2026-07-24
version: 1
statut: approuve
---

# Pack de prompts images — Téranga Beach · « Lancement Digital 2026 »

Ce livrable décline en visuels les 4 contenus approuvés du Créateur :
1. Facebook — « Le coucher de soleil vaut le déplacement »
2. Facebook — « Le poisson frais du jour, fait maison »
3. Reel/TikTok — « Golden Hour à Téranga Beach »
4. Facebook — « L'accueil d'Abdou, l'esprit téranga »

Formats livrés pour chaque visuel : **1:1** (1080×1080, feed FB/IG) · **4:5** (1080×1350,
feed IG portrait) · **9:16** (1080×1920, Stories/Reels/TikTok) · **16:9** (1920×1080,
couverture FB, bandeau site, miniature YouTube).

---

## 0. Garde-fous obligatoires (lus dans `clients/teranga-beach/brand.md`)

1. **Palette NON validée par le client.** La palette bleu mer / sable-beige /
   touches terracotta-coucher de soleil utilisée dans les prompts ci-dessous est une
   **recommandation par défaut**, cohérente avec le lieu, mais **elle doit être
   confirmée par le client avant toute impression ou déploiement final** (charte
   graphique, réseaux sociaux, mini-site). Tant que non validée, considérer chaque
   visuel « à ajuster colorimétriquement » si le client fournit d'autres préférences.
2. **Stock générique interdit.** Aucun visuel ne doit ressembler à une banque
   d'images « plage tropicale générique ». Voir section 0.2 ci-dessous sur le risque
   spécifique de généricité IA pour ce lieu.
3. **Vraies photos = priorité absolue.** Pour une PME locale déjà dotée d'un lieu
   photogénique réel (plage, transats, plats, équipe), une vraie photo/vidéo du lieu
   sera **toujours plus convertissante et plus conforme à la marque** qu'une image
   générée. Les prompts IA de ce document sont des **plans de secours ou des
   compléments d'ambiance**, à n'activer que si une vraie photo n'existe pas ou pas
   en qualité suffisante.
4. **Aucune fausse preuve sociale.** Ne jamais générer ni suggérer de trophées,
   labels, étoiles ou récompenses non confirmés par le client.
5. **Cohérence avec « loin de la foule ».** Le territoire éditorial n°1 revendique
   un spot authentique et peu fréquenté. Aucun visuel ne doit montrer une plage
   bondée ou une ambiance de club de plage surpeuplé — cela contredirait le
   positionnement.
6. **Abdou et l'équipe : personnes réelles nommées.** Il est **exclu de générer un
   visage IA et de le présenter comme « Abdou »** ou comme un membre de l'équipe :
   ce serait une usurpation d'identité d'une vraie personne citée dans les avis, et
   une atteinte directe à l'authenticité revendiquée par la marque. Voir détail au
   visuel 4.

### 0.2 Risque de généricité IA spécifique à ce lieu (à anticiper dans les prompts)

La Petite Côte sénégalaise (Warang Sérère) a un visage précis, différent des clichés
« plage tropicale » que les IA génératives produisent par défaut (palmiers
touffus, sable blanc éclatant, eau turquoise type Caraïbes/Asie du Sud-Est). Le vrai
site est plutôt : sable doré à beige, filaos (pins de bord de mer) et cocotiers
clairsemés, pirogues de pêcheurs sénégalaises au loin, ciel qui vire à l'orangé/rose
franc au coucher de soleil, ambiance Sahel côtier. **Chaque prompt ci-dessous
intègre ces éléments distinctifs** pour limiter le risque de rendu « stock
générique », mais le résultat restera une approximation — d'où la priorité donnée
à la vraie photo (§0.1 point 3).

---

## 1. Visuel — « Le coucher de soleil vaut le déplacement » (Facebook, angle 1)

### Recommandation prioritaire — VRAIE PHOTO
Le post du Créateur demande la **photo prioritaire n°1** : coucher de soleil sur la
plage de Warang Sérère, transats au premier plan. **Statut signalé « à confirmer »**
dans le contenu source (disponibilité réelle non vérifiée). Action recommandée :
1. Vérifier en priorité si Téranga Beach possède déjà une photo/vidéo golden hour
   récente et net (téléphone du gérant, réseaux sociaux existants, clients ayant
   partagé des photos avec autorisation).
2. Si oui → shooting/retouche légère uniquement, **pas de génération IA**.
3. Si non → programmer une prise de vue réelle un soir dégagé (peu coûteux, un
   smartphone récent suffit en golden hour) **avant** d'utiliser les prompts IA
   ci-dessous, qui ne sont qu'un dépannage temporaire.

### Prompts IA de secours (si aucune vraie photo/vidéo disponible sous 2 semaines)

**Outil recommandé : Midjourney v6** (meilleur rendu photoréaliste cinématique pour
lumière dorée, textures sable/eau, ambiance golden hour). Éviter tout texte dans
l'image (voir note plus bas).

Prompt de base (à décliner par ratio) :
> Photoréaliste, coucher de soleil sur une plage de la Petite Côte sénégalaise
> (Warang), sable doré, transats en bois et tissu clairs vides au premier plan
> orientés vers l'océan, quelques filaos (pins de bord de mer) discrets sur le
> côté, une pirogue de pêcheur sénégalaise au loin sur l'eau, ciel qui s'embrase en
> orangé et rose, réflexion du soleil sur l'eau calme, ambiance chaleureuse et
> paisible, aucune foule, aucune personne visible ou une silhouette discrète assise
> de dos, palette bleu marine profond / sable beige / touches terracotta-orangé
> (recommandation à valider), lumière naturelle basse, style photo de voyage
> authentique, pas de logo, pas de texte incrusté, format --ar {ratio}

- **1:1** → `--ar 1:1` — cadrage centré sur 2-3 transats et l'horizon, bon pour feed.
- **4:5** → `--ar 4:5` — recadrage vertical resserré sur les transats + ciel, laisser
  de l'espace en haut pour un éventuel sticker/légende IG.
- **9:16** → `--ar 9:16` — plan plus large verticalement : sable en bas, transats au
  milieu, grand ciel orangé en haut (pour Stories/Reels cover).
- **16:9** → `--ar 16:9` — plan large panoramique océan/horizon, idéal bandeau
  site ou couverture Facebook.

**Alternative outil** : Gemini Imagen si Midjourney indisponible — bonne fidélité
au prompt mais rendu légèrement moins « cinéma », correct en dépannage.

**Texte dans le visuel** : le post prévoit d'intégrer le verbatim de Sébastien
(« Le coucher de soleil vaut vraiment le déplacement... ») **dans la légende du
post, pas dans l'image**. Si une version « carte citation » est envisagée plus tard
(texte incrusté sur l'image), signaler explicitement : **risque élevé de texte
illisible ou déformé si généré directement par Midjourney/Imagen**. Recommandation :
ajouter le texte en post-production (Canva, Figma) sur l'image finale, ou utiliser
Ideogram (meilleur rendu typographique) avec un texte très court (≤ 6-8 mots) et
relecture manuelle obligatoire avant publication.

---

## 2. Visuel — « Le poisson frais du jour, fait maison » (Facebook, angle 2)

### Recommandation prioritaire — VRAIE PHOTO
Le post demande la **photo prioritaire n°2** : assiette signature calamars/crevettes
sautés + frites maison, en gros plan. **C'est le cas d'usage le plus favorable à la
vraie photo** : un plat déjà servi en cuisine peut être photographié en 10 minutes
avec un smartphone et une lumière naturelle (près d'une fenêtre ou en terrasse),
pour un résultat plus appétissant et plus fidèle qu'une génération IA — la
génération IA de plats spécifiques (calamars/crevettes molles sautées version
Téranga Beach) risque de produire un plat plausible mais générique, pas *le* plat
du restaurant. **Fortement recommandé : shooting réel en cuisine avant recours à
l'IA.**

### Prompts IA de secours (dépannage uniquement, si aucun plat ne peut être
photographié à temps pour la publication)

**Outil recommandé : Gemini Imagen** (meilleure fidélité culinaire/texture pour la
food photography que Midjourney sur ce type de plan rapproché produit/assiette) ou
**Midjourney v6** en variante plus stylée.

Prompt de base :
> Photographie culinaire réaliste, gros plan sur une assiette de calamars et
> crevettes molles sautés grillés dorés, accompagnés de frites maison croustillantes
> et d'un quartier de citron, servie dans une assiette simple sur une table en bois
> clair de restaurant de plage, lumière naturelle chaude en fin de journée, léger
> flou d'arrière-plan laissant deviner du sable et l'océan, ambiance bord de mer
> Petite Côte sénégalaise, pas de logo, pas de texte, style photo appétissante et
> naturelle (pas de studio léché), format --ar {ratio}

- **1:1** → `--ar 1:1` — assiette centrée, feed.
- **4:5** → `--ar 4:5` — assiette légèrement décentrée, espace en haut pour légende IG.
- **9:16** → `--ar 9:16` — plan vertical serré sur l'assiette + un bout de table,
  cadrage Story/Reel.
- **16:9** → `--ar 16:9` — assiette à gauche/droite, table + horizon flou en
  arrière-plan, format bandeau/site.

**Texte dans le visuel** : aucun texte prévu dans l'image (le CTA WhatsApp reste en
légende de post). Ne pas ajouter de mention de prix ou de nom de plat en incrustation
— cela reviendrait à publier un menu/prix non validé (interdiction bloquante du
brief).

---

## 3. Visuel — « Golden Hour à Téranga Beach » (Reel/TikTok, angle 1 vidéo)

### Recommandation prioritaire — TOURNAGE RÉEL (rappel du Créateur : obligatoire)
Le script précise noir sur blanc : **« Vraies images du lieu obligatoires »** et
**« tournage réel requis, pas de stock ni de banque d'images génériques »**. Le rôle
du Designer ici se limite à :
1. des **prompts de secours pour des plans isolés** si un plan précis du storyboard
   s'avère impossible à filmer à temps (ex. absence d'Abdou le jour du tournage,
   cf. note du Créateur sur le plan 7) ;
2. des **visuels statiques dérivés** (miniature de couverture, extraits repostables
   en 1:1/4:5/16:9 sur Facebook/Instagram feed) une fois la vidéo réelle tournée et
   montée.

### 3.1 Prompts IA de secours pour un plan isolé manquant (jamais pour toute la vidéo)

**Outil recommandé : Midjourney v6** pour cohérence de lumière/ambiance avec les
autres plans golden hour déjà filmés.

Exemple — plan de secours « vagues + transats en silhouette » (plan 4 du storyboard,
si le plan filmé est inutilisable) :
> Photoréaliste, gros plan sur des vagues douces qui viennent lécher un sable doré
> au coucher du soleil, silhouettes de transats en bois visibles en arrière-plan
> flou, lumière rasante orangée, reflets sur l'eau, ambiance Petite Côte sénégalaise
> (Warang), aucune foule, aucun texte, aucun logo, format --ar {ratio}

- **9:16** (`--ar 9:16`) : format natif du Reel — prompt à privilégier en premier.
- **1:1**, **4:5**, **16:9** : uniquement pour des reposts du même plan en dehors du
  Reel (feed statique), recadrages du même prompt.

**Attention plan 7 (Abdou/équipe)** : le Créateur signale une donnée manquante sur
la disponibilité d'un plan filmé d'Abdou en golden hour. **Ne jamais combler ce vide
par un visage généré par IA présenté comme Abdou ou un membre de l'équipe** (cf.
garde-fou §0.1 point 6). Si le plan n'est pas disponible, le Créateur prévoit déjà
un remplacement conforme (plan supplémentaire de plage ou de plat signature) — suivre
cette consigne, ne pas généré de figurant IA en tenue de serveur pour combler.

### 3.2 Miniatures / vignettes de couverture (à partir du montage réel une fois tourné)

Une fois la vidéo réelle montée, en extraire une image fixe (frame du plan 1 ou 5 —
plage/transats/ciel orangé) pour servir de **miniature de couverture** sur les
plateformes qui l'exigent (couverture Reel Facebook, vignette YouTube Shorts) :
- **9:16** : couverture native du Reel/TikTok (frame extraite directement, pas de
  génération).
- **1:1 / 4:5 / 16:9** : recadrages de la même frame pour publication croisée en
  post statique sur le feed — **retouche photo classique, pas de génération IA**
  recommandée ici (cohérence colorimétrique avec la vidéo réelle).

### 3.3 Textes prévus dans le Reel — RISQUE D'ILLISIBILITÉ SIGNALÉ

Le storyboard du Créateur prévoit **deux inserts texte** :
- **Plan 6 (13-16s)** : « Téranga Beach — Warang Sérère, à 5 km de Mbour, Petite
  Côte » en plein écran.
- **Plan 8 (19-24s)** : « Réservez votre table au coucher du soleil » + « WhatsApp
  +221 77 754 90 89 ».

**Signalement explicite (obligatoire)** : ces textes — en particulier le **numéro de
téléphone/WhatsApp** — **ne doivent jamais être générés par un outil d'image ou de
vidéo IA** (Midjourney, Imagen, Sora-like). Le risque de chiffres déformés ou
illisibles est élevé et une erreur sur ce numéro est critique (perte de réservation).
**Recommandation ferme** : ajouter ces textes en post-production avec un éditeur
vidéo classique (CapCut, Premiere, Canva Vidéo) en texte natif éditable, avec
relecture manuelle systématique avant publication. Idem pour les hooks A/B en
overlay (plan 1) et les sous-titres — texte natif éditeur, jamais incrusté par
génération IA.

---

## 4. Visuel — « L'accueil d'Abdou, l'esprit téranga » (Facebook, angle 3)

### Recommandation prioritaire — VRAIE PHOTO (obligatoire, pas de solution IA de repli acceptable pour Abdou lui-même)
Le post demande la **photo prioritaire n°5** : Abdou et l'équipe en situation
d'accueil. Le Créateur signale une **donnée à confirmer : accord d'Abdou et de
l'équipe pour apparaître nommément et en photo**.

**Point de vigilance majeur (garde-fou renforcé)** : ce visuel repose sur une
personne réelle et nommée dans les avis clients (Abdou) ainsi que sur une équipe
réelle. Il est **exclu de produire une image générée par IA représentant un homme
et la présentant, même implicitement, comme « Abdou »** — ce serait trompeur pour
l'audience et contraire à l'authenticité revendiquée. **Il n'y a donc pas de prompt
IA de secours proposé pour ce visuel en remplacement direct d'Abdou.**

Actions recommandées, dans l'ordre :
1. Confirmer avec Abdou et l'équipe leur accord pour apparaître en photo (préalable
   bloquant, à traiter avant tout shooting ou publication).
2. Organiser une prise de vue réelle : Abdou souriant, en situation d'accueil
   (accueillant un client fictif ou en pied sur la terrasse/plage), lumière
   naturelle de fin d'après-midi de préférence pour cohérence avec les autres
   visuels golden hour.
3. Si Abdou n'est pas disponible pour la séance mais que l'équipe accepte : possibilité
   de publier une photo de l'équipe (sans sur-titrer nommément une personne non
   présente sur la photo) en attendant.

### Option de secours conforme (si aucune photo d'équipe/Abdou n'est disponible à temps)
Plutôt qu'un visage généré par IA, utiliser en attendant un **visuel d'ambiance sans
personnage** (transats + table dressée + un cocktail servi, suggérant l'accueil sans
représenter faussement une personne) :

**Outil recommandé : Midjourney v6**
> Photoréaliste, table de restaurant de plage dressée avec soin, un cocktail maison
> fraîchement servi au premier plan, une chaise tirée en signe d'accueil, ambiance
> chaleureuse de fin d'après-midi, sable et transats visibles en arrière-plan flou,
> lumière dorée, ambiance conviviale et accueillante sans personnage visible, Petite
> Côte sénégalaise (Warang), pas de texte, pas de logo, format --ar {ratio}

- **1:1** → `--ar 1:1`
- **4:5** → `--ar 4:5`
- **9:16** → `--ar 9:16`
- **16:9** → `--ar 16:9`

À utiliser **uniquement en solution transitoire**, en remplaçant dès que possible
par la vraie photo d'Abdou/l'équipe une fois l'accord et le shooting obtenus — car
l'angle éditorial « accueil d'Abdou » perd une grande partie de sa force de
conviction sans visage humain réel.

**Texte dans le visuel** : aucun texte incrusté prévu (verbatims en légende de post
uniquement, cf. copy du Créateur). Si une future version « carte citation » avec le
verbatim de Roseline/Maria/Sonia incrusté est envisagée : même mise en garde qu'au
visuel 1 — texte court, Ideogram ou post-production manuelle, relecture obligatoire,
risque de déformation sinon.

---

## 5. Synthèse — priorité vraie photo vs IA, par visuel

| Visuel | Vraie photo dispo ? | Recours IA acceptable | Outil si IA | Risque texte illisible |
|---|---|---|---|---|
| 1. Coucher de soleil | À confirmer | Oui, en dépannage | Midjourney v6 (Imagen en repli) | Élevé si carte citation — éviter texte incrusté par l'IA |
| 2. Poisson frais | Facilement réalisable (shooting simple) | Oui, en dépannage seulement | Gemini Imagen / Midjourney v6 | Faible (pas de texte prévu) |
| 3. Reel golden hour | Obligatoire (tournage réel) | Non pour la vidéo entière, oui pour un plan isolé manquant hors plan Abdou | Midjourney v6 (plan isolé) | Élevé — 2 inserts texte + n° WhatsApp : jamais en génération IA, post-prod uniquement |
| 4. Accueil Abdou | Obligatoire — accord à confirmer, aucun substitut IA du visage d'Abdou | Non pour représenter Abdou/l'équipe ; oui pour un visuel d'ambiance sans personnage en transition | Midjourney v6 (ambiance sans personnage) | Faible sur ce visuel (pas de texte prévu) |

## 6. Rappels finaux avant production

- **Palette bleu mer / sable / terracotta = recommandation, non validée.** Ne pas
  figer une charte graphique dessus avant retour du client.
- **Menu, prix et événements** : aucun visuel ne doit afficher de prix ou de menu
  détaillé (cohérent avec le brief et les contenus).
- **Pas de foule** sur aucun visuel, y compris ceux générés par IA — cohérence avec
  le positionnement « loin de la foule ».
- **Sous-titres et légendes** de tous les formats vidéo à intégrer nativement en
  post-production, jamais via génération IA, en particulier pour tout ce qui
  contient le numéro **+221 77 754 90 89**.
