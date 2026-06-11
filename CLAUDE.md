# CLAUDE.md — Site vitrine CLEAN IMPERIAL

> Ce fichier est le **brief global** destiné à Claude Code pour générer l’intégralité du site
> vitrine de **Clean Imperial** (Yaoundé, Cameroun). Il contient : identité de marque, palette,
> typographie, structure des pages, contenu rédactionnel complet, grilles tarifaires et
> directives techniques. **Toutes les informations ci-dessous proviennent des brochures
> officielles de l’entreprise — ne pas inventer d’autres prix, contacts ou services.**

-----

## 1. IDENTITÉ DE LA MARQUE

|Champ              |Valeur                                                                                                        |
|-------------------|--------------------------------------------------------------------------------------------------------------|
|**Nom**            |Clean Imperial                                                                                                |
|**Signature**      |*L’Empereur du Nettoyage*                                                                                     |
|**Slogan**         |L’excellence du nettoyage professionnel et industriel                                                         |
|**4 piliers**      |Propreté · Santé · Sécurité · Qualité                                                                         |
|**Activité**       |Nettoyage professionnel & industriel, blanchisserie, pressing, traitement des surfaces, hygiène & désinfection|
|**Localisation**   |Yaoundé – Awae, Carrefour Monti (Façade Prodiges Hôtel), Cameroun                                             |
|**Téléphones**     |(+237) 694 96 29 48 · (+237) 651 68 68 68                                                                     |
|**WhatsApp**       |+237 651 68 68 68                                                                                             |
|**Email**          |[cleanimperialcmr@gmail.com](mailto:cleanimperialcmr@gmail.com)                                               |
|**Réseaux sociaux**|Facebook, Instagram, TikTok, X, LinkedIn — nom de compte : « Clean Impérial »                                 |

**Positionnement** : marque “impériale” haut de gamme mais accessible — sérieux, rigueur,
confiance B2B (hôtels, hôpitaux, entreprises) tout en restant proche des particuliers
pour le pressing/blanchisserie.

-----

## 2. IDENTITÉ VISUELLE

### Palette de couleurs (extraite des brochures)

|Token         |Hex      |Usage                                                                            |
|--------------|---------|---------------------------------------------------------------------------------|
|`--navy`      |`#0E2240`|Fond principal des sections sombres, header, footer, titres                      |
|`--navy-deep` |`#091831`|Dégradés, fond du hero                                                           |
|`--gold`      |`#C9A227`|Couleur d’accent principale : boutons, soulignés de titres, bordures, icônes     |
|`--gold-light`|`#E8C766`|Dégradés dorés (bandeaux diagonaux signature des brochures)                      |
|`--teal`      |`#2BB3B1`|Accent secondaire (couleur du logo) : sous-titres de services, icônes secondaires|
|`--white`     |`#FFFFFF`|Fonds clairs, texte sur navy                                                     |
|`--off-white` |`#F6F7FA`|Fond des sections claires alternées                                              |
|`--ink`       |`#1A2433`|Texte courant sur fond clair                                                     |
|`--whatsapp`  |`#25D366`|Uniquement le bouton WhatsApp flottant                                           |

**Motif signature** : les brochures utilisent des **bandeaux diagonaux dorés en dégradé**
(`linear-gradient(135deg, #C9A227, #E8C766, #C9A227)`). Reprendre ce motif comme élément
graphique récurrent : liseré diagonal en bas du hero, séparateurs de sections, bordure
des cartes mises en avant. C’est LA signature visuelle du site.

### Typographie

- **Display / titres** : `Montserrat` (Google Fonts), graisses 700–800, majuscules pour
  les titres de sections — fidèle au style des brochures.
- **Signature script** : `Great Vibes` (Google Fonts) — UNIQUEMENT pour la mention
  *« L’Empereur du Nettoyage »* (hero et footer), en doré sur navy.
- **Corps de texte** : `Inter` ou `Open Sans`, 400/600, interlignage 1.6.
- Titres de section : majuscules navy (ou blanc sur fond navy) avec un **souligné doré
  court** (60px, 3px) à gauche — exactement comme dans les brochures.

### Style général

- Sections alternées : fond blanc / off-white / navy (la section Tarifs ou Contact en navy).
- Cartes avec coins arrondis 12px, ombre douce `0 8px 32px rgba(14,34,64,.10)`.
- Icônes : Font Awesome (CDN) ou SVG inline, style ligne, doré ou teal.
- Boutons primaires : fond doré dégradé, texte navy, gras, arrondi 8px, hover léger lift.
- Boutons secondaires : contour doré, texte doré, fond transparent.
- Animations : reveal au scroll discret (fade-up via IntersectionObserver), respecter
  `prefers-reduced-motion`. Pas d’excès.
- **Bouton WhatsApp flottant** en bas à droite sur toutes les pages →
  `https://wa.me/237651686868?text=Bonjour%20Clean%20Imperial,%20je%20souhaite%20un%20devis`

-----

## 3. STACK TECHNIQUE

- **HTML5 + CSS3 + JavaScript vanilla** (pas de framework, pas de build) — site statique
  100 % compatible **GitHub Pages**.
- Fichiers : `index.html`, `services.html`, `tarifs.html`, `contact.html`,
  `css/style.css`, `js/main.js`, dossier `img/` (placeholders pour l’instant).
- Responsive **mobile-first** (la clientèle consulte majoritairement sur téléphone).
- SEO : balises `<title>` et `<meta description>` uniques par page, Open Graph,
  attributs `alt`, HTML sémantique (`header/nav/main/section/footer`), `lang="fr"`.
- Données structurées JSON-LD type `LocalBusiness` (nom, téléphone, adresse Yaoundé-Awae,
  horaires si fournis plus tard).
- Performance : images en `loading="lazy"`, pas de librairie lourde.
- Accessibilité : contrastes respectés (texte doré jamais sur blanc — réserver le doré
  aux fonds navy ou aux éléments épais), focus visible, navigation clavier.

### Images

Utiliser des **placeholders** propres (div avec dégradé navy + icône + libellé) nommés
explicitement : `img/hero-equipe.jpg`, `img/nettoyage-industriel.jpg`,
`img/blanchisserie.jpg`, `img/marbre.jpg`, `img/desinfection.jpg`,
`img/fin-chantier.jpg`, `img/bureaux.jpg`, `img/facade-pressing.jpg`,
`img/client-prodiges.png`, `img/client-allodocteur.png`, `img/client-prima.png`.
Les vraies photos seront ajoutées plus tard avec ces noms exacts.

-----

## 4. NAVIGATION

Header sticky, fond navy, logo texte « CLEAN **IMPERIAL** » (Clean en blanc, Imperial en
doré ou teal), menu burger sur mobile :

`Accueil · Services · Tarifs · Contact` + bouton CTA doré « Demander un devis »
(ancre vers le formulaire de contact).

-----

## 5. PAGE ACCUEIL — `index.html`

### 5.1 Hero

- Fond navy profond (dégradé `--navy-deep` → `--navy`), liseré diagonal doré en bas.
- Surtitre script doré : *L’Empereur du Nettoyage*
- H1 : **CLEAN IMPERIAL**
- Sous-titre : « L’excellence du nettoyage professionnel et industriel »
- Les 4 piliers en badges dorés : Propreté · Santé · Sécurité · Qualité
- 2 boutons : « Demander un devis » (doré) et « Voir nos tarifs » (contour).

### 5.2 Qui sommes-nous ?

Texte officiel (brochure) :

> Clean Imperial est une entreprise spécialisée dans les solutions de nettoyage
> professionnel, d’entretien industriel et de traitement technique des surfaces.
> Nous accompagnons les entreprises, hôtels, établissements de santé et institutions
> dans la gestion complète de leur hygiène et de leurs espaces, en garantissant des
> standards élevés de qualité, de sécurité et de performance.
> 
> Grâce à une équipe qualifiée, des équipements adaptés et une approche orientée
> résultats, nous proposons des prestations sur mesure répondant aux exigences
> spécifiques de chaque secteur.

**Notre mission** : Offrir des services de nettoyage et d’entretien fiables, efficaces
et durables, tout en contribuant à créer des environnements sains, propres et
accueillants pour nos clients et leurs usagers.

### 5.3 Nos services (aperçu — 6 cartes, lien vers services.html)

1. **Nettoyage professionnel** — bureaux, hôtels, restaurants, résidences
1. **Entretien industriel & blanchisserie** — blanchisserie industrielle, grands sites
1. **Traitement & rénovation des surfaces** — ponçage marbre, remise à neuf des sols
1. **Hygiène & désinfection** — espaces sensibles, traitement antibactérien
1. **Pressing & blanchisserie particuliers** — packs au kilo et à la pièce
1. **Nettoyage de fin de chantier** — livraison de locaux propres et prêts

### 5.4 Pourquoi choisir Clean Imperial ? (4 cartes, contenu officiel)

1. **Une équipe professionnelle et qualifiée** — Des agents formés et encadrés pour
   garantir des prestations fiables et professionnelles.
1. **Des solutions adaptées à chaque structure** — Des prestations personnalisées selon
   vos besoins et votre secteur d’activité.
1. **Réactivité & efficacité** — Des interventions rapides, organisées et conformes aux
   normes d’hygiène et de sécurité.
1. **Engagement qualité** — Des équipements performants et des produits professionnels
   pour des résultats durables.

### 5.5 Notre approche (4 étapes — frise numérotée, l’ordre est réel)

1. **Analyse des besoins** — Étude de votre environnement et de vos exigences
1. **Proposition personnalisée** — Élaboration d’une offre adaptée à votre activité
1. **Mise en œuvre opérationnelle** — Déploiement d’équipes qualifiées et d’équipements adaptés
1. **Suivi qualité & amélioration continue** — Contrôle régulier et ajustement des prestations

### 5.6 Ils nous ont fait confiance

3 références (cartes logo + nom) : **Prodiges Hôtel** · **Allô Docteur** · **Laboratoire Prima**

### 5.7 Nos clients (secteurs)

Hôtels & complexes touristiques · Hôpitaux, cliniques & centres de santé ·
Restaurants & établissements alimentaires · Entreprises & bureaux ·
Institutions & administrations

### 5.8 Bandeau CTA (fond navy, liseré doré)

> Confiez-nous l’entretien de vos espaces et bénéficiez d’un service professionnel à la
> hauteur de vos exigences. Demandez dès maintenant une étude personnalisée et un devis
> adapté à vos besoins.

Bouton doré « Demander un devis » + bouton WhatsApp.

-----

## 6. PAGE SERVICES — `services.html`

Une section détaillée par domaine (image placeholder + texte officiel) :

### Nettoyage professionnel

- Nettoyage de bureaux et espaces administratifs
- Entretien d’hôtels et établissements touristiques
- Nettoyage de restaurants et espaces de restauration
- Entretien de résidences et immeubles

### Nettoyage industriel et commercial

**Nous intervenons sur** : sites industriels, zones de production, grandes surfaces,
ateliers, espaces commerciaux.
**Nos prestations incluent** : balayage et lavage des sols, dégraissage des machines et
équipements, dépoussiérage des surfaces techniques, désinfection des sanitaires et
espaces communs, gestion des déchets industriels.

### Entretien industriel & blanchisserie

- Blanchisserie industrielle (hôtels, hôpitaux, restaurants…)
- Nettoyage de grandes surfaces et sites industriels
- Entretien d’environnements à forte exigence
- Gestion complète de l’hygiène sur site

### Nettoyage de bureaux & conciergerie

Entretien complet des espaces professionnels afin de garantir :

- Un environnement de travail propre et agréable
- Une meilleure image de marque
- Le respect des normes d’hygiène
- Le confort des collaborateurs et visiteurs

### Traitement & rénovation des surfaces

- Ponçage et traitement du marbre
- Nettoyage et entretien des carreaux extérieurs
- Entretien des esplanades et surfaces extérieures
- Rénovation, protection et remise à neuf des sols

### Hygiène & désinfection / Assainissement

Techniques de désinfection professionnelles et produits adaptés pour :

- Éliminer germes et bactéries
- Assainir les espaces sensibles
- Garantir un cadre sain et sécurisé
- Désinfection des espaces professionnels et sensibles
- Traitement antibactérien et assainissement
- Mise en place de protocoles adaptés aux normes sanitaires

### Nettoyage de fin de chantier

Nos équipes interviennent après travaux pour :

- Éliminer poussières et résidus
- Nettoyer les surfaces techniques
- Remettre les espaces en état rapidement
- Livrer des locaux propres et prêts à l’utilisation

### Notre valeur ajoutée (encadré doré en fin de page)

- Personnel qualifié, formé et encadré
- Utilisation d’équipements professionnels performants
- Interventions adaptées à chaque secteur d’activité
- Respect strict des normes d’hygiène et de sécurité
- Capacité à gérer des sites de petite et grande envergure
- Expertise technique en blanchisserie industrielle et traitement des surfaces

-----

## 7. PAGE TARIFS — `tarifs.html`

⚠️ Reprendre EXACTEMENT ces prix (FCFA), aucune invention. Présenter en cartes/tableaux
élégants style brochure (en-tête navy, lignes alternées, prix en doré gras).

### Blanchisserie (au kilo)

|Pack              |Prix      |
|------------------|----------|
|Pack 1 Kg         |2 000 F/kg|
|Pack 5 Kg         |1 900 F/kg|
|Pack 10–29 Kg     |1 800 F/kg|
|Pack 30 Kg et plus|1 600 F/kg|

### Pressing (à la pièce)

|Pack              |Prix       |
|------------------|-----------|
|Pack 10 Chemises  |700 F/pièce|
|Pack 5–9 Pantalons|900 F/pièce|
|Pack 10 Pantalons |800 F/pièce|
|Pack 5–9 Robes    |900 F/pièce|
|Pack 10 Robes     |800 F/pièce|

### Mise en avant spéciale (bandeau doré, icône nœud papillon)

**Nettoyage complet Costume : 3 000 F / pièce**

### Note sous les tableaux

« Plus la quantité est importante, plus le tarif est avantageux. Pour les prestations
entreprises (nettoyage, désinfection, surfaces), demandez une étude personnalisée et un
devis gratuit. » + bouton « Demander un devis ».

-----

## 8. PAGE CONTACT — `contact.html`

- **Coordonnées** (cartes avec icônes) : téléphones, email, WhatsApp, adresse
  « Yaoundé – Awae, Carrefour Monti (Façade Prodiges Hôtel) ».
- **Carte Google Maps** intégrée (iframe embed centré sur Awae, Yaoundé — placeholder
  d’embed générique de Yaoundé en attendant les coordonnées exactes).
- **Formulaire de devis** (Formspree — laisser `action="https://formspree.io/f/VOTRE_ID"`
  avec un commentaire HTML expliquant de remplacer l’ID) :
  Nom complet · Téléphone · Email · Type de service (select : Pressing/Blanchisserie,
  Nettoyage professionnel, Nettoyage industriel, Désinfection, Traitement des surfaces,
  Fin de chantier, Autre) · Message.
- **Réseaux sociaux** : icônes Facebook, Instagram, TikTok, X, LinkedIn → « Clean Impérial »
  (liens `#` en placeholder, à remplacer par les vraies URLs plus tard).

-----

## 9. FOOTER (toutes pages)

Fond navy-deep, liseré diagonal doré en haut :

- Colonne 1 : logo + signature script *L’Empereur du Nettoyage* + slogan
- Colonne 2 : liens de navigation
- Colonne 3 : contacts (tél, email, adresse)
- Colonne 4 : les 4 piliers avec icônes (Propreté, Santé, Sécurité, Qualité)
- Barre basse : « © 2026 Clean Imperial — Tous droits réservés »

-----

## 10. ORDRE D’EXÉCUTION POUR CLAUDE CODE

1. Créer l’arborescence des fichiers.
1. Écrire `css/style.css` (variables CSS du §2, mobile-first).
1. Générer les 4 pages HTML avec tout le contenu de ce brief.
1. Écrire `js/main.js` : menu burger, reveal au scroll, année dynamique du footer.
1. Vérifier le responsive (320px → 1440px) et les contrastes.
1. Commit : `feat: site vitrine Clean Imperial complet` puis push sur `main`.
1. Si le dépôt utilise GitHub Pages sur une branche `gh-pages`, synchroniser
   cette branche avec `main` et pousser.

**Règle d’or : ne jamais inventer de prix, de numéro, d’adresse ou de service absent
de ce document. En cas de doute, laisser un placeholder commenté.**