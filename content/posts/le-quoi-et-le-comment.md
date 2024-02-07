---
title: 'Le Quoi et Le comment'
date: 2024-02-07T23:28:11+01:00
comments:
  host: mastodon.social
  username: johjo
  id: 111892793301822054
---

Lorsqu'on apprend à développer, la première chose que l'on découvre, c'est le **Comment**. On apprend à diriger l'ordinateur en écrivant du code.

C'est un premier pas tout à fait normal dans le monde du développement, et en tant que personne qui développe, c'est notre raison première de savoir le **Comment**.

Mais si l'on ne fait pas attention, on se concentre essentiellement sur le **Comment** et on en oublie le **Quoi**. Et c'est là que l'on commence à tomber dans le piège. Nous perdons le contrôle sur notre code et il devient plus complexe à écrire.

Pour sortir de ce piège, il faut comprendre ce qu'est le **Comment** et ce qu'est le **Quoi**.

## Une histoire d'abstraction

**Abstraction** : tout au long de ma carrière, j'ai vu beaucoup de dev souffrir à cause de ce mot. J'ai demandé à chat GPT une définition de l'abstraction : 

> l'abstraction est le processus de filtrer les informations pour se concentrer sur les aspects plus généraux, essentiels ou conceptuels de quelque chose, en mettant de côté les détails spécifiques.

À partir de cette définition, nous pouvons en extraire les notions de **Quoi** et de **Comment**.

Le **Comment**, ce sont les détails spécifiques.
Le **Quoi**, ce sont les aspects généraux.

Le **Quoi** sert à définir ce que l'on fait et le **Comment** sert à décrire comment on le fait.

Voici un petit exemple dans le cadre de la conduite automobile.

Notre **Quoi** est le fait de conduire une voiture. Notre **Comment**, c'est d'utiliser le volant, le levier de vitesse et les pédales.

## Inception, le quoi peut devenir le comment
Ce qui est intéressant, c'est que le **Quoi** peut devenir le **Comment** tout simplement en changeant de point de vue.

Si l'on reprend la conduite automobile, le fait de *conduire une voiture* est une composante du **Comment** lorsqu'on parle de *partir en vacances au bord de la mer*.

Que fait-on ?
On part en vacances au bord de la mer. Comment ? En conduisant la voiture.

Que fait-on ?
On conduit une voiture. Comment ? En utilisant le volant, les pédales et le levier de vitesse.

Que fait-on ?
On tourne le volant. Comment ? En mobilisant les muscles de nos bras.

Que fait-on ?
On utilise les muscles de notre bras. Comment ? En envoyant des signaux électriques via les nerfs.

Suivant le contexte, le **Quoi** peut devenir le **Comment** et inversement.

Notre cerveau est très doué pour jouer à ce jeu d'abstraction sans que l'on s'en rende compte. Et c'est pour ça que l'on tombe dans le piège.

## Le piège de l'abstraction
Nous n'avons pas conscience que nous manipulons des abstractions à longueur de journée. En permanence, le cerveau nous masque le maximum de détail de notre activité du moment. Il ne laisse dans notre conscience que les éléments qui ont du sens. Tout ça pour nous simplifier la vie.

Lorsqu'on apprend à lire, on commence par distinguer chaque lettre, mais lorsqu'on est habitué, nous ne voyons plus des lettres, ni des mots, mais des phrases.

Le problème, c'est que lorsqu'on développe, on doit indiquer **TOUT** ce que doit faire le système (pas tout à fait, car nos langages sont déjà des abstractions en soi).

Et là, notre cerveau n'est pas habitué à cette gymnastique. Il pose tout au même niveau d'abstraction. En fait, on ne perçoit que le **Comment**.
Qu'en est-il du **Quoi** ? Il est bien dans notre tête, mais il n'apparait pas dans notre code.

Cela pose problème car tout se mélange. Dans le même bloc de code, on peut se retrouver à parler de choses qui n'ont pas la même abstraction. 

On peut parler de *vacances au bord de la mer* et de *levier de vitesse*. Dis comme cela, ces deux notions n'ont aucun lien, mais si on a en tête les différents niveau d'abstraction des exemples cités plus haut, alors, on fait le lien.

Si l'on ne fait pas attention au niveau d'abstraction, on mélange dans le code des notions qui n'ont rien à voir. Dans ce cas, le risque de perdre le contrôle sur notre code augmente. Il est plus dur à écrire, à comprendre, à maintenir.

C'est pour cela que la maîtrise du **Quoi** et du **Comment** est primordial. Il nous permet de mieux gérer ces différents niveaux d'abstractions.

## Quels outils à disposition ? 
Heureusement, nous avons à disposition deux outils très simple pour créer des abstractions : Les **variables** et les **fonctions**.

Le nom de la variable ou de la fonction peut exprimer le **Quoi** et la valeur de la variable ou le contenu de la fonction peut exprimer le **Comment**.

La fonction est plus pratique car elle permet de masquer le contenu, contrairement à la variable qui doit rester très proche de sa valeur.

## Pour finir
Il est primordial d'apprendre à distinguer les différents niveaux d'abstractions et à ne pas les mélanger.

Sans cette compétence, le code que l'on écrit risque d'être compliqué à maintenir et à faire évoluer.

S'y habituer le plus rapidement possible, c'est se simplifier la vie pour les dizaines de milliers d'heures que nous allons passer à coder.