# Cours | [ChatGPT Prompt Engineering for Developers](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/)

[English](../en/README.md) | **Français** | [Português](../pt/README.md)

<img src="../images/ChatGPT_curso_prompting.png" alt="Image créée par des outils Text-2-Image" title="Image créée par des outils Text-2-Image">

- **Crédit**: [DeepLearning.AI](https://www.deeplearning.ai) et [OpenAI](https://openai.com/)
- **Auteur de cette page**: [Pierre Guillou](https://www.linkedin.com/in/pierreguillou)
- **Date**: 9 juin 2023
- **Blog post**: [IA Generativa | Como controlar o ChatGPT para escrever um texto que atenda às suas expectativas (curso de DeepLearning.AI e OpenAI)](https://medium.com/@pierre_guillou/ia-generativa-como-controlar-o-chatgpt-para-escrever-um-texto-que-atenda-%C3%A0s-suas-expectativas-e1b7abe59012)
- **Contexte**: Ce cours créé à l'origine pour les développeurs enseigne les principes et tactiques à utiliser pour contrôler ChatGPT, c'est-à-dire l'amener grâce à une instruction en langage naturel à rédiger un texte qui répond à vos attentes. Cependant, puisqu'il s'agit essentiellement d'apprendre à parler à ChatGPT et qu'il est possible de le faire sans aucun code (c'est-à-dire dans une interface Web), il m'a semblé que tout le monde pouvait bénéficier de ce cours. Ainsi, j'ai décidé de résumer chacun de ses chapitres et de lister les points clés mis en avant par les formateurs Isa Fulford (OpenAI) and Andrew Ng (DeepLearning.AI). En plus des anglophones, j'ai également décidé de faciliter son accès aux francophones et aux lusophones avec des versions traduites dans leurs langues respectives. 
- **Réalisation**: Alors, comment faire tout cela le plus rapidement possible ? Bien sûr, j'ai travaillé avec un assistant... du nom de [ChatGPT 4](https://openai.com/gpt-4). A l'aide de mon compte personnel sur OpenAI, j'ai demandé à ChatGPT de résumer les retranscriptions textuelles de chacune des vidéos du cours, d'en extraire les point-clés sous forme d'une liste, puis de traduire ses réponses textuelles (les instructions utilisées se trouvent en annexe). J'ai ensuite fait une relecture des textes et éventuellement fait quelques retouches quand je l'ai jugé nécessaire (rien d'essentiel). Enfin, j'ai intégré tous les textes dans github.
- **Note**: Les transcriptions textuelles et les notebooks sont mis à disposition via des liens pour permettre à chacun de sourcer les informations de cette page et faciliter leur mise en œuvre. En revanche, il faut s'inscrire sur la page du cours pour visionner les vidéos.

## Sommaire

- [Leçon 1 - Introduction](#leçon-1---introduction)
- [Leçon 2 - Principes et tactiques](#leçon-2---principes-et-tactiques)
- [Leçon 3 - Instruction interactive](#leçon-3---instruction-interactive)
- [Leçon 4 - Résumé et extraction d'informations](#leçon-4---résumé-et-extraction-dinformations)
- [Leçon 5 - Inférence (classification, détection de thématiques, extraction d'informations)](#leçon-5---inférence-classification-détection-de-thématiques-extraction-dinformations)
- [Leçon 6 - Transformations](#leçon-6---transformations)
- [Leçon 7 - Assistant](#leçon-7---assistant)
- [Leçon 8 - ChatBot](#leçon-8---chatbot)
- [Leçon 9 - Conclusion](#leçon-9---conclusion)
- [Annexe](#annexe)

## Leçon 1 - Introduction

<img src="../images/lesson1/DeepLearning_course_ChatGPT_video1.png" width="400">

- **Ressource**: [transcription 1](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/transcripts/transcript_video1.txt)

- **Résumé**: Ce cours offre un guide complet sur l'ingénierie des instructions ChatGPT pour les développeurs. Il couvre les meilleures pratiques pour le développement de logiciels utilisant les grands modèles linguistiques (LLMs), y compris l'utilisation d'appels API pour la construction d'applications. Il différencie les LLMs de base et les LLMs accordés aux instructions, mettant en évidence les avantages et les applications de ces dernières. Le cours illustre également l'importance des instructions claires et spécifiques lors de l'utilisation de ces modèles.
- **Points clés**: 
  - Le cours est co-animé par Isa Fulford, membre du personnel d'OpenAI, qui a une expérience significative avec les Grands Modèles Linguistiques (LLMs) et l'enseignement des techniques de prompt, ainsi que par Andrew Ng, professeur de Deep Learning à l'université de Stanford et créateur de DeepLearning.AI.
  - Il met l'accent sur le pouvoir sous-estimé des LLMs pour les développeurs pour construire rapidement des applications logicielles en utilisant des appels API.
  - Le programme couvrira les meilleures pratiques pour le prompting (stratégie d'instructions), des cas d'utilisation communs (tels que la résumé, l'inférence, la transformation, l'expansion) et des applications pratiques comme la construction d'un chatbot en utilisant un LLM.
  - Le cours fait la différence entre deux types de LLMs: les LLMs de base qui prédisent le mot suivant en fonction des données d'entraînement de texte, et les LLMs accordés aux instructions qui suivent des instructions spécifiques.
  - Les LLMs accordés aux instructions sont préférés en raison de leur capacité à suivre des instructions, et leurs caractéristiques de sécurité qui les rendent moins susceptibles de produire des sorties toxiques.
  - Le cours souligne l'importance d'instructions claires et spécifiques pour de meilleurs résultats d'un LLM accordé aux instructions.
  - Un certain nombre de contributeurs d'OpenAI et de DeepLearning.AI ont joué un rôle significatif dans la création des matériaux du cours.

## Leçon 2 - Principes et tactiques

<img src="../images/lesson2/DeepLearning_course_ChatGPT_principles12.png" width="400">

- **Ressources**:
  - [transcription 2](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/transcripts/transcript_video2.txt)
  - [l2-guidelines.ipynb](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/notebooks/l2-guidelines.ipynb)

- **Résumé**: Dans ce cours, Isa discute des directives pour une invitation efficace avec les modèles de langage, avec un accent sur la clarté et la spécificité des instructions et le temps accordé au modèle pour traiter des tâches complexes. De plus, elle introduit des tactiques pratiques comme l'utilisation de délimiteurs, les demandes de sortie structurée, la vérification d'instructions, et l'apprentissage para le modèle à partir de quelques exemples. Les leçons sont illustrées par des exemples d'instructions impliquant des tâches comme le résumé et la traduction de textes, ainsi que la résolution de problèmes mathématiques. La section se termine en annonçant la prochaine leçon, traitant du processus de développement itératif d'instructions.

- **Principe 1**: **Rédiger des instructions claires et spécifiques**
  - **Objectif**: Fournir des directives explicites et claires pour guider le modèle vers la sortie souhaitée et réduire les réponses non pertinentes ou incorrectes. Attention: instructions claires ne veut pas dire courtes.
  - **Tactiques**:
    1. **Utilisation de délimiteurs**: Indiquer clairement les parties distinctes de l'entrée avec des signes de ponctuation ou des symboles spécifiques pour aider le modèle à mieux comprendre l'instruction. Vous pouvez utiliser les délimiteurs suivants par exemple: ```, """, < >, <tag> </tag>
    2. **Demander une sortie structurée**: Cela peut faciliter l'analyse des sorties du modèle, en demandant des sorties structurées comme HTML ou JSON, ou même une liste.
    3. **Vérification de condition**: Instruire le modèle pour vérifier d'abord les hypothèses, aidant à éviter les erreurs et les résultats inattendus. Lui demander une sortie différente si la condition est vérifiée ou non.
    4. **Invitation à s'inspirer de quelques exemples**: Fournir des exemples de réussite d'exécutions de tâches pour guider la compréhension du modèle de la tâche requise.

- **Principe 2**: **Aider le modèle à réfléchir**
  - **Objectif**: Pour des tâches complexes, aider le modèle à "réfléchir" peut éviter des conclusions incorrectes précipitées. Cela implique d'instruire le modèle pour qu'il consacre plus d'efforts de calcul à la tâche.
  - **Tactiques**:
    1. **Spécification des étapes pour les tâches**: Détailler les étapes pour que le modèle puisse accomplir une tâche peut améliorer ses performances et garantir qu'il retourne le résultat souhaité. Le cours a démontré cela avec une tâche impliquant la résumé, la traduction, l'extraction de noms et la sortie JSON (après avoir listé de manière chronologique les tâches, indiquer au modèle le format de sa sortie).
    2. **Demander au modèle de trouver ses propres solutions**: Le modèle d'IA peut être guidé pour raisonner les solutions de manière indépendante avant d'évaluer les solutions des autres. Le cours a démontré cela avec un problème de mathématiques, où le modèle a pu identifier une erreur dans la solution d'un étudiant seulement lorsqu'il a été invité à résoudre le problème lui-même en premier.

**Limites du modèle**: **"Hallucinations"**
- Le cours met en garde contre une limite où le modèle peut générer des réponses plausibles mais fabriquées, connues sous le nom de "hallucinations". Un exemple a été montré où le modèle a été invité à décrire un modèle de brosse à dents inexistant et a donné une description réaliste mais inventée.
- Pour minimiser les hallucinations, le modèle peut être invité à trouver des citations pertinentes dans un texte et utiliser ces citations pour répondre à des questions. Cette approche peut aider à retracer la réponse au document source, fournissant une réponse plus fiable.

## Leçon 3 - Instruction interactive

<img src="../images/lesson3/DeepLearning_course_ChatGPT_video3.png" width="400">

- **Ressources**:
  - [transcription 3](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/transcripts/transcript_video3.txt)
  - [l3-iterative-prompt-development.ipynb](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/notebooks/l3-iterative-prompt-development.ipynb)

- **Résumé**: Andrew souligne l'importance du développement itératif de l'instruction lors de l'utilisation de grands modèles de langage. Il n'est pas crucial qu'une instruction fonctionne parfaitement la première fois. C'est l'amélioration de l'instruction en fonction des résultats qui est la clé du succès. Andrew utilise l'exemple de la génération d'un résumé pour une fiche technique de chaise, affinant l'instruction pour répondre à différentes contraintes comme la longueur, le détail technique, et le format du texte produit para ChatGPT. L'importance de tester les instructions sur des ensembles de données plus importants à mesure que les applications mûrissent est également soulignée.

- **Points clés**:
  - Le développement d'instructions efficaces pour les grands modèles de langage est un processus itératif.
  - L'instruction parfaite n'est généralement pas atteinte lors de la première tentative, mais plutôt elle s'améliore au fil du temps en fonction des exigences de l'application et des résultats précédents.
  - Un exemple a été donné de raffinement d'une instruction pour générer un résumé d'une fiche technique de chaise, ajustant pour des facteurs tels que le décompte des mots, l'inclusion de détails techniques, et le format de sortie (ici, le HTML).
  - Il a été noté que les grands modèles de langage peuvent parfois avoir du mal avec les instructions pour des décomptes de mots ou de caractères très précis, mais ce n'est pas le cas de ChatGPT qui est plutôt fiable sur ce sujet.
  - À mesure que les applications deviennent plus matures, il peut être bénéfique d'évaluer et d'affiner les instructions par rapport à de plus grands ensembles d'exemples pour assurer une performance constante dans divers cas d'utilisation.
  - Le processus de développement d'instruction est important, sinon plus, que de connaître l'instruction parfaite. Il s'agit d'avoir un bon processus pour développer des instructions efficaces pour des applications spécifiques.

## Leçon 4 - Résumé et extraction d'informations

<img src="../images/lesson4/DeepLearning_course_ChatGPT_video4.png" width="400">

- **Ressources**:
  - [transcription 4](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/transcripts/transcript_video4.txt)
  - [l4-summarizing.ipynb](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/notebooks/l4-summarizing.ipynb)

- **Résumé**: Andrew discute de l'utilité des grands modèles de langage dans le résumé de textes, en particulier les avis sur un site de commerce électronique. Il démontre comment ces modèles peuvent générer des résumés ou extraire des informations spécifiques pertinentes pour différents départements (comme l'expédition ou la tarification), facilitant ainsi un processus de révision plus efficace et ciblé. Un code est également introduit pour résumer efficacement plusieurs avis, permettant un accès rapide à leur contenu.

- **Points clés**:
  - Les grands modèles de langage peuvent être utilisés pour résumer de grands volumes de texte, permettant une compréhension efficace du contenu.
  - Un résumé spécifique peut être généré en fonction des exigences de différents départements, par exemple l'expédition ou la tarification, grâce à des instructions adaptées.
  - Andrew a introduit le concept d'extraction d'informations spécifiques plutôt que de fournir un résumé général, ce qui pourrait être plus approprié pour certains départements.
  - Une mise en œuvre pratique d'un code de résumé de plusieurs avis a été montré, permettant un accès rapide à l'essence de plusieurs avis.
  - Les grands modèles de langage aident non seulement à résumer, mais pourraient également aider à faire des inférences à partir de textes, comme déterminer le sentiment positif ou négatif dans les avis sur les produits, qui sera discuté dans la prochaine session.

## Leçon 5 - Inférence (classification, détection de thématiques, extraction d'informations)

<img src="../images/lesson5/DeepLearning_course_ChatGPT_video5.png" width="400">

- **Ressources**:
  - [transcription 5](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/transcripts/transcript_video5.txt)
  - [l5-inferring.ipynb](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/notebooks/l5-inferring.ipynb)

- **Résumé**: Andrew discute de la manière dont les grands modèles de langage peuvent être utilisés pour déduire diverses informations à partir d'un texte, comme le sentiment, les expressions d'émotions, ou pour extraire les détails sur les produits ou les marques, la détection de sujet, et comment ils peuvent gérer plusieurs tâches simultanément à l'aide d'une instruction codifiée. Il explique en outre les applications de ces modèles pour les critiques de clients, l'identification de caractéristiques spécifiques dans un texte, et l'apprentissage zéro-shot pour la détection de sujets dans les articles de presse.

- **Points clés**:
  - Les grands modèles de langage peuvent effectuer diverses tâches inférentielles comme l'analyse des sentiments, l'extraction de noms, de labels, et la compréhension du contexte en utilisant de simples instructions textuelles.
  - Les modèles peuvent traiter et fournir une analyse sur une chaîne de texte de manière plus efficace et rapide par rapport au flux de travail traditionnel de l'apprentissage automatique qui nécessite des modèles séparés pour différentes tâches.
  - En utilisant des instructions spécifiques, les modèles peuvent non seulement classer le sentiment d'une critique, mais aussi identifier la liste des émotions exprimées et évaluer si un client est particulièrement contrarié. Ces informations peuvent être précieuses pour les organisations de support client.
  - L'extraction d'informations est une autre capacité importante des grands modèles de langage qui peut être utilisée pour extraire et résumer des informations clés comme le produit et le fabricant à partir d'une grande collection de critiques.
  - Les grands modèles de langage peuvent également gérer des instructions multitâches, en extrayant plusieurs champs d'une chaîne de texte en une seule instruction, ce qui permet d'économiser du temps et des ressources de traitement.
  - Ces modèles peuvent inférer des sujets à partir d'un grand morceau de texte, ce qui les rend utiles pour analyser et catégoriser de grands corps de texte comme les articles de presse.
  - L'apprentissage zéro-shot permet au modèle d'identifier quels sujets d'une liste prédéfinie sont abordés dans un texte donné sans aucune donnée d'entraînement spécifique.
  - Les grands modèles de langage peuvent rapidement construire plusieurs systèmes pour les inférences de texte qui auraient auparavant pris un temps considérable même pour des développeurs expérimentés en apprentissage automatique.

## Leçon 6 - Transformations

<img src="../images/lesson6/DeepLearning_course_ChatGPT_video6.png" width="400">

- **Ressources**: 
  - [transcription 6](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/transcripts/transcript_video6.txt)
  - [l6-transforming.ipynb](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/notebooks/l6-transforming.ipynb)

- **Résumé**: Isa présente plusieurs capacités des grands modèles linguistiques, en particulier GPT-4, notamment la traduction de texte, la transformation de ton, les corrections d'orthographe et de grammaire, et les conversions de format. Elle montre comment utiliser GPT-4 dans des tâches de traduction à travers diverses langues et niveaux de formalité, introduit le concept de transformation de ton dans l'écriture, et montre les capacités de relecture. De plus, elle montre la conversion de données d'un format (JSON) à un autre (HTML).

- **Points clés**:
  - Les grands modèles linguistiques peuvent traduire du texte à travers plusieurs langues, y compris des versions informelles et formelles.
  - Ils peuvent détecter la langue d'un texte donné, utile dans un environnement multilingue comme une entreprise de commerce électronique multinationale.
  - Les modèles peuvent modifier le ton du texte écrit, comme transformer l'argot en langage commercial.
  - Ils peuvent convertir les données entre différents formats (par exemple : JSON en HTML).
  - GPT-4 peut aider à relire et à corriger les erreurs de grammaire et d'orthographe dans le texte.
  - GPT-4 peut également aider à transformer le texte pour qu'il s'adapte à certains styles et formats, tels que le style APA et le format markdown.

## Leçon 7 - Assistant

<img src="../images/lesson7/DeepLearning_course_ChatGPT_video7.png" width="400">

- **Ressources**: 
  - [transcription 7](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/transcripts/transcript_video7.txt)
  - [l7-expanding.ipynb](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/notebooks/l7-expanding.ipynb)

- **Résumé**: Isa discute des utilisations variées des grands modèles de langage, notamment pour la traduction entre différentes langues et formats, la correction orthographique et grammaticale, le changement de ton, et l'expansion du texte. Elle décrit également comment améliorer les instructions pour le modèle afin d'obtenir des résultats plus précis et comment créer un assistant de service à la clientèle AI pour répondre aux avis des clients.

- **Points clés**: 
  - Les grands modèles de langage peuvent traduire du texte entre différentes langues et formats, et peuvent aider à la correction orthographique et grammaticale.
  - Avec une instruction appropriée, le modèle peut changer le ton d'un texte pour l'adapter à différents publics.
  - Les modèles de langage peuvent être utilisés pour transformer des textes courts en textes plus longs, utiles pour générer du contenu plus détaillé à partir de prompts.
  - Le modèle peut être utilisé comme un assistant de service à la clientèle AI pour générer des réponses personnalisées aux avis des clients.
  - Le paramètre de température peut être utilisé pour contrôler le degré d'exploration ou de variabilité dans les réponses du modèle.
  - Il est important d'itérer et d'ajuster les instructions pour obtenir des résultats plus précis.
  - Il est crucial de faire preuve de transparence lorsque l'IA génère du texte destiné aux utilisateurs, en leur faisant savoir que le texte a été généré par un modèle de langage.

## Leçon 8 - ChatBot

<img src="../images/lesson8/DeepLearning_course_ChatGPT_role.png" width="400">

- **Ressources**: 
  - [transcription 8](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/transcripts/transcript_video8.txt)
  - [l8-chatbot.ipynb](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/notebooks/l8-chatbot.ipynb)

- **Résumé**: Isa aborde la manière d'utiliser un modèle de langage large pour construire un chatbot personnalisé. Elle explique le format OpenAI ChatCompletions, le rôle des messages système et utilisateur, ainsi que l'importance de fournir du contexte au modèle pour générer des réponses précises. Elle présente des exemples d'utilisation du chatbot pour différentes tâches, telles que la génération de blagues shakespeariennes et la collecte de commandes de pizza. Le transcript couvre également le processus de création d'une interface utilisateur et l'ajout de messages au contexte de la conversation. Enfin, elle montre comment générer un résumé JSON basé sur la conversation pour un traitement ultérieur.

- **Points clés**:
  - Les modèles de langage large peuvent être utilisés pour construire des chatbots personnalisés pour diverses tâches.
  - Le format de chat implique l'utilisation d'une liste de messages, comprenant des messages système et utilisateur.
  - Les messages système aident à définir le comportement et la personnalité de l'assistant sans que l'utilisateur en soit conscient.
  - Fournir du contexte est crucial pour que le modèle génère des réponses précises.
  - Une interface utilisateur peut être créée pour interagir avec le chatbot et collecter les requêtes de l'utilisateur.
  - Les conversations peuvent être étendues en ajoutant des messages au contexte.
  - Le modèle peut générer des résumés JSON basés sur la conversation pour un traitement ultérieur.
  - La personnalisation du comportement et de la personnalité du chatbot peut être réalisée en modifiant le message système.

## Leçon 9 - Conclusion

<img src="../images/lesson9/DeepLearning_course_ChatGPT_conclusion.png" width="400">

- **Ressources**: 
  - [transcription 9](https://github.com/piegu/language-models/edit/master/chatgpt/deeplearning_ai_chatgpt_prompt_engineering_course/transcripts/transcript_video9.txt)

- **Résumé**: Isa et Andrew concluent ce court cours sur les techniques de formulation de requêtes et qui met en évidence deux principes clés : rédiger des instructions claires et spécifiques, et laisser le modèle le temps de réfléchir. Ils soulignent l'importance du développement itératif des requêtes et d'explorer les différentes capacités des grands modèles de langage, tels que la synthèse, l'inférence, la transformation et l'expansion. Ils encouragent les apprenants à explorer leurs propres idées de projet, à commencer par de petits projets et à améliorer progressivement leurs compétences. L'utilisation responsable des outils d'IA est mise en avant, et les créateurs du cours expriment leur enthousiasme pour le potentiel du domaine. La transcription se termine par des remerciements et une invitation à partager les projets réalisés.

- **Points clés**: 
  - Deux principes clés pour la formulation de requêtes : des instructions claires et le temps accordé au modèle pour réfléchir.
  - L'importance du développement itératif des requêtes pour trouver la bonne approche pour des applications spécifiques.
  - Différentes capacités des grands modèles de langage, tels que la synthèse, l'inférence, la transformation et l'expansion.
  - Encouragement à explorer ses propres idées de projet, même en commençant par de petits projets ou des projets ludiques.
  - L'excitation et le potentiel de croissance liés à la création d'applications avec les grands modèles de langage.
  - L'importance de l'utilisation responsable des outils d'IA, en mettant l'accent sur l'impact positif.
  - Invitation à partager et à faire connaître le cours ainsi que les projets réalisés.

## Annexe

### Instruction 1

```
You are a course teacher. 
Summarize the transcript delimited by triple quotes at most 80 words. 
Then, extract the most important points of the transcript as a list with a short explanation if necessary.

Follow the following format:
Summary: <summary of the transcript>
Key points: <most important points of the transcript as a list>
- ...
- ...
- ...

Transcript:
"""
<transcript>
"""
Summary: 
Key points:
```

### Instruction 2
```
Translate the summary and key points into French and Portuguese.
```

### Instruction 3 (quand nécessaire)
```
Keep writing until the translation is finished.
```
