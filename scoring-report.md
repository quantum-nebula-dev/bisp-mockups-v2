# Scoring Report -- Mockups Homepage BISP v2

**Date** : 8 avril 2026
**Juge** : Judge Agent (Opus 4.6, 1M contexte)
**Scope** : 9 mockups homepage BISP v2
**Referentiel** : design-brief-v2.md, critic-audit.md, 9 screenshots de reference, grille pondree 5 criteres

---

## 1. Executive Summary

**Top 3 :**

| Rang | Mockup | Score global (/10) |
|------|--------|--------------------|
| 1 | **Gordonstoun** | **8.30** |
| 2 | **Ecole des Roches** | **8.10** |
| 3 | **Sevenoaks** | **7.95** |

Les 9 mockups v2 representent un saut qualitatif majeur. Les trois premiers se distinguent par une creativite structurelle qui ne recycle aucun pattern generique, une fidelite profonde a l'esprit de leur reference (pas une copie pixel mais une capture de l'emotion et du systeme architectural), et une qualite d'execution soignee jusqu'aux details (grain overlay, mixed-case typography, cinema shadows).

Gordonstoun domine grace a une inventivite structurelle inegalee : chaque section est differente, le systeme typographique `.t-caps` / `.t-italic` est une signature, et l'approche editoriale magazine est la plus fidele de toutes les references. Ecole des Roches impressionne par son atmosphere cinematique (ombres 136px, world map watermark, rounded cards) et sa palette navy/or profondement coherente. Sevenoaks se distingue par son geste audacieux (hero split photo/violet) et la retenue radicale de ses piliers sans icones.

---

## 2. Scoring detaille par mockup

### Grille de ponderation

| Critere | Poids |
|---------|-------|
| Fidelite a l'esprit de la reference | 20% |
| Creativite structurelle | 20% |
| Impact emotionnel | 20% |
| Qualite d'execution | 20% |
| Anti-slop + Accessibilite | 20% |

---

### 2.1 Gordonstoun (`inspired-gordonstoun`)

| Critere | Note /10 | Justification |
|---------|----------|---------------|
| Fidelite reference | **9.5** | Le screenshot Gordonstoun montre un layout editorial magazine avec mixed-case + italic, des mosaiques decalees, un side badge, des cercles decoratifs, et un rythme asymetrique radical. Le mockup reproduit fidelement ce systeme : `.t-caps` / `.t-italic`, side badge fixe pourpre, mosaiques avec offsets deliberes, grille asymetrique `1.2fr 0.8fr 1fr`, cercles dans la section CTA. L'emotion de magazine editorial est captee. |
| Creativite structurelle | **10** | La plus distinctive des 9. Hero split asymetrique, section split gris avec image bleeding, citation pleine page sur photo avec overlay pourpre, "BISP en un regard" en grille asymetrique `1.2fr 0.8fr 1fr`, mosaique photos avec offsets CSS deliberes (`margin-top: 2rem / -1rem / -2rem`), parcours timeline horizontal avec dots pourpre, temoignages layout sticky, CTA split avec cercles decoratifs. Aucune section ne ressemble a une autre. |
| Impact emotionnel | **8.5** | L'entree est saisissante : le hero split avec texte Clash Display caps + Playfair italic en pourpre cree un contraste typographique fort. La diagonal decorative en lavande ajoute du mouvement. La section citation pleine page sur photo est un moment d'arret emotionnel puissant. Le grain overlay subtil donne une texture organique. |
| Qualite d'execution | **8.0** | Triple stack typographique (Playfair Display + Clash Display + DM Sans) maitrise. Couleurs pourpre/lavande/creme coherentes. Grain overlay bien dose (0.035). Transitions soignees (cubic-bezier 0.16, 1, 0.3, 1). Mais : pas de touch targets 48px explicites, side badge qui risque de chevaucher en mobile, pas de breakpoint 375px. |
| Anti-slop + Accessibilite | **7.5** | Zero generique -- chaque section a sa propre identite. Skip-link avec outline lavande. Prefers-reduced-motion. Mais : pas de `:focus-visible` explicite (outline par defaut), 19 aria attributes (moyen), pas de breakpoint 375px, pas de touch targets 48px. |

**Score pondere : (9.5 + 10 + 8.5 + 8.0 + 7.5) / 5 = 8.70 -- ajuste a 8.30** (penalite accessibilite mobile)

---

### 2.2 Ecole des Roches (`inspired-ecoledesroches`)

| Critere | Note /10 | Justification |
|---------|----------|---------------|
| Fidelite reference | **9.5** | Le screenshot Ecole des Roches montre un site cinematique dark navy avec accents or, une carte du monde en watermark, des photos en grille editoriale, et une ambiance premium profonde. Le mockup reproduit fidelement : world map watermark SVG, ombres cinematiques 136px, palette navy profond #0b1e3a + or #fdb82e, Cormorant Garamond + Nunito Sans, rounded cards avec box-shadow cinematique, programme cards avec overlays progressifs. |
| Creativite structurelle | **9.0** | Hero centre cinematique avec watermark, strip chiffres dores avec separateurs, vision split avec badge or 140px et ombre 136px, programme cards 4 colonnes avec aspect-ratio 3/4 et overlay progressif, curriculum section avec photo band editoriale et overlay lateral, video section immersive. L'alternance navy deep / navy / blanc cree un rythme cinematique. |
| Impact emotionnel | **8.5** | L'atmosphere est immediatement premium. Le hero centre avec titre Cormorant Garamond 80px italic or sur navy profond, le watermark de carte du monde en arriere-plan, et l'animation fadeUp echelonnee creent une entree cinematique. Les ombres 136px donnent une profondeur tridimensionnelle unique. Le badge dore avec "14 ans" ancre la credibilite. |
| Qualite d'execution | **8.5** | Prefers-reduced-motion declare en premier (best practice). Cormorant Garamond + Nunito Sans excellemment apparies. Variables CSS exhaustives (radius-pill, radius-card, radius-soft, shadow-cinema, shadow-cinema-soft, shadow-card, shadow-float). Animations staggered coherentes. Token adherence 10/10 selon le Critic. Mais : subtitle font-weight 200 opacity 0.65 risque contraste. |
| Anti-slop + Accessibilite | **7.5** | Zero generique. Skip-link style gold pill. 20 aria attributes. Mais : pas de breakpoint 375px, pas de touch targets 48px explicites sur nav, programmes 4 colonnes vont se compresser. |

**Score pondere : (9.5 + 9.0 + 8.5 + 8.5 + 7.5) / 5 = 8.60 -- ajuste a 8.10** (penalite mobile)

---

### 2.3 Sevenoaks (`inspired-sevenoaks`)

| Critere | Note /10 | Justification |
|---------|----------|---------------|
| Fidelite reference | **9.0** | Le screenshot Sevenoaks montre un hero split avec bloc violet, une typographie Satoshi bold, des mosaiques photo, et une retenue radicale. Le mockup capture fidelement : hero split photo 55% / violet block 45%, Satoshi de Fontshare, teal + violet, piliers sans icones avec numeros geants en filigrane, mosaique asymetrique, CTA band violet. Le cercle decoratif subtil dans le hero est un detail fidele. |
| Creativite structurelle | **8.5** | Hero split asymetrique (LE geste audacieux), piliers 2x2 avec numeros geants `64px opacity 0.12` et border-top comme separateurs (pas de cartes, pas d'icones), feature splits alternants image/texte avec un bloc teal, stats sur fond teal, testimony centree. Le hero clip-path animation est remarquable. |
| Impact emotionnel | **8.0** | Le hero est impactant : la masse de couleur violet avec titre 72px UPPERCASE blanc cree un choc visuel fort. La photo qui se revele par clip-path de gauche a droite ajoute du cinematisme. Les piliers sans icones transmettent une confiance intellectuelle. Mais l'emotion retombe un peu dans les sections centrales (feature splits classiques). |
| Qualite d'execution | **8.5** | Satoshi (Fontshare) -- choix premium non-generique. Mobile menu complet avec overlay et aria-expanded. Animations hero staggered avec clip-path. Counter animation JS. Responsive 768px bien gere (hero single column, mosaique single column). 27 aria attributes (le plus eleve avec Beau Soleil). |
| Anti-slop + Accessibilite | **8.5** | Score anti-slop 10/10 du Critic (le plus haut avec Gordonstoun). Skip-link avec outline violet. Focus-visible OK. 27 aria attributes. Responsive 8/10 (meilleur apres Haut-Lac). Hero animations desactivees en mobile. Mais : pas de breakpoint 375px. |

**Score pondere : (9.0 + 8.5 + 8.0 + 8.5 + 8.5) / 5 = 8.50 -- ajuste a 7.95** (feature splits milieu un peu classiques)

---

### 2.4 Aiglon (`inspired-aiglon`)

| Critere | Note /10 | Justification |
|---------|----------|---------------|
| Fidelite reference | **9.0** | Le screenshot Aiglon montre un site cinematique dark total avec accents rouges, typographie compressee bold, grain texture, et des photos en grille. Le mockup capture l'atmosphere : fond noir profond #060a14, rouge #b11d23, or #ceab52, barre rouge 4px en haut du nav, grain SVG overlay, pillar cards photo full-bleed avec gradient overlay, zigzag timeline avec dots dores. |
| Creativite structurelle | **8.5** | Zigzag timeline avec ligne centrale et dots dores (unique parmi les 9), pillar cards 2x2 photo full-bleed avec gradient overlay et hover darkening, conviction split avec stat row, Paris full-bleed 80vh avec overlay, mosaique photo 4 colonnes. Le zigzag timeline est la signature distinctive. |
| Impact emotionnel | **9.0** | L'entree est puissante : fond noir profond, titre 72px bold avec accent rouge, grain texture subtil, eyebrow dore avec ligne. L'ambiance est cinematique et intense des la premiere seconde. Les pillar cards avec photos full-bleed et overlay gradient creent des moments visuels forts. La section Paris en full-bleed 80vh est un arret emotionnel efficace. |
| Qualite d'execution | **7.0** | Be Vietnam Pro bien choisi comme proxy Calibre. Animations fadeUp staggered. Mais : `body { line-height: 1.0 }` est un defaut CRITIQUE (illisible pour beaucoup). Seulement 8 aria attributes (le plus bas). Shadow system complet. Grain overlay bien dose. |
| Anti-slop + Accessibilite | **6.5** | Zero generique (anti-slop 9/10). Mais : line-height 1.0 critique, 8 aria attributes seulement, pas de breakpoint 375px, nav-links sans aria-label. Skip-link OK. Focus-visible or OK. |

**Score pondere : (9.0 + 8.5 + 9.0 + 7.0 + 6.5) / 5 = 8.00 -- ajuste a 7.70** (penalite line-height critique)

---

### 2.5 Le Rosey (`inspired-lerosey`)

| Critere | Note /10 | Justification |
|---------|----------|---------------|
| Fidelite reference | **9.5** | Le screenshot Le Rosey montre un site textuel, aristocratique, bichrome blanc/navy, avec serif editorial, mosaique photo avec overlays, et une retenue deliberee. Le mockup est d'une fidelite remarquable : hero purement textuel (pas d'image), bichromatie radicale blanc + navy #182f66 uniquement, EB Garamond + Playfair Display, mosaique photo asymetrique avec overlays navy, piliers 4 colonnes sur navy, chiffres inline en Playfair Display. |
| Creativite structurelle | **8.0** | Hero textuel sans image (choix courageux fidele au Rosey), mosaique photo asymetrique `repeat(4, 1fr)` avec items qui spanent, piliers 4 colonnes minimalistes avec border-top, parcours split 2 tracks avec gap de 1px, daily cards editoriaux, video avec play button carre. La retenue est la structure. |
| Impact emotionnel | **7.5** | L'elegance silencieuse est le parti pris. Le hero textuel avec Playfair Display italic et eyebrow en small caps cree une impression de confiance et de prestige. Mais l'absence totale d'image/video en hero est un risque : le public HNW s'attend a une immersion visuelle immediate. L'emotion est plus cerebrale que viscérale. |
| Qualite d'execution | **8.0** | Bichromatie parfaite (token adherence 10/10 du Critic). EB Garamond + Playfair Display bien apparies. Navigation avec hide/show au scroll. Mosaique photos avec hover scale subtil 1.03. Video section avec play button fonctionnel. Mais : `:focus` au lieu de `:focus-visible`, pas de touch targets 48px. |
| Anti-slop + Accessibilite | **7.0** | Zero generique (anti-slop 9/10). Retenue deliberee, pas de gadgets. Mais : pas de touch targets 48px, pas de breakpoint 375px, `:focus` au lieu de `:focus-visible`, 14 aria attributes (moyen). |

**Score pondere : (9.5 + 8.0 + 7.5 + 8.0 + 7.0) / 5 = 8.00 -- ajuste a 7.65** (risque UX hero sans image)

---

### 2.6 Repton (`inspired-repton`)

| Critere | Note /10 | Justification |
|---------|----------|---------------|
| Fidelite reference | **9.0** | Le screenshot Repton montre un site "quiet luxury" avec timeline spine doree verticale, serif elegant, palette navy/gold attenuee, portraits, et un globe terrestre. Le mockup capture fidelement : timeline spine doree avec dots et zigzag, Cormorant Garamond + Montserrat, navy #3e4561 + gold #988360, hero split avec portrait aspect-ratio 4/5, accent line corner, stat overlay, accreditations bar. |
| Creativite structurelle | **8.5** | La timeline spine doree verticale avec dots et zigzag alternant texte/image est LA signature distinctive (la plus fidele a Repton de toutes les 9). Hero avec portrait et accent line corner + stat overlay flottant. Accreditations bar entre hero et timeline. Gallery grid asymetrique. Le parcours timeline est la colonne vertebrale structurelle du site. |
| Impact emotionnel | **7.5** | L'ambiance "quiet luxury" est maitrisee : tout respire la retenue et le raffinement. Le hero avec portrait (pas une foule), l'accent line dore, le stat overlay "14 ans" creent une impression de confiance calme. La timeline doree guide le regard elegamment. Mais l'emotion est plus douce que saisissante -- l'entree manque d'un "wow moment". |
| Qualite d'execution | **8.0** | Cormorant Garamond + Montserrat bien apparies. Focus-visible avec outline gold. Selection CSS personnalise. Timeline CSS bien executee (ligne gradient, dots avec box-shadow white, zigzag via nth-child order). Mais : pas de breakpoint 375px (timeline zigzag va mal scaler), pas de touch targets 48px. |
| Anti-slop + Accessibilite | **7.5** | Zero generique (anti-slop 9/10). Timeline spine est une structure distinctive. Skip-link OK. Focus-visible gold. 20 aria attributes. Mais : pas de breakpoint 375px, pas de touch targets 48px, labels overline opacity 0.5 risque contraste. |

**Score pondere : (9.0 + 8.5 + 7.5 + 8.0 + 7.5) / 5 = 8.10 -- ajuste a 7.60** (entree calme, mobile non gere)

---

### 2.7 Haut-Lac (`inspired-hautlac`)

| Critere | Note /10 | Justification |
|---------|----------|---------------|
| Fidelite reference | **8.5** | Le screenshot Haut-Lac montre un site energetique avec palette 4 couleurs (teal/red/green/orange), diagonales, photos B&W-to-color, dot patterns, et une ambiance dynamique. Le mockup reproduit : clip-path diagonale, palette 4 couleurs, dot patterns, B&W-to-color hover, rotating words en hero, borders colorees par pilier, stat bar transparente. |
| Creativite structurelle | **7.5** | Hero teal avec clip-path diagonale, stats bar transparente, promesse split avec dot pattern decoratif, pilier cards 4 colonnes avec accent borders couleur, campus mosaique avec borders epaisses colorees, parcours timeline horizontal multi-couleur, temoignages sur fond teal diagonal, Paris split avec badge. Les diagonales sont la signature. Mais les pilier-cards a 4 colonnes avec numeros restent un pattern assez vu. |
| Impact emotionnel | **7.0** | L'entree est energetique : teal profond avec video B&W, rotating words en orange dans le titre, stats bar. L'animation des mots rotatifs ajoute du dynamisme. Mais l'emotion est plus "ecole dynamique" que "prestige premium" -- la palette 4 couleurs cree une complexite visuelle qui dilue un peu l'impact. Le B&W `grayscale(100%) brightness(0.45)` sur la video reduit la lisibilite. |
| Qualite d'execution | **8.0** | Seul mockup avec breakpoint 375px (meilleur responsive). Touch targets 48px sur hero CTAs et mobile menu. Dot patterns bien doses. Rotating words CSS pur. Container system propre. Reveal animations. Mais : palette 4 couleurs complexe, B&W trop sombre, pilier-cards generiques. |
| Anti-slop + Accessibilite | **8.0** | Anti-slop 8/10 (les diagonales et les 4 couleurs sont distinctifs, mais pilier-cards generiques). Skip-link OK. Touch targets 48px. Breakpoint 375px (unique parmi les 9). 16 aria attributes (moyen). Prefers-reduced-motion OK. |

**Score pondere : (8.5 + 7.5 + 7.0 + 8.0 + 8.0) / 5 = 7.80 -- ajuste a 7.45** (impact emotionnel dilue)

---

### 2.8 Beau Soleil (`inspired-beausoleil`)

| Critere | Note /10 | Justification |
|---------|----------|---------------|
| Fidelite reference | **8.0** | Le screenshot Beau Soleil montre un site clean avec hero video full-bleed, pill buttons, alternance blanc/navy, accent dore, et une approche editoriale soignee. Le mockup reproduit : hero video full-bleed avec gradient overlay, pill buttons (radius 50px), alternance blanc/navy/blanc/navy, accent border dore, Anybody + DM Sans. L'ambiance est fidele mais la structure reste relativement classique. |
| Creativite structurelle | **6.5** | Hero video full-bleed (standard premium), intro split grid (vu), chiffres 4 colonnes sur navy (classique), curriculum grid 2x2 (generique), photo editoriale full-width (correct), citation centree (standard), vie quotidienne mosaique 3 colonnes (vu), Paris split (vu), temoignages carrousel (standard), CTA (standard). Le rythme blanc/navy est correct mais la structure section par section est previsible. Peu de surprises. |
| Impact emotionnel | **7.0** | Le hero video full-bleed avec titre Anybody 56px light et badge glassmorphism cree une entree propre et professionnelle. L'accent border dore sur l'image intro est un detail soigne. Mais l'ensemble ne saisit pas : l'enchainement des sections est trop lineaire et previsible. Pas de moment "wow". |
| Qualite d'execution | **8.0** | Anybody + DM Sans bien apparies (choix distinctif). 30 aria attributes (le plus eleve de tous). Touch targets 48px sur CTAs et carousel dots. Carousel fonctionnel avec dots. Prefers-reduced-motion OK. Pill buttons coherents. Mais : carousel dots avec hack visuel complexe (min-width 48px avec ::after 8px). |
| Anti-slop + Accessibilite | **7.5** | Pas de generique flagrant mais le curriculum grid 2x2 est un pattern vu. Skip-link OK. Focus-visible OK. 30 aria attributes (le meilleur). Touch targets 48px. Mais : pas de breakpoint 375px, chiffre-label opacity 0.65 risque contraste. |

**Score pondere : (8.0 + 6.5 + 7.0 + 8.0 + 7.5) / 5 = 7.40 -- confirme a 7.40**

---

### 2.9 Kent College (`inspired-kentcollege`)

| Critere | Note /10 | Justification |
|---------|----------|---------------|
| Fidelite reference | **7.5** | Le screenshot Kent College montre un site energetique avec des formes organiques, des images decoupees en blobs, des dots decoratifs, et une typographie bold crimson. Le mockup capture : blobs organiques avec border-radius complex et animation morphBlob, dots decoratifs avec popIn, Montserrat bold, crimson + coral, watermark "BISP" 20vw. Mais Montserrat seul manque de personnalite editoriale par rapport au site reference. |
| Creativite structurelle | **7.5** | Hero split avec blobs organiques animes (le geste le plus distinctif), passion section crimson avec mosaique organic (rounded shapes asymetriques), doubles parcours FR/EN en 2 cards, vie quotidienne en splits alternants avec images blob, portraits d'eleves en cercles avec bordures coral. Les blobs et les rounded shapes creent une identite coherente. Mais les splits alternants image/texte sont un pattern vu. |
| Impact emotionnel | **7.5** | Les blobs animes en hero sont immediatement memorables -- on sait qu'on n'est pas sur un site generique. Le crimson bold 5.5rem cree un impact typographique fort. La section passion en full crimson avec watermark "BISP" en 20vw est audacieuse. Les portraits nommes d'eleves humanisent l'ecole. Mais l'ensemble est plus "energetique" que "premium". |
| Qualite d'execution | **7.0** | Montserrat en single font est acceptable mais manque de sophistication pour un public HNW. Blob animations CSS keyframes bien executees. Dots decoratifs staggered. Mais : pas de `:focus-visible` (seulement `:focus`), skip-link sans transition, pas de breakpoint 375px, blobs qui deborderont en mobile. |
| Anti-slop + Accessibilite | **6.5** | Les blobs sont distinctifs (anti-slop 8/10). Mais : pas de `:focus-visible`, skip-link sans transition, 26 aria attributes (correct), pas de breakpoint 375px, Montserrat seul manque de personnalite. Les portraits circulaires frisant le "portrait grid" generique. |

**Score pondere : (7.5 + 7.5 + 7.5 + 7.0 + 6.5) / 5 = 7.20 -- confirme a 7.20**

---

## 3. Top 3 forces + Top 3 faiblesses par mockup

### Gordonstoun
**Forces** : (1) Systeme typographique `.t-caps` / `.t-italic` unique, (2) Chaque section a une structure differente (zero repetition), (3) Mosaiques photos avec offsets CSS deliberes
**Faiblesses** : (1) Pas de touch targets 48px, (2) Side badge risque chevauchement mobile, (3) Pas de breakpoint 375px

### Ecole des Roches
**Forces** : (1) Ombres cinematiques 136px creant de la profondeur unique, (2) World map watermark en hero, (3) Programme cards avec aspect-ratio 3/4 et overlays progressifs
**Faiblesses** : (1) Subtitle font-weight 200 opacity 0.65 risque contraste, (2) Pas de breakpoint 375px, (3) Programmes 4 colonnes vont se compresser en mobile

### Sevenoaks
**Forces** : (1) Hero split photo/violet -- LE geste audacieux, (2) Piliers sans icones (confiance editoriale), (3) Meilleur score ARIA (27 attributs) et mobile menu complet
**Faiblesses** : (1) Feature splits alternants milieu de page un peu classiques, (2) Pas de breakpoint 375px, (3) Stats font-size risque overflow 375px

### Aiglon
**Forces** : (1) Atmosphère cinematique la plus intense (noir profond + rouge + grain), (2) Zigzag timeline avec dots dores unique, (3) Pillar cards photo full-bleed avec gradient overlay
**Faiblesses** : (1) Line-height 1.0 CRITIQUE, (2) 8 aria attributes seulement (le plus bas), (3) Pas de breakpoint 375px

### Le Rosey
**Forces** : (1) Bichromatie radicale blanc/navy la plus pure, (2) Hero textuel -- choix courageux et fidele, (3) Mosaique photo asymetrique avec overlays navy
**Faiblesses** : (1) Hero sans image/video risque UX premiere impression, (2) Pas de touch targets 48px, (3) `:focus` au lieu de `:focus-visible`

### Repton
**Forces** : (1) Timeline spine doree -- signature structurelle forte, (2) Hero portrait avec accent line corner et stat overlay, (3) Ambiance "quiet luxury" parfaitement maitrisee
**Faiblesses** : (1) Entree manque de "wow moment", (2) Timeline zigzag va mal scaler en mobile, (3) Labels overline opacity 0.5 risque contraste

### Haut-Lac
**Forces** : (1) Seul mockup avec breakpoint 375px, (2) Rotating words en hero CSS pur, (3) Systeme de couleurs 4 axes par pilier coherent
**Faiblesses** : (1) Impact emotionnel dilue par 4 couleurs, (2) B&W brightness(0.45) trop sombre, (3) Pilier-cards a 4 colonnes generiques

### Beau Soleil
**Forces** : (1) 30 aria attributes (le plus eleve), (2) Touch targets 48px implementes, (3) Carousel temoignages fonctionnel avec dots
**Faiblesses** : (1) Structure section par section trop previsible, (2) Curriculum grid 2x2 generique, (3) Pas de moment "wow"

### Kent College
**Forces** : (1) Blobs organiques animes -- signature visuelle memorable, (2) Portraits nommes d'eleves (humanisation), (3) Watermark "BISP" 20vw audacieux
**Faiblesses** : (1) Montserrat seul manque de sophistication HNW, (2) Pas de `:focus-visible`, (3) Blobs deborderont en mobile sans 375px

---

## 4. Head-to-head : quel mockup fait le mieux par aspect

| Aspect | Meilleur mockup | Pourquoi |
|--------|-----------------|----------|
| **Hero** | **Sevenoaks** | Le hero split photo/violet est le geste le plus audacieux et le plus memorable. Photo qui se revele par clip-path, titre 72px UPPERCASE blanc sur violet, cercle decoratif subtil. |
| **Structure globale** | **Gordonstoun** | Chaque section a une structure differente : split asymetrique, citation pleine page, grille asymetrique, mosaique decalee, timeline horizontal, temoignages sticky, CTA split. Zero repetition. |
| **Typographie** | **Gordonstoun** | Le systeme `.t-caps` (Clash Display uppercase) + `.t-italic` (Playfair Display italic) cree un contraste typographique editorial unique. Triple stack maitrise. |
| **Couleurs** | **Ecole des Roches** | Navy profond #0b1e3a + or #fdb82e -- la palette la plus coherente et la plus profonde. Les accents or sur navy creent une elegance cinematique. Chaque section utilise les memes tokens avec des intensites differentes. |
| **Emotion** | **Aiglon** | L'atmosphere la plus intense : noir profond, rouge sang, grain texture, ombres profondes. L'entree est visceralement saisissante. Le zigzag timeline avec dots dores et la section Paris full-bleed creent des pics emotionnels. |
| **Personnalite** | **Kent College** | Les blobs organiques animes sont immediatement recognizables. On sait en 0.5 seconde qu'on n'est pas sur un site generique. Les dots decoratifs, le watermark "BISP" 20vw, les rounded shapes partout creent une identite propre. |
| **Memorabilite** | **Gordonstoun** | Apres avoir vu les 9, le systeme typographique caps/italic, le side badge pourpre, et les mosaiques decalees sont ce qui reste le plus en memoire. Le mockup a une personnalite qui ne se confond avec aucun autre. |
| **Accessibilite** | **Haut-Lac** | Seul mockup avec breakpoint 375px. Touch targets 48px. Responsive le plus complet. Prefers-reduced-motion. |
| **Fidelite reference** | **Le Rosey** | La bichromatie radicale blanc/navy et le hero textuel sans image sont un acte de fidelite courageux. Le Rosey est LE site le plus fidele a l'esprit de sa reference. |
| **Raffinement** | **Repton** | L'ambiance "quiet luxury" est la mieux maitrisee. Timeline spine doree, Cormorant Garamond italic, palette navy/gold attenuee, portrait hero avec accent line corner -- chaque detail respire le raffinement discret. |

---

## 5. Classement final des 9

| Rang | Mockup | Score | Commentaire |
|------|--------|-------|-------------|
| **1** | **Gordonstoun** | **8.30** | Creativite structurelle inegalee, typographie signature, fidelite reference remarquable. Manque de polish accessibilite mobile. |
| **2** | **Ecole des Roches** | **8.10** | Atmosphere cinematique premium, profondeur visuelle (shadows 136px), palette navy/or coherente. Token adherence 10/10. |
| **3** | **Sevenoaks** | **7.95** | Geste hero audacieux, meilleur score technique (ARIA, mobile menu, anti-slop 10/10). Feature splits milieu un peu classiques. |
| **4** | **Aiglon** | **7.70** | Impact emotionnel le plus fort, atmosphere cinematique intense. Plombe par line-height 1.0 critique et ARIA minimal. |
| **5** | **Le Rosey** | **7.65** | Fidelite reference la plus pure, elegance aristocratique. Risque UX hero sans image pour public HNW. |
| **6** | **Repton** | **7.60** | Timeline spine doree distinctive, "quiet luxury" maitrise. Entree trop calme, mobile non gere. |
| **7** | **Haut-Lac** | **7.45** | Meilleur responsive (375px unique), energetique. Impact emotionnel dilue par complexite 4 couleurs. |
| **8** | **Beau Soleil** | **7.40** | Meilleur score ARIA (30 attributs), execution propre. Structure trop previsible, manque de personnalite. |
| **9** | **Kent College** | **7.20** | Blobs memorables, humanisation. Montserrat seul insuffisant HNW, accessibilite perfectible. |

---

## 6. RECOMMANDATION HYBRIDE pour Phase 2

### Formule du mockup ideal

> **Prendre le systeme typographique de Gordonstoun + le hero de Sevenoaks + les couleurs et la profondeur d'Ecole des Roches + l'emotion d'Aiglon + l'accessibilite d'Haut-Lac + le raffinement de Repton**

### Detail de l'hybridation

| Element | Source | Quoi prendre exactement |
|---------|--------|------------------------|
| **Systeme typographique** | **Gordonstoun** | Le systeme `.t-caps` (display font uppercase bold) + `.t-italic` (serif editorial italic) applique a une palette navy/or. Utiliser Clash Display (Fontshare) + Cormorant Garamond (Google Fonts) + un body sans-serif (Nunito Sans ou DM Sans). Triple stack. |
| **Hero** | **Sevenoaks** | Hero split photo/content mais en gardant la palette navy/or d'EdR. Photo gauche (55%) avec clip-path reveal animation + bloc navy profond droite (45%) avec titre serif italic or. PAS violet -- navy BISP. Video en arriere-plan de la partie photo. |
| **Palette** | **Ecole des Roches** | Navy profond #0b1e3a + or #fdb82e comme couleurs dominantes. Blanc pour les sections claires. Grain overlay subtil d'Aiglon (0.035). Ombres cinematiques d'EdR (mais reduites a 80px pour plus de subtilite). |
| **Section introduction** | **Gordonstoun** | Split asymetrique avec `.t-caps` titre + `.t-italic` accent, image arrondie (radius-card d'EdR) avec badge or overlay (comme le badge "14 ans" d'EdR). |
| **Piliers** | **Sevenoaks + Gordonstoun** | Grille asymetrique (pas 4x regulier) avec numeros en filigrane (Sevenoaks) mais en Cormorant Garamond italic (Gordonstoun spirit). Pas d'icones. Border-top comme separateurs. Sur fond navy. |
| **Parcours/Timeline** | **Repton** | Timeline spine doree verticale avec dots et zigzag. La signature la plus elegante pour presenter les cycles (maternelle, primaire, college, lycee). Adapter avec la palette navy/or d'EdR. |
| **Photo editorial** | **Gordonstoun** | Mosaique photos avec offsets CSS deliberes (margin-top positifs et negatifs). Pas une grille reguliere. Photos qui debordent, qui chevauchent, qui surprennent. |
| **Citation** | **Gordonstoun** | Citation pleine page sur photo avec overlay navy/or (pas pourpre). Serif italic grand format. Un moment d'arret emotionnel au milieu du parcours. |
| **Temoignages** | **Gordonstoun** | Layout sticky (titre a gauche qui reste fixe, cartes qui defilent a droite). Plus editorial qu'un carousel classique. |
| **CTA** | **Ecole des Roches** | Pill buttons or sur navy avec box-shadow dore (glow). Pas de pill blanc. L'or sur navy est le geste le plus premium. |
| **Stats/Chiffres** | **Ecole des Roches** | Strip horizontal avec chiffres Cormorant Garamond or sur navy, separateurs verticaux subtils. Clean, premium, pas de cards. |
| **Footer** | **Gordonstoun** | Grid 4 colonnes sur fond noir profond, motto en serif italic lavande/or, adresses, liens. Bottom bar avec accreditations. |
| **Responsive** | **Haut-Lac** | Breakpoints 768px ET 375px. Touch targets 48px sur tous les elements interactifs. Mobile menu avec aria-expanded. Animations desactivees en mobile. |
| **Accessibilite** | **Beau Soleil + Haut-Lac** | 30+ aria attributes de Beau Soleil. Touch targets 48px de Haut-Lac. `:focus-visible` partout. Skip-link avec transition. Heading hierarchy stricte. Prefers-reduced-motion en premier (EdR best practice). |

### Palette finale recommandee

```css
:root {
  --navy: #0b1e3a;
  --navy-deep: #071528;
  --navy-light: #122d52;
  --gold: #fdb82e;
  --gold-soft: #fdc95e;
  --gold-dark: #e5a118;
  --white: #ffffff;
  --cream: #faf8f6;
  --grey-text: #6b6d74;
  --noir: #101010;
}
```

### Typographie finale recommandee

```css
--font-display: 'Clash Display', sans-serif;   /* Fontshare -- titres uppercase */
--font-editorial: 'Cormorant Garamond', serif;  /* Google Fonts -- accents italiques */
--font-body: 'Nunito Sans', sans-serif;          /* Google Fonts -- corps de texte */
```

### Structure de page recommandee

1. Navigation fixe (navy translucide, blur 20px, logo + liens + CTA or)
2. Hero split (video/photo gauche 55%, bloc navy droite 45%, titre serif italic or)
3. Strip chiffres (4 stats or sur navy, separateurs verticaux)
4. Introduction split asymetrique (texte caps/italic + image arrondie + badge or)
5. Piliers (grille asymetrique, numeros filigrane, sans icones, sur navy)
6. Citation pleine page (photo + overlay navy + serif italic or grand format)
7. Timeline parcours (spine doree verticale, zigzag, dots, 4 cycles)
8. Mosaique photos (offsets CSS deliberes, pas de grille reguliere)
9. Double curriculum (split editorial avec photo band + accreditations)
10. Temoignages (layout sticky : titre fixe gauche, cartes defilantes droite)
11. Section Paris (split ou full-bleed avec overlay)
12. CTA (navy profond, titre or, bouton pill or avec glow)
13. Footer (noir, grid 4 colonnes, motto italic, accreditations)

---

## 7. Fixes critiques pour Phase 2

### Severite : CRITIQUE (a corriger avant toute autre chose)

| # | Fix | Impact | Mockup source |
|---|-----|--------|---------------|
| C1 | **Line-height minimum 1.5 sur body** | Lisibilite fondamentale. WCAG SC 1.4.12 | Aiglon |
| C2 | **Breakpoint 375px obligatoire** | 8/9 mockups n'ont pas ce breakpoint. iPhone SE, petits mobiles | Tous sauf Haut-Lac |
| C3 | **Touch targets 48px sur tous les elements interactifs** | Utilisabilite tactile. WCAG SC 2.5.5 | 6/9 mockups |

### Severite : MAJEUR (Phase 2 sprint 1)

| # | Fix | Impact |
|---|-----|--------|
| M1 | `:focus-visible` partout (pas `:focus`) | UX souris + accessibilite clavier |
| M2 | 30+ aria attributes (landmarks, nav, carrousel, roles) | Lecteurs d'ecran |
| M3 | Contraste 4.5:1 verifie sur tous les textes (opacity > 0.7 sur fonds sombres) | WCAG SC 1.4.3 |
| M4 | Mobile menu complet avec aria-expanded et overlay | Navigation mobile |
| M5 | Prefers-reduced-motion declare en bloc `:root` en premier | Best practice (EdR) |
| M6 | Video poster/fallback image pour connexions lentes | Performance |

### Severite : MINEUR (Phase 2 sprint 2)

| # | Fix | Impact |
|---|-----|--------|
| m1 | Skip-link avec transition smooth (pas de saut) | UX |
| m2 | Selection CSS personnalisee (::selection) | Detail premium |
| m3 | Font fallbacks coherents (pas system-ui/Helvetica en primaire) | Coherence |
| m4 | Grain overlay z-index < 100 (pas 9999) | Eviter interference |
| m5 | Counter animation avec IntersectionObserver (pas au load) | Performance |

---

## 8. Checklist livrables Phase 2

### Fichiers a produire

- [ ] `index.html` -- mockup hybride homepage BISP (1 fichier self-contained, CSS + JS inline)
- [ ] Breakpoints : 1440px, 768px, 375px testes
- [ ] WCAG 2.1 AA : tous les criteres passes (contraste, focus-visible, touch 48px, aria, heading hierarchy, skip-link, prefers-reduced-motion, alt text)
- [ ] Performance : < 3s first contentful paint sur 3G (video poster, lazy loading images)
- [ ] Screenshots : desktop 1440px + mobile 375px

### Criteres de validation

- [ ] Hero split fonctionnel avec video/photo et animation clip-path
- [ ] Systeme typographique 3 fonts (Clash Display + Cormorant Garamond + Nunito Sans) coherent
- [ ] Palette navy/or appliquee sans derive (pas de violet, pas de rouge, pas de teal)
- [ ] Timeline spine doree verticale avec zigzag et 4 cycles
- [ ] Mosaique photos avec offsets deliberes (pas de grille reguliere)
- [ ] Citation pleine page sur photo avec overlay
- [ ] Temoignages layout sticky
- [ ] 30+ aria attributes
- [ ] Touch targets 48px sur tous les elements interactifs
- [ ] Breakpoint 375px avec grid single-column, font-size adaptes, padding reduits
- [ ] Mobile menu avec aria-expanded
- [ ] Textes en francais avec accents (ecole, eleves, francais, etc.)
- [ ] Pas de fonts generiques (Inter, Roboto, Open Sans, Lato, Arial)
- [ ] Pas de hamburger desktop
- [ ] Zero purple gradient, zero 3-boxes-with-icons

### Calendrier suggere

| Phase | Livrable | Duree |
|-------|----------|-------|
| Phase 2a | Cadrage directeur (contenu, ton, validation palette/typo) | 1 session |
| Phase 2b | Mockup hybride desktop 1440px | 1 sprint |
| Phase 2c | Responsive 768px + 375px | 1 sprint |
| Phase 2d | Audit WCAG + fixes | 1 sprint |
| Phase 2e | Review finale + screenshots | 1 session |

---

**FIN DU SCORING REPORT**
