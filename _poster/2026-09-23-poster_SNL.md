---
title: "Project 2: Sensorimotor Language Encoding"
subtitle: "SNL poster 2026: more on the figures and stories."
#hero_image: /xx/xx/short_stories.jpeg
#hero_alt: "Stories_Example"
---
[Download Poster (PDF)]({{ '/assets/cv/SarahSaneei_SNL2026.pdf' | relative_url }}){: .btn .btn--primary}

**TL;DR** Using sEEG recorded while patients listen to naturalistic stories, we ask how
sensorimotor features of language (motor, oral, internal and auditory-visual) are encoded
in cortex. Stories were built and validated so that each one emphasises a single dimension,
and word-locked broadband high-frequency activity (BHA) are going to be modelled with epoched ridge
regression on word-, sentence, and story-level LSN composites.

[Overview](#overview) · [Stimuli design: LSN groups](#composition) · [Stimuly design: stories](#design) · [Validation](#validation) · [Planned analysis](#analysis)

## Overview {#overview}

**Poster, SNL 2026.** *Cortical Encoding of Sensorimotor Language Features During Naturalistic Story Listening*

sEEG encoding model · Sandbox · 3 patients · Word- and sentence-level LSN composites · Broadband high-frequency activity (BHA)

## Stimuli design {#composition}

Stories were selected from a larger corpus and assigned to one of four sensorimotor
categories based on LSN composite scores, plus a neutral baseline condition.

**Categories:**  Oral  · Auditory-Visual · Internal · Motor · Neutral

<!-- Add figures by uncommenting and pointing to your image files, e.g.:
![Story composition overview: distribution of stories across categories and patients](/assets/photos/poster_SNL/composition.png)
![LSN composite distributions per category, across all valid words](/assets/photos/poster_SNL/lsn-distributions.png)
-->

## Stimuli design  (Stories) {#design}

Each sensorimotor category contains 4 matched stories, plus 4 neutral stories.
Below are example figures for each dimension and for the neutral baseline.


### Oral

![Top oral stories](/assets/photos/poster_SNL/group_top_oral_story1.png)

#### French: 
<p> Par un matin de printemps, Marie découvrit dans son jardin que la floraison des tulipes et des lys avait transformé sa pelouse en paradis coloré. Passionnée de gastronomie, elle décida de préparer un repas spécial avec des herbes fraîches de son potager. Elle concocta une délicieuse soupe de chou parfumée, accompagnée de pain frais de la boulangerie, de beurre et de fromage local. L'odeur qui s'échappait de sa cuisine attirant les voisins, elle ajouta une sauce à l'huile d'olive, du poivre, et même du saumon fumé qu'elle avait acheté au marché. Un verre de vin rouge et du jus d'orange frais complétaient ce festin, créant une ambiance chaleureuse où chaque chose avait du sens.
L'après-midi, les personnes du village arrivèrent pour célébrer cette journée insolite. Le boulanger apporta des pâtisseries au chocolat et au cacao, tandis que la brasserie locale offrait de la bière artisanale et un soupçon de rhum pour les plus aventureux. Les enfants transformèrent le jardin en cirque improvisé, jouant près des fruits et des herbes qui embaumaient l'air. On parlait d'environnement, de rejeter la pollution, les engrais chimiques, le diesel et le gaz, pour privilégier une vie plus saine. Contrairement aux souvenirs d'autrefois où tout sentait l'ammoniac et le tabac, cette existence culturelle renouvelée permettait à chacun de manger en paix, savourant chaque moment de bonheur simple et authentique. </p>

#### English:
<p>One spring morning, Marie discovered in her garden that the blooming tulips and lilies had transformed her lawn into a colorful paradise. As a food enthusiast, she decided to prepare a special meal using fresh herbs from her garden. She whipped up a delicious, fragrant cabbage soup, served with fresh bread from the bakery, butter, and local cheese. As the aroma wafting from her kitchen drew in the neighbors, she added a sauce made with olive oil, pepper, and even some smoked salmon she’d bought at the market. A glass of red wine and fresh orange juice rounded out the feast, creating a warm atmosphere where everything felt just right.
In the afternoon, the villagers arrived to celebrate this unusual day. The baker brought chocolate and cocoa pastries, while the local brewery offered craft beer and a splash of rum for the more adventurous. The children turned the garden into an impromptu circus, playing among the fruits and herbs that perfumed the air. People talked about the environment, about rejecting pollution, chemical fertilizers, diesel, and gas, in favor of a healthier lifestyle. Unlike memories from the past, when everything smelled of ammonia and tobacco, this renewed cultural way of life allowed everyone to eat in peace, savoring every moment of simple, authentic happiness.

<i>Translated with DeepL.com (free version)</i></p>


### Auditory-Visual

![Top auditory-visual stories](/assets/photos/poster_SNL/group_top_audvis_story4.png) 

#### French:
<p>Dans une petite ville pittoresque, un groupe d'amis passionnés de musique se réunissait chaque semaine pour partager leur amour du son et de la musique. Le groupe, composé de Julie au piano, Maxime à la clarinette et Léo, le bassiste, rêvait d'organiser un grand concert pour les habitants du village. Un jour, alors qu'ils discutaient de leur projet, un désaccord surgit sur le choix du thème musical. Julie voulait des morceaux classiques, tandis que Maxime suggérait des compositions modernes. Heureusement, Léo proposa de fusionner les deux styles pour créer une trame originale et musicale qui plairait à tout le public.
Le jour du concert arriva enfin, et la petite salle était pleine. Les premières notes du piano et de la clarinette résonnèrent dans la salle, et la magie opéra immédiatement. Les mélodies du piano, soutenues par les rythmes vibrants de la basse et de la clarinette, captivèrent le public. Chacun écoutait pour entendre chaque nuance de la musique. À la fin, le public se leva pour applaudir, demandant un rappel enthousiaste. Les musiciens, touchés par l'énergie du public et les paroles d'encouragement, promirent de donner un nouveau concert. Ce soir musical, un rêve était devenu réalité, et l'harmonie triompha des disputes initiales autour du thème.</p>

#### English:
<p>In a small, picturesque town, a group of friends who were passionate about music would get together every week to share their love of sound and music. The group—made up of Julie on piano, Maxime on clarinet, and Léo on bass—dreamed of putting on a big concert for the townspeople. One day, as they were discussing their project, a disagreement arose over the choice of musical theme. Julie wanted classical pieces, while Maxime suggested modern compositions. Fortunately, Léo proposed blending the two styles to create an original musical arrangement that would appeal to the entire audience.
The day of the concert finally arrived, and the small hall was packed. The first notes from the piano and clarinet echoed through the room, and the magic took hold immediately. The piano melodies, supported by the vibrant rhythms of the bass and clarinet, captivated the audience. Everyone listened intently to catch every nuance of the music. At the end, the audience rose to their feet to applaud, enthusiastically demanding an encore. The musicians, moved by the audience’s energy and words of encouragement, promised to give another concert. On that musical evening, a dream had come true, and harmony triumphed over the initial disagreements about the theme.

<i>Translated with DeepL.com (free version)</i></p>


### Internal

![Top internal stories](/assets/photos/poster_SNL/group_top_internal_story1.png)

#### French:
<p>Dans un village en altitude, vivait Élise, tourmentée par une profonde souffrance. Sa grossesse avait été suivie d'une fracture complexe et d'une infection persistante qui l'avait laissée en état d'affaiblissement constant. Ses nuits étaient hantées par des cauchemars, remplis de terreur et de panique, alimentant une anxiété profonde. Elle se sentait contrainte, confuse, et parfois même prisonnière de cette agonie. Son envie de dormir sans fin, d'oublier tout ce douloureux passé, était une obsession. Mais un instinct puissant, une volonté  inébranlable, la poussait à ne pas tenter de fuir complètement.
Un jour, cherchant à refroidir ses pensées, Élise rencontra Théo. Sa passion pour la botanique et son inspiration l'attirèrent. Il parlait de plantes nourrissantes et de l'empathie qu'il ressentait. Avec lui, Élise sentit une vigueur nouvelle. Ses blessures de l'âme commençaient à guérir. Leur humeur commune, positivement enjouée, fut marquée par des moments de légèreté et des discussions sur la croyance en la guérison. Malgré la nostalgie de son passé, Élise retrouva espoir et un sentiment de justesse. Ce fut un bonheur simple mais une immense satisfaction, un amour sublime né de leur bravoure partagée.</p>

#### English:
<p>In a high-altitude village lived Élise, tormented by profound suffering. Her pregnancy had been followed by a complex fracture and a persistent infection that had left her in a constant state of weakness. Her nights were haunted by nightmares, filled with terror and panic, fueling deep anxiety. She felt constrained, confused, and at times even trapped by this agony. Her desire to sleep endlessly, to forget that painful past, had become an obsession. But a powerful instinct, an unshakable will, urged her not to try to escape completely.
One day, seeking to clear her mind, Élise met Théo. She was drawn to his passion for botany and the inspiration he exuded. He spoke of nourishing plants and the empathy he felt. With him, Élise felt a newfound vigor. The wounds of her soul were beginning to heal. Their shared, positively cheerful spirit was marked by moments of lightheartedness and discussions about the belief in healing. Despite her nostalgia for the past, Élise rediscovered hope and a sense of rightness. It was a simple happiness but an immense satisfaction—a sublime love born of their shared courage.

<i>Translated with DeepL.com (free version)</i></p>





### Motor

![Top motor stories](/assets/photos/poster_SNL/group_top_motor_story4.png)

#### French:
<p>Dans une petite maison en brique au bord de la mer, vivait un artisan aux cheveux gris nommé Jean. Il passait ses journées à pousser les limites de son artisanat en créant des objets pratiques : un aimant pour retrouver les bijoux perdus, une brosse avec un système de lavage automatique, et même un pistolet à eau avec pression réglable pour arroser son jardin. Son atelier était rempli de meubles recouverts de velours. On y trouvait aussi un vieux tapis oriental et un établi couvert d'outils de précision. Il portait toujours ses bottes usées et un col en laine, et il notait chaque idée sur du papier froissé posé près d'un carnet de croquis. Ses mains expertes maniaient chaque outil avec précision, ses doigts habiles travaillant sur des surfaces de coton et autres matières. Dans son bain quotidien, il réfléchissait à ses créations, sentir l'eau chaude sur sa peau l'aidait à penser.
Un jour, alors qu'il testait un levier pour ramassage automatique, il fit la rencontre de Léa, une artiste textile venue chercher un ancien tissu rare. Fascinée par ses créations, elle s'assit sur une chaise près de lui, caressa la texture douce du coton qu'il lui tendait et l'écouta parler avec passion. Elle remarqua ses bras musclés par le travail, son cou solide, même son coude appuyé sur l'établi semblait naturel et rassurant. Ensemble, ils combinèrent leurs talents : elle créait des motifs soyeux sur des tissus flexibles, tandis qu'il y intégrait des boutons innovants et des systèmes de refroidissement. Leurs mains se touchaient souvent pendant le travail, un contact électrisant qui les rapprochait. Bientôt, leur collaboration donna naissance à une ligne de textiles interactifs. Ils tombèrent peu à peu amoureux, échangeant un baiser timide lors d'un test de tissu intelligent. Chaque surface de leur atelier vibrait désormais de créativité et de bonheur, et ils transformèrent même un vieux coin de l'atelier en espace de création partagée.</p>

#### English:
<p>In a small brick house by the sea lived a gray-haired craftsman named Jean. He spent his days pushing the boundaries of his craft by creating practical objects: a magnet to find lost jewelry, a brush with an automatic cleaning system, and even a water gun with adjustable pressure for watering his garden. His workshop was filled with velvet-upholstered furniture. There was also an old oriental rug and a workbench covered with precision tools. He always wore his worn-out boots and a woolen collar, and he jotted down every idea on crumpled paper placed next to a sketchbook. His expert hands handled each tool with precision, his nimble fingers working on surfaces of cotton and other materials. During his daily bath, he would reflect on his creations; the feel of the warm water on his skin helped him think.
One day, while he was testing a lever for an automatic picking mechanism, he met Léa, a textile artist who had come looking for a rare vintage fabric. Fascinated by his creations, she sat down on a chair next to him, ran her fingers over the soft texture of the cotton he held out to her, and listened as he spoke passionately. She noticed his arms, muscular from hard work, and his strong neck; even his elbow resting on the workbench seemed natural and reassuring. Together, they combined their talents: she created silky patterns on flexible fabrics, while he incorporated innovative buttons and cooling systems into them. Their hands often touched as they worked—an electrifying contact that drew them closer. Soon, their collaboration gave rise to a line of interactive textiles. They gradually fell in love, sharing a shy kiss during a smart fabric test. Every surface of their workshop now vibrated with creativity and happiness, and they even transformed an old corner of the workshop into a shared creative space.

<i>Translated with DeepL.com (free version)</i></p>

### Neutral

![Neutral baseline stories](/assets/photos/poster_SNL/group_neutral_baseline_story2.png)

#### French
<p>Un système informatique devait traiter une série d'opérations complexes réparties en plusieurs modules interdépendants. Chaque étape dépendait des résultats de la précédente, ce qui nécessitait une vérification rigoureuse à chaque transition. Les paramètres furent examinés un par un, et les erreurs potentielles soigneusement identifiées et consignées. Des corrections furent apportées au fur et à mesure, en suivant un protocole établi par l'équipe technique. Certaines anomalies nécessitèrent plusieurs cycles de validation avant d'être résolues. Une fois l'ensemble des modules validés, le processus fut lancé automatiquement selon le calendrier prévu. Les résultats obtenus correspondaient aux attentes initiales définies dans le cahier des charges. Un rapport de synthèse fut généré et transmis aux responsables concernés. Le système pouvait désormais fonctionner de manière autonome, sans intervention humaine régulière. Une période de surveillance fut néanmoins maintenue pour garantir la stabilité des opérations sur le long terme.</p>

#### English
<p>A computer system was designed to process a series of complex operations divided into several interdependent modules. Each step depended on the results of the previous one, which required rigorous verification at each transition. The parameters were examined one by one, and potential errors were carefully identified and documented. Corrections were made as the process progressed, following a protocol established by the technical team. Some anomalies required several validation cycles before they were resolved. Once all modules had been validated, the process was launched automatically according to the scheduled timeline. The results obtained met the initial expectations defined in the specifications. A summary report was generated and sent to the relevant managers. The system could now operate autonomously, without regular human intervention. However, a monitoring period was maintained to ensure long-term operational stability.

<i>Translated with DeepL.com (free version)</i></p>



## Validation {#validation}

Stories and sentences were rated by external participants on all four sensorimotor
dimensions, to check that the LSN-based category assignments match human perception.

One figure per dimension:
![Validation](/assets/photos/poster_SNL/validation_1.png)
![Validation](/assets/photos/poster_SNL/validation_2.png)


## Planned analysis {#analysis}

1. **BHA epoch extraction.** Word-locked broadband high-gamma (70–150 Hz, z-scored) extracted from sEEG FIF files using `onset_fif` timestamps. Window: −200 ms to +1000 ms around each word onset.
2. **Feature matrix.** Per valid word (identical status, content word, LSN available): 4 LSN composites (motor, oral, internal, auditory-visual) plus control regressors (surprisal, semantic distance, concreteness, valence). About 355–500 valid words per patient.
3. **Epoched ridge regression.** Per electrode × timepoint: BHA ~ LSN composites, with cross-validated lambda selection (5-fold). Outputs: beta coefficients (n_electrodes × n_timepoints × 4) and cross-validated R².
4. **Statistical thresholding.** FDR correction (Benjamini-Hochberg, α = 0.05) across electrode × timepoint cells. Permutation-based p-values planned for publication.
5. **Visualization.** R² heatmap (electrodes × time), temporal beta profiles per dimension, and peak R² projected onto the MNI brain (native and MNI coordinates from BIDS `electrodes.tsv`).

### Features at each level

| Feature | Word-level | Sentence-level | Story-level |
|---|---|---|---|
| **LSN composites** | Motor / Oral / Internal / Audvis | Mean over content words | Mean over sentences |
| **Surprisal** | CamemBERT or trigram? | Mean or sentence LM prob? | — |
| **Semantic distance** | Cosine to context (FastText / CamemBERT, w = 1/3/5) | CamemBERT CLS cosine | Story embedding cosine |
| **Concreteness** | Brysbaert EN (~40k) / Bonin FR (~2k) | Mean over content words | Mean over sentences |
| **Valence** | FANCat FR (1033 words) | Mean or CamemBERT CLS? | Mean or story embedding? |