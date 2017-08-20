---
title: r1d27 Migration Jekyll vers Hugo
date: 2017-08-20T08:21:00Z
tags: [100daysofcode, gohugo, jekyll]
lastmod: 2017-08-20T08:25:00+02:00
draft: false
---

r1d27 : Migration vers [GoHugo](https://gohugo.io/)

## Jekyll vs Hugo ?

Jekyll est un générateur de site statique incroyable et je ne voudrais en aucun cas le dénigrer dans ce post. Bertrand Keller mon *mentor* statique vous en parlera mieux que moi sur son dernier post ["Jekyll et Hugo sont dans un bateau"](https://bertrandkeller.info/2017/07/03/jekyll-hugo-sont-bateau/). 

![Jekyll build et version Ruby](https://monosnap.com/file/kXoJF1LsSSFVsjamdrTw37klKqc7C4.png)

Mais comme d'autres [utilisateurs plus ou moins néophytes](https://jamstatic.fr/2017/06/07/migration-de-jekyll-a-hugo/), je rencontrais trop souvent des agacements lors des mises à jour de version Jekyll. Les averstissmements et erreurs de build étaient bien trop rebutantes à mon goût pour tenir un flow d'écriture dans l'éditeur markdown.

L'appel GoHugo me démange depuis quelques mois. Les [premiers pas effectués sur un sous-domaine "100daysofcode"](https://100daysofcode.christopheducamp.com/page/thanks) m'ont emballé pour persévérer.

Je continuerai à utiliser Jekyll. Je conserve une instance de famille pour effectuer des tests. Et j'accompagnerai Barbara à la rentrée dans la prise en main de son nouveau site professionnel où Bertrand [nous invite à jongler avec des milliers de photos](http://jekyll-for-craftman.netlify.com/) pour organiser la présentation de ses collections


## Migration "hugo-zen"

Ce qui suit demeure une expérience personnelle de non développeur. Si vous êtes développeur web, vous aurez sûrement de meilleures astuces. Ce qui me fascine dans Hugo -outre la vitesse de "build"- c'est la visualisation live en local du rendu d'affichage durant les modifications de code. Ne plus avoir à rafraîchir la page s'avère à l'usage pratique et très fonctionnel pour l'apprentissage et les itérations de design css.

Encouragé par [matjaz](https://matjaz.it/) dans son post "[Hugo Power User : make it web friendly part 1](https://matjaz.it/hugo-power-user-make-it-web-friendly-1/)", je migre ainsi aujourd'hui avec le thème [hugo-zen](https://github.com/rakuishi/hugo-zen) pour repartir sur des bases simples à itérer.

![terminal : hugo serve](/img/migration-gohugo/hugo-zen-hugo-serve.png)

Ne me sentant pas encore capable de [créer un thème à partir de zéro](https://gohugo.io/categories/themes), ma ligne d'apprentissage est de m'accrocher à ce thème minimaliste et [parvenir à le personnaliser](https://gohugo.io/categories/themes). Le thème "hugo-zen" est basé sur le [framewok Skeleton](http://getskeleton.com/) avec une `custom.css` de moins de 100 lignes. Ce qui me changera du thème "beautiful hugo" (bootstrap) bien trop obèse à mon goût.

## Récap des travaux du jour 

Utilisé la [commande import](https://gohugo.io/commands/hugo_import_jekyll/) `hugo import jekyll`

1. nettoyé quelques front-matter de posts 
2. les photos et images sont désormais posées dans le dossier `static\img`
2. paramétré les `permalinks` dans le fichier de `config.toml` pour conserver la structure des URLs jekyll (format AAAA/MM/JJ.)
3. localisation de la date en français dans les templates 
4. copié tous mes fichiers images provenant de Jekyll dans le dossier `/static` de Hugo.
5. déploiement du site sur [netlify](https://www.netlify.com/)
	6. conservé l'ancien repo
	6. changé de repo github : <https://github.com/ChristopheDucamp/xtof-hugo-zen>

## yeah !

A ce stade, j'apprécie le retour à la vitesse et la simplicité. Tout reste à ranger, mettre en forme.

  




