---
title: 'Ma définition de TDD'
date: 2024-01-04T06:39:53+01:00
draft: false
comments:
  host: mastodon.social
  username: johjo
  id: 111705975316853471
---
## Introduction

Dans ce blog, je vais essentiellement parler du Test Driven Development ou TDD. Malheureusement, plus cette méthode est utilisée et plus le nombre de définitions augmente.

Cette page va me servir pour te donner MA définition de TDD. Elle sera un pré-requis dans la lecture du blog.

## Définition générale

Les deux notions suivantes sont la base de ma définition de TDD. Il s'agit de Red - Green - Refactoring et des 3 lois de TDD. Je vais d'abord les présenter d'un point de vue général, et ensuite, j'expliquerai ma vision des choses.

### Red - Green - Refactoring

![Le cycle TDD - Red - Green - Refactoring](/blog/images/CycleTDD.png)

Le cycle TDD est constitué de 3 étapes : Red - Green - Refactoring, représentées par des cercles dans le schéma. On voit qu'il y a aussi deux états : Red et Green. Ces deux états, nommés comme les étapes peuvent poser des incompréhensions. J'utiliserai donc à la place les termes : *Tous les tests passent* (Green) et *Un seul test échoue* (Red).

On entre dans l'étape *Red* lorsqu'on est dans l'état *Tous les tests passent*. L'objectif est de passer le plus rapidement possible à l'état *un seul test échoue*. Dans cette étape, on n'écrit du code que dans le test. On passe à l'étape suivante lorsqu'on a un test qui échoue (et un seul doit échouer puisqu'on n'a écrit que du code de test).

On arrive alors dans l'étape *Green*. On peut entrer dans cette étape seulement si on est dans l'état *un seul test échoue*. L'objectif est de passer le plus rapidement possible à l'état *Tous les tests passent*. Quand je dis rapidement, c'est vraiment le plus rapidement possible, de la manière la plus naïve possible. L'idéal étant d'écrire le moins de code possible. On peut passer à l'étape suivante lorsque tous les tests passent.

Et arrive enfin la dernière étape, celle du *Refactoring*. On peut y rentrer seulement si on est dans l'état *Tous les tests passent*, et là, l'objectif, c'est de ne jamais sortir de cet état.

Une fois dans cette étape, il n'est plus question de se hâter. Au contraire, le temps s'est arrêté et on peut essayer de faire les choses du mieux que l'on peut. On améliore le code. On supprime le code que l'on peut supprimer. On fait les choses bien. Et lorsqu'on pense avoir fait tout ce qu'il y a à faire, on peut recommencer le cycle et passer à l'étapre *Red*.

J'associe tout le temps le cycle Red - Green - Refactoring aux 3 lois de TDD, car celles-ci apportent un complément d'information sur la signification de l'état *Un seul test échoue*.

### Les 3 lois de TDD

En effet, qu'est-ce que l'on entend par le fait qu'un test échoue ? Pour le savoir, examinons ces 3 lois. Il existe plusieurs versions, plus ou moins proche. A toi de voir celle qui te correspond le mieux.  

1. You must write a failing test before you write any production code.
2. You must not write more of a test than is sufficient to fail, or fail to compile.
3. You must not write more production code than is sufficient to make the currently failing test pass.

Ou en français : 

1. Tu dois écrire un test qui échoue avant d'écrire du code de production.
2. Tu ne dois pas écrire plus d'un seul test qui échoue. L'échec de compilation est considéré comme un échec du test.
3. Tu ne dois pas écrire plus de code de production que nécessaire pour faire passer le test.

Ces 3 lois nous apportent donc la précision sur ce que l'on considère l'état : *Un seul test échoue*. On entre dans cet état dès le moment où on constate qu'il y a quelque chose qui ne fonctionne pas : 
- On rencontre une erreur de compilation ? On passe à la phase *Green*.
- Notre code rencontre une exception ? On passe à la phase *Green*.
- Notre code ne renvoit pas le résultat attendu ? On passe à la phase *Green*.

Elles nous apportent aussi de la précision sur la durée de l'étape *Green*. On écrit seulement le code suffisant pour repasser dans l'état *Tous les tests passent*.

Avec le cycle Red - Green - Refactoring et les 3 lois de TDD, tu as tout ce qu'il faut pour te lancer dans TDD.

C'est ce que j'applique tous les jours, mais je te propose de pousser la vision un peu plus loin.

## Ma vision

Je challenge régulièrement le concept du cycle Red - Green - Refactoring. Si tu as déjà échangé avec moi, tu constateras que je l'ai formulé de plusieurs manières différentes, j'ai créé des schémas du cycle avec plus d'étapes, plus d'états. Mais je reste quand même très fortement attaché aux deux concepts que l'on a vu plus haut.

### La véritable essence de TDD

#### Focus sur une seule chose

Pour moi, TDD est une silver bullet car je l'utilise au quotidien, même quand je ne code pas. Et lorsque je code, je considère que je fais du TDD, même si je n'utilise pas de tests automatiques. Pour arriver à cette vision, j'ai reformulé le cycle TDD sous une autre forme : 

- *Red* : je constate qu'il y a quelque chose qui ne convient pas. S'il y a plusieurs choses qui ne conviennent pas, j'en choisi une et j'ignore les autres.
- *Green* : j'effectue l'action qui me permettra de constater que tout convient (à l'exception de ce que j'ignore).
- *Refactoring* : j'améliore les choses en vérifiant que tout fonctionne (à l'exception de ce que j'ignore).

Cette vision me permet d'être minimaliste et d'être focus sur une seule chose à la fois. Il existe des cas où cela n'est pas possible, mais la plupart du temps, ne faire qu'une seule chose à la fois me permet d'être plus efficace que d'en faire plusieurs.

Et c'est là toute la force de TDD, c'est une méthode qui permet de se concentrer sur un seul problème à la fois. Et cela permet de prendre son temps pour faire les choses correctement. Il est plus simple de jongler avec une seule balle qu'avec deux.

TDD est donc un processus de développement **itératif**.

Je reviens sur l'étape du *red*, cette étape où l'on constate que quelque chose ne convient pas. Il y a tout le temps plein de choses qui ne conviennent pas. Il y en aura toujours. Et c'est une bonne chose, car sans ce constat, il n'y aurait pas d'action. Mais comment savoir quelle est la chose à faire ? 

Et bien, à moins de savoir lire le futur, c'est impossible. C'est pourquoi j'applique la stratégie des baby steps lorsque je fais du TDD. 

#### Baby step

En français, on peut traduire les *baby steps* par *petits pas*.

Imaginons que je veuille faire une marche en partant de chez moi (Valence) pour aller à Paris. Je n'ai qu'une seule chose à faire, aller d'un point A à un point B. Mais il y a environ 537 kilomètre. Ce n'est pas possible de le faire. En fait, pour faire cette marche, et en simplifiant, je devrais faire environ 800000 pas 😅. Choisir les bons devient très important, car si je ne vais pas dans la bonne direction, je peux me retrouver en Italie. de plus, je ne peux pas faire n'importe quel pas, je ne peux faire que ceux qui partent de mon emplacement actuel.

Je vais faire la même chose lorsque j'écris du code. Je vais partir de mon code actuel et essayer de déterminer quelle est la prochaine modification à apporter.

Cependant, je ne pars pas du code de production (mais on peut s'en inspirer) mais du code de test. Mon prochain *pas* débute donc à l'étape *Red*. Si je reviens sur l'exemple de la marche vers Paris, je constate que je ne suis pas arrivé à Paris, alors, je me fixe le prochain objectif qui va m'en rapprocher. Je décide donc du pas qui va me rapprocher de ma destination. 

Dans le code, c'est pareil. J'écris le prochain test qui va me permettre d'avancer. Il doit me mener de ma situation actuelle à l'étape juste après.

Puis je passe à la phase *Green*. Dans le cas de la marche, c'est effectuer le pas que je viens de décider. Dans le cas du développement, c'est écrire le petit bout de code qui va me permettre de passer à l'état *Tous les tests passent*.

Avec cette approche, on constate que TDD est aussi un processus de développement **incrémental**.

Maintenant que j'ai expliqué ce qu'est TDD pour moi, je vais aborder ce qu'il n'est pas pour moi.

### Ce n'est pas une méthode de test
TDD ne sert pas à tester son code. C'est un processus d'écriture du code. 

Mais vu qu'il a une excellente synergie avec les tests automatiques, c'est un heureux hasard qu'il nous aide la plupart du temps à produire des tests automatiques.

Faire du TDD et savoir écrire des tests sont deux compétences différentes. Elles sont complémentaires, certes, mais elles sont différentes.

Contrairement à TDD, la compétence *Savoir écrire des tests* nécessite une expérience plus approfondie.

### Ce n'est pas une méthode de design
Je ne considère pas TDD comme une méthode de design de code. Pourquoi ? Tout simplement parce que si une personne ne sait pas designer du code, TDD ne lui sera pas d'un grand secours.

Le design de code est une compétence à part entière. Elle aussi a une excellente synergie avec TDD. Pourquoi ? Tout simplement parce que TDD permet de prendre son temps, de ralentir le temps au moment où l'on prend des décisions.

La compétence *savoir écrire des tests automatiques* fonctionne aussi en synergie avec la compétence de design.

Comme elle, la compétence *design du code* est complexe à acquérir. 

### TDD, simple à apprendre, difficile à maîtriser
Au final, si on se réfère à ma vision, je pense que TDD est assez simple à apprendre. Il suffit de suivre un cycle assez bien documenté et 3 lois assez explicites.

Les freins que je vois à l'acquisition de TDD sont les suivants : 
- on pense qu'on ne peut pas faire de TDD sans avoir toutes les compétences annexes (design, refactoring, testing, etc...)
- on a peur de perdre du temps en prenant le temps de bien faire les choses, car effectivement, l'un des enjeux de TDD, c'est de pouvoir ralentir le temps.

Il y a cependant une difficulté, mais elle n'est pas un frein, c'est l'aspect incrémental de TDD. Choisir le bon baby step est très compliqué. C'est l'expérience qui te permettra de choisir le bon. Mais faire un pas trop gros n'empêche pas de faire du TDD, cela fait juste perdre du temps.

Je finirai donc avec cette phrase : 

> TDD est simple à apprendre, difficile à maîtriser...

J'encourage vivement les personnes qui souhaite acquérir cette compétence à la pratiquer dès maintenant. Même si l'approche est naïve, mal exécutée, sans test, l'approche itérative et incrémentale de TDD t'aidera dans tes projets de développement. Avec le temps et l'expérience, tu pourras commencer à y intégrer des tests automatiques, pratiquer un meilleur refactoring, etc...

Voilà, tu connais ma vision de TDD. Tous les articles que j'écrirais à ce sujet se baseront sur celui-ci. Je le complèterai au fur et à mesure que je verrai des points apparaître.

Si tu as des questions ou des remarques sur le sujet, je me ferai une joie d'échanger avec toi.

---
## Référence
- https://www.les-traducteurs-agiles.org/2015/01/06/les-cycles-du-developpement-pilote-par-les-tests.html
- http://blog.cleancoder.com/uncle-bob/2014/12/17/TheCyclesOfTDD.html

