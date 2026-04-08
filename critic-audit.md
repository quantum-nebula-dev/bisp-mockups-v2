# Audit Critique — Mockups BISP v2

**Date** : 7 avril 2026
**Auditeur** : Critic Agent (Opus 4.6)
**Scope** : 9 mockups homepage BISP v2
**Referentiel** : WCAG 2.1 AA, design-brief-v2.md, tokens Dembrandt par site

---

## Executive Summary

Les 9 mockups v2 representent un saut qualitatif significatif. Chaque designer a produit une identite visuelle distincte, ancree sur les tokens Dembrandt de sa reference. Les problemes systematiques de la v1 (polices generiques, absence de skip-link, layouts cookie-cutter) sont largement resolus. Les points forts sont la diversite structurelle, la qualite typographique, et l'utilisation coherente des assets BISP.

**Points forts collectifs** :
- 9/9 ont un skip-link fonctionnel
- 9/9 utilisent des polices non-generiques (aucun Inter/Roboto/Arial en font primaire)
- 9/9 ont une responsive media query (768px minimum)
- 9/9 utilisent IntersectionObserver pour les scroll reveals
- 9/9 incluent le logo BISP et la video de presentation
- 9/9 ont du contenu en francais avec accents
- 9/9 implementent prefers-reduced-motion

**Points faibles collectifs** :
- Touch target 48px : seulement 3/9 mockups ont des touch targets explicites a 48px pour les boutons interactifs (Beau Soleil, Aiglon, Haut-Lac)
- Breakpoint 375px : seulement 1/9 a un breakpoint specifique 375px (Haut-Lac) - les autres s'arretent a 768px
- ARIA : la couverture est inegale (8 a 30 attributs aria-label/aria-expanded selon le mockup)
- Contraste sur dark backgrounds : plusieurs mockups ont du texte a opacite 0.5-0.6 sur fond sombre, risquant de ne pas atteindre 4.5:1

---

## Detail par mockup

### 1. Beau Soleil (`inspired-beausoleil`)

**Fonts** : Anybody + DM Sans (Google Fonts) -- choix distinctif, conforme aux tokens Beau Soleil
**Palette** : Navy #002654, blue accent #0087c9, gold #ffd931 -- ancree sur les tokens
**Structure** : Hero video full-bleed, intro split, chiffres navy, curriculum grid 2x2, photo editoriale full-width, citation, vie quotidienne mosaique, Paris split, temoignages carrousel, CTA, footer
**Creativite** : Bonne. Le rythme blanc/navy/blanc/navy cree une alternance editoriale. L'accent border dore sur l'image d'intro est un detail soigne. Le carrousel de temoignages avec dots est fonctionnel.

| Critere | Score | Notes |
|---------|-------|-------|
| WCAG 2.1 AA | 8/10 | Skip-link OK, focus-visible OK, prefers-reduced-motion OK, heading hierarchy H1>H2>H3, touch 48px sur CTA et carousel dots, 30 aria attributes |
| Responsive | 7/10 | Media query 768px OK mais pas de 375px specifique |
| Token adherence | 9/10 | Navy, blue, gold corrects. Fonts non-generiques |
| Anti-slop | 8/10 | Pas de purple gradients, pas de 3-boxes-with-icons. Curriculum grid 2x2 est un peu generique |
| Creativite structurelle | 7/10 | Fidele au style Beau Soleil (clean, navy, pill buttons) mais structure relativement classique |
| Contenu | 9/10 | Francais avec accents, textes originaux, temoignages credibles |
| Assets BISP | 10/10 | Logo, video, photos, logos accreditation |

**Issues** :
- **Major** : Pas de breakpoint 375px
- **Minor** : Texte `.chiffre-label` a `opacity: 0.65` sur fond navy -- risque contraste
- **Minor** : Les carousel dots utilisent un hack visuel (min-width 48px avec ::after 8px) -- fonctionnel mais complexe

---

### 2. Aiglon (`inspired-aiglon`)

**Fonts** : Be Vietnam Pro (Google Fonts) -- proxy correct pour Calibre (Aiglon). `system-ui, Helvetica` en fallback (acceptable comme fallback, pas comme primaire)
**Palette** : Noir profond #060a14, rouge #b11d23, or #ceab52 -- fidele aux tokens Aiglon
**Structure** : Hero video cinematique, conviction split, piliers photo grid 2x2, parcours timeline zigzag, Paris full-bleed, metrics counters, temoignages grid 3 colonnes, mosaique photos, CTA, footer
**Creativite** : Excellente. Le grain overlay, la barre rouge en haut du nav, le zigzag timeline avec dots dores, les pillar cards photo full-bleed avec gradient overlay -- tout ca cree une atmosphere cinematique tres Aiglon.

| Critere | Score | Notes |
|---------|-------|-------|
| WCAG 2.1 AA | 7/10 | Skip-link OK, focus-visible (or), prefers-reduced-motion OK, mais seulement 8 aria attributes (le plus bas). body line-height 1.0 est trop serre |
| Responsive | 7/10 | Media query 768px OK mais pas de 375px |
| Token adherence | 9/10 | Rouge, or, noir profond corrects. Be Vietnam Pro est un bon proxy Calibre |
| Anti-slop | 9/10 | Zero generique. Grain texture, zigzag timeline, photo grid asymetrique |
| Creativite structurelle | 9/10 | Tres fidele a l'atmosphere Aiglon : cinematique, dark, angular |
| Contenu | 9/10 | Francais avec accents, textes originaux, accroches percutantes |
| Assets BISP | 9/10 | Logo (avec filtre invert), video, photos. Pas de logos accreditation visibles en premier scroll |

**Issues** :
- **Critical** : `body { line-height: 1.0; }` -- trop serre pour la lisibilite, WCAG recommande 1.5 minimum pour le corps de texte
- **Major** : Seulement 8 aria attributes -- les nav-links manquent d'aria-label, le carrousel n'a pas de role
- **Major** : Pas de breakpoint 375px
- **Minor** : `system-ui, Helvetica` dans le fallback font -- acceptable mais non ideal

---

### 3. Le Rosey (`inspired-lerosey`)

**Fonts** : EB Garamond + Playfair Display (Google Fonts) -- serif bichromatique, tres Le Rosey
**Palette** : Blanc + navy #182f66 uniquement -- bichromatie radicale fidele a Le Rosey
**Structure** : Hero textuel (pas de video en hero), intro split, mosaique photo editorial, piliers 4 colonnes sur navy, chiffres inline, double parcours split, vie quotidienne grid 3 cartes, temoignage centree, video avec play button, admissions CTA navy, footer
**Creativite** : Elegante. La retenue est le message. Le hero textuel sans image est un choix courageux qui reproduit l'approche Le Rosey. La mosaique photo asymetrique avec overlays est soignee.

| Critere | Score | Notes |
|---------|-------|-------|
| WCAG 2.1 AA | 7/10 | Skip-link OK, prefers-reduced-motion OK, mais le skip-link n'a pas de transition visible. 14 aria attributes. Les nav-links utilisent `:focus` au lieu de `:focus-visible` |
| Responsive | 7/10 | Media query 768px OK, pas de 375px. Le hero textuel devrait bien scaler |
| Token adherence | 10/10 | Bichromatie blanc/navy parfaite. EB Garamond + Playfair = serif editorial fidele |
| Anti-slop | 9/10 | Zero generique. Retenue deliberee, pas de gadgets |
| Creativite structurelle | 9/10 | Tres fidele au Le Rosey : aristocratique, textuel, minimaliste |
| Contenu | 9/10 | Francais avec accents, textes raffines, ton juste |
| Assets BISP | 9/10 | Logo, video (dans section dediee), photos, accreditations |

**Issues** :
- **Major** : Pas de touch target 48px explicite sur aucun element interactif (CTA, liens nav)
- **Major** : Pas de breakpoint 375px
- **Minor** : `:focus` au lieu de `:focus-visible` sur nav-links -- affiche l'outline au clic souris
- **Minor** : Le hero sans video/image est un risque UX pour le public cible HNW (premiere impression moins immersive)

---

### 4. Sevenoaks (`inspired-sevenoaks`)

**Fonts** : Satoshi (Fontshare) -- excellent choix premium, non-generique
**Palette** : Teal #004f5d, violet #4a2072, blanc -- fidele aux tokens Sevenoaks
**Structure** : Hero split (photo gauche, violet block droite), intro centree, mosaique photo, piliers 2x2 avec numeros geants, feature splits alternants, stats sur teal, temoignage centree, accreditations, CTA band violet, footer
**Creativite** : Tres forte. Le hero split avec le bloc violet est audacieux et distinctif. Les piliers sans icones (juste des numeros geants en filigrane) sont un choix editorial courageux. Les feature splits alternants evitent la monotonie.

| Critere | Score | Notes |
|---------|-------|-------|
| WCAG 2.1 AA | 8/10 | Skip-link OK, focus-visible OK, prefers-reduced-motion OK, 27 aria attributes (bon), mobile menu avec aria-expanded |
| Responsive | 8/10 | Media query 768px, mobile menu complet avec overlay, animations desactivees en mobile |
| Token adherence | 9/10 | Teal, violet corrects. Satoshi est un excellent proxy |
| Anti-slop | 10/10 | Zero generique. Hero split asymetrique, piliers sans icones, feature alternance |
| Creativite structurelle | 9/10 | Le hero split avec bloc violet est une signature forte. Structure tres fidele au langage Sevenoaks |
| Contenu | 9/10 | Francais avec accents, textes originaux |
| Assets BISP | 9/10 | Logo, video en hero, accreditations, photos |

**Issues** :
- **Major** : Pas de breakpoint 375px specifique
- **Minor** : Le violet profond (#4a2072) avec texte blanc doit etre verifie pour le contraste 4.5:1 -- le ratio est ~7.8:1, OK
- **Minor** : Les `stat__number` a font-size clamp(48px,5vw,72px) pourraient depasser le viewport en mobile sans breakpoint 375px

---

### 5. Gordonstoun (`inspired-gordonstoun`)

**Fonts** : Playfair Display + Clash Display + DM Sans -- triple stack editorial, tres Gordonstoun
**Palette** : Pourpre #702381, lavande #c7b0d5, creme #faf8f6, noir -- fidele aux tokens
**Structure** : Hero split asymetrique (texte gauche, video droite), split gris avec image, citation pleine page photo overlay, "BISP en un regard" grid asymetrique, mosaique photos decalees, parcours timeline horizontal, temoignages layout sticky, CTA split, footer
**Creativite** : Remarquable. Le mixed caps + italic system (.t-caps / .t-italic), le side badge fixe, les mosaiques avec offsets deliberes, le layout "at a glance" asymetrique -- tout reproduit l'editorial magazine de Gordonstoun. Les decorations en cercles sont fideles.

| Critere | Score | Notes |
|---------|-------|-------|
| WCAG 2.1 AA | 7/10 | Skip-link OK, focus outline lavande, prefers-reduced-motion OK, 19 aria attributes. Mais pas de focus-visible explicite (utilise l'outline par defaut) |
| Responsive | 7/10 | Media query 768px OK, pas de 375px |
| Token adherence | 9/10 | Pourpre, lavande, creme corrects. Clash Display est un excellent choix editorial |
| Anti-slop | 10/10 | Zero generique. Chaque section a une structure differente. Le grain overlay, le side badge, les mosaiques offset |
| Creativite structurelle | 10/10 | La plus distinctive des 9. Chaque section surprend. Fidele au langage magazine Gordonstoun |
| Contenu | 9/10 | Francais avec accents, textes originaux, ton editorial |
| Assets BISP | 9/10 | Logo, video, photos. Accreditations non visibles en scroll initial |

**Issues** :
- **Major** : Pas de touch target 48px -- les boutons ont des padding genereux mais pas de min-height/min-width explicite
- **Major** : Pas de breakpoint 375px
- **Minor** : Le grain overlay `body::after` avec z-index 9999 pourrait interferir avec des elements interactifs (pointer-events: none est present, OK)
- **Minor** : Le side badge fixe pourrait chevaucher le contenu en mobile

---

### 6. Repton (`inspired-repton`)

**Fonts** : Cormorant Garamond + Montserrat (Google Fonts) -- serif + sans duo, fidele a Repton
**Palette** : Navy #3e4561, gold #988360, grey whisper #f4f4f4 -- quiet luxury fidele
**Structure** : Hero split (texte gauche, portrait droite avec accent line et stat overlay), accreditations bar, timeline spine verticale avec zigzag, key figures, video section, temoignage centree, Paris photo avec overlay lateral, gallery grid asymetrique, CTA section, footer
**Creativite** : Excellente. La timeline spine doree avec les dots et le zigzag est la signature du mockup. Le portrait hero avec l'accent line corner et le stat overlay est soigne. L'ambiance "quiet luxury" est maitrisee.

| Critere | Score | Notes |
|---------|-------|-------|
| WCAG 2.1 AA | 8/10 | Skip-link OK, focus-visible avec outline gold sur les liens et CTAs, prefers-reduced-motion OK, 20 aria attributes |
| Responsive | 7/10 | Media query 768px, pas de 375px. La timeline zigzag va se compresser |
| Token adherence | 9/10 | Navy, gold, grey corrects. Cormorant Garamond est un excellent proxy serif |
| Anti-slop | 9/10 | Zero generique. Timeline spine, portrait asymetrique, gallery grid |
| Creativite structurelle | 9/10 | La timeline est une structure tres distinctive et coherente. Fidele au langage Repton |
| Contenu | 9/10 | Francais avec accents, textes soignes, ton raffine |
| Assets BISP | 9/10 | Logo, video, photos, accreditations |

**Issues** :
- **Major** : Pas de breakpoint 375px -- la timeline va mal scaler
- **Minor** : Les textes `.tl-body` avec color: var(--grey-text) sur fond blanc sont OK mais les labels overline a opacity 0.5 pourraient etre limites
- **Minor** : Le hero stat overlay (position absolute bottom: -30px, left: -30px) pourrait depasser le viewport en mobile

---

### 7. Kent College (`inspired-kentcollege`)

**Fonts** : Montserrat (Google Fonts) -- single font, bold et energetique
**Palette** : Crimson #aa0040, coral #ff4951, blanc -- fidele aux tokens Kent College
**Structure** : Hero split (texte gauche, blobs organiques droite), passion section crimson avec mosaique organic, chiffres avec separateurs coral, double parcours (2 cards FR/EN), vie quotidienne splits alternants avec images blob, portraits d'eleves (circle portraits), Paris split avec image rounded, CTA centree, footer
**Creativite** : Forte. Les blobs organiques avec animation morphBlob sont une signature visuelle claire. Les rounded shapes partout (50px, blob, circle portraits) creent une coherence. Le watermark "BISP" en 20vw dans la section passion est un geste audacieux.

| Critere | Score | Notes |
|---------|-------|-------|
| WCAG 2.1 AA | 7/10 | Skip-link OK (mais sans transition :focus), prefers-reduced-motion OK, 26 aria attributes. Focus-visible absent du CSS (seulement :focus sur les liens) |
| Responsive | 7/10 | Media query 768px, pas de 375px. Les blobs vont deborder |
| Token adherence | 8/10 | Crimson, coral corrects. Montserrat est un peu generique mais acceptable pour Kent College |
| Anti-slop | 8/10 | Les blobs sont distinctifs. Les portraits circulaires sont un risque "portrait grid" mais les circles avec border coral et les quotes personnalisees sauvent le design |
| Creativite structurelle | 8/10 | Les blobs et les rounded shapes creent une identite. Les alternances image/texte sont bien executees |
| Contenu | 9/10 | Francais avec accents, textes originaux, portraits d'eleves nommes |
| Assets BISP | 8/10 | Logo, photos, accreditations. Video de presentation non utilisee en hero |

**Issues** :
- **Major** : Pas de `:focus-visible` dans le CSS -- seulement `:focus` sur nav links
- **Major** : Pas de breakpoint 375px
- **Minor** : Le skip-link n'a pas de transition (saute de top:-100% a top:0 sans animation)
- **Minor** : Montserrat en single font pourrait manquer de personnalite pour un site HNW

---

### 8. Haut-Lac (`inspired-hautlac`)

**Fonts** : Montserrat + Be Vietnam Pro (Google Fonts) -- double stack, fidele aux tokens Haut-Lac
**Palette** : Teal #348397, red #ed3122, green #429e7b, orange #d89137 -- palette 4 couleurs fidele
**Structure** : Hero teal avec video B&W, mosaic stats, promesse split avec image stack et dot pattern, piliers 4 cards sur diagonal teal, campus mosaique avec borders colorees, parcours timeline horizontal multi-couleur, temoignages 3 cards sur teal diagonal, Paris split avec badge, CTA, footer
**Creativite** : Tres forte. Les diagonal clip-paths, les borders colorees par pilier (teal/red/green/orange), les dot patterns, le B&W-to-color hover sur la video, les rotating words dans le H1 -- tout ca cree un design energetique et systematique fidele a Haut-Lac.

| Critere | Score | Notes |
|---------|-------|-------|
| WCAG 2.1 AA | 8/10 | Skip-link OK, prefers-reduced-motion OK, 16 aria attributes. Touch targets 48px sur hero CTAs et mobile menu button |
| Responsive | 9/10 | Media query 768px ET 375px (seul mockup avec le breakpoint 375). Dot patterns et mosaiques gerees |
| Token adherence | 9/10 | Teal, red, green, orange fideles. Montserrat acceptable |
| Anti-slop | 8/10 | Les diagonales et les 4 couleurs sont distinctifs. La timeline horizontale multi-couleur est unique. Mais les pilier-cards 4 colonnes avec icones numerotees sont un peu "cards with numbers" |
| Creativite structurelle | 8/10 | Les diagonales clip-path et le systeme de couleurs 4 axes sont la signature. Fidele a Haut-Lac |
| Contenu | 9/10 | Francais avec accents, textes originaux, rotating words en hero |
| Assets BISP | 10/10 | Logo, video, photos, accreditations, tout utilise |

**Issues** :
- **Minor** : Les pilier-cards avec numeros et hover sont un pattern un peu vu
- **Minor** : La palette 4 couleurs peut creer une complexite visuelle excessive sur petit ecran
- **Minor** : Le hero B&W filter `grayscale(100%) brightness(0.45)` reduit fortement la lisibilite des images

---

### 9. Ecole des Roches (`inspired-ecoledesroches`)

**Fonts** : Cormorant Garamond + Nunito Sans (Google Fonts) -- serif + ultra-legere, fidele aux tokens
**Palette** : Navy profond #0b1e3a, gold #fdb82e, blanc -- cinematique fidele
**Structure** : Hero centre cinematique avec watermark world map, strip chiffres dores, vision split avec image rounded et accent gold badge, programmes 4 cards avec photo overlay, double curriculum split editorial avec photo band, video section immersive, temoignages carousel, Paris magazine strip, CTA, footer
**Creativite** : Excellente. Le world map watermark SVG en hero, les ombres cinematiques (136px !), les programme cards avec overlays progressifs, la photo band editoriale dans le curriculum section, les pill shapes -- tout contribue a une atmosphere premium cinematique.

| Critere | Score | Notes |
|---------|-------|-------|
| WCAG 2.1 AA | 8/10 | Skip-link OK (style gold pill), focus-visible implicite via outline, prefers-reduced-motion DECLARE EN PREMIER (best practice), 20 aria attributes |
| Responsive | 7/10 | Media query 768px, pas de 375px |
| Token adherence | 10/10 | Navy profond, gold, blanc fideles. Cormorant Garamond + Nunito Sans sont des proxys excellents |
| Anti-slop | 9/10 | Zero generique. World map watermark, cinema shadows, magazine editorial layout |
| Creativite structurelle | 9/10 | Tres fidele a l'atmosphere Ecole des Roches : cinematique, profonde, editoriale |
| Contenu | 9/10 | Francais avec accents, textes soignes |
| Assets BISP | 10/10 | Logo + texte, video, photos, accreditations |

**Issues** :
- **Major** : Pas de breakpoint 375px
- **Minor** : La hero subtitle font-weight 200 (`Nunito Sans 200`) sur fond navy profond avec color opacity 0.65 est un risque contraste
- **Minor** : Les programme cards a 4 colonnes vont se compresser fortement en mobile sans breakpoint fin

---

## Tableau comparatif

| Mockup | WCAG | Responsive | Tokens | Anti-slop | Creativite | Contenu | Assets | **TOTAL** |
|--------|------|-----------|--------|-----------|------------|---------|--------|-----------|
| **Gordonstoun** | 7 | 7 | 9 | 10 | **10** | 9 | 9 | **61** |
| **Sevenoaks** | 8 | 8 | 9 | **10** | 9 | 9 | 9 | **62** |
| **Ecole des Roches** | 8 | 7 | **10** | 9 | 9 | 9 | **10** | **62** |
| **Aiglon** | 7 | 7 | 9 | 9 | 9 | 9 | 9 | **59** |
| **Le Rosey** | 7 | 7 | **10** | 9 | 9 | 9 | 9 | **60** |
| **Repton** | 8 | 7 | 9 | 9 | 9 | 9 | 9 | **60** |
| **Beau Soleil** | 8 | 7 | 9 | 8 | 7 | 9 | **10** | **58** |
| **Haut-Lac** | 8 | **9** | 9 | 8 | 8 | 9 | **10** | **61** |
| **Kent College** | 7 | 7 | 8 | 8 | 8 | 9 | 8 | **55** |

**Top 3 par creativite structurelle** : Gordonstoun (10), Sevenoaks (9), Aiglon/Le Rosey/Repton/Ecole des Roches (9 ex aequo)

**Top 3 par qualite technique** : Sevenoaks (WCAG 8, Responsive 8), Haut-Lac (Responsive 9, touch targets), Ecole des Roches (prefers-reduced-motion first, tokens 10)

---

## Issues par severite

### Critical (1)

| # | Mockup | Issue | Impact |
|---|--------|-------|--------|
| C1 | Aiglon | `body { line-height: 1.0 }` | Corps de texte illisible pour de nombreux utilisateurs. WCAG SC 1.4.12 (espacement du texte) |

### Major (14)

| # | Mockup | Issue | Impact |
|---|--------|-------|--------|
| M1 | Beau Soleil | Pas de breakpoint 375px | Mise en page cassee sur iPhone SE / petits mobiles |
| M2 | Aiglon | Pas de breakpoint 375px | Idem |
| M3 | Aiglon | 8 aria attributes seulement | Navigation, carrousel et landmarks non annonces aux lecteurs d'ecran |
| M4 | Le Rosey | Pas de breakpoint 375px | Idem |
| M5 | Le Rosey | Pas de touch target 48px | Boutons et liens trop petits en tactile |
| M6 | Sevenoaks | Pas de breakpoint 375px | Idem |
| M7 | Gordonstoun | Pas de breakpoint 375px | Idem |
| M8 | Gordonstoun | Pas de touch target 48px | Idem Le Rosey |
| M9 | Repton | Pas de breakpoint 375px | Timeline va mal scaler |
| M10 | Kent College | Pas de `:focus-visible` | Outline au clic souris, mauvaise UX |
| M11 | Kent College | Pas de breakpoint 375px | Blobs vont deborder |
| M12 | Ecole des Roches | Pas de breakpoint 375px | 4 colonnes programmes compressees |
| M13 | Ecole des Roches | Pas de touch target 48px | Boutons nav trop petits en tactile |
| M14 | Repton | Pas de touch target 48px | Liens timeline trop petits en tactile |

### Minor (14)

| # | Mockup | Issue | Impact |
|---|--------|-------|--------|
| m1 | Beau Soleil | `.chiffre-label` opacity 0.65 sur navy | Risque contraste |
| m2 | Beau Soleil | Carousel dots hack complexe | Maintenabilite |
| m3 | Aiglon | `system-ui, Helvetica` en fallback | Acceptable mais non ideal |
| m4 | Le Rosey | `:focus` au lieu de `:focus-visible` | Outline visible au clic souris |
| m5 | Le Rosey | Hero sans image/video | Risque UX premiere impression |
| m6 | Sevenoaks | Stats font-size risque overflow 375px | Debordement possible |
| m7 | Gordonstoun | Grain overlay z-index 9999 | Potentielle interference |
| m8 | Gordonstoun | Side badge en mobile | Chevauchement possible |
| m9 | Repton | Hero stat overlay position absolute | Debordement en mobile |
| m10 | Repton | Overline labels opacity 0.5 | Risque contraste |
| m11 | Kent College | Skip-link sans transition | Saut visuel abrupt |
| m12 | Kent College | Montserrat en single font | Personnalite limitee pour HNW |
| m13 | Haut-Lac | Pilier-cards pattern generique | Manque d'originalite locale |
| m14 | Ecole des Roches | Subtitle font-weight 200, opacity 0.65 | Risque contraste sur navy |

---

## Recommandations prioritaires

1. **Ajouter un breakpoint 375px a tous les mockups** (8/9 manquent) -- minimum : grid single-column, font-size adaptes, padding reduits
2. **Corriger le line-height 1.0 d'Aiglon** -- passer a 1.5 minimum pour le body
3. **Ajouter touch targets 48px** sur tous les elements interactifs des 6 mockups qui n'en ont pas
4. **Uniformiser `:focus-visible`** au lieu de `:focus` sur Le Rosey et Kent College
5. **Ameliorer la couverture ARIA** d'Aiglon (landmarks, nav, carrousel)

---

**FIN DE L'AUDIT**
