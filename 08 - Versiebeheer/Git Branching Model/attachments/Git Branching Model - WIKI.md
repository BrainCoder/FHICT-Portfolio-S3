# Git Branching Model

Om de manier waarop we git gebruiken te standaardiseren en professionaliseren gaan we gebruik maken van gitflow.

Gitflow is een workflow geoptimaliseerd voor software waarbij er naar een release toe gewerkt wordt en er meerdere versies van de software kunnen voorkomen in productie.

## Meet the brances

**develop** Deze branch is de werk versie van het project waar alle feature branches op gebaseerd worden.

**feature/** In deze brances word een nieuwe feature toegevoegt die waneer hij af is gemergd wordt met develop.

**release/** In deze branches wordt een release candidate afgesplitst van develop en wordt er een build gemaakt ook word de feedback van de klant nodig voor release hier verwerkt.

**master** In deze branch staan de uiteindelijke release versies

**hotfix/** In deze brances worden breaking bugs in al gereleasde firmware opgelost deze worden dan meteen gemerged naar master voor een nieuwe release.

![[gitflow.png]]

## Develop & Master branches

In plaats van 1 enkele master branch maken we in onze gitflow gebruik van een losse master en develop branch.

De master branch is bedoelt voor het bijhouden van de releases die bedoelt zijn voor gebruik in productie terwijl de develop branch dient als integratie punt van de nieuwe features.

Op zowel de master als de develop branch horen write protected te zijn want het is niet de bedoeling direct naar deze branches te pushen.

## Feature branches

In feature branches gaan we je raad het al features implementeren. Het is hierbij de bedoeling dat elke feature in een losse feature branch komt te staan.

Deze feature branches worden afgesplitst van develop zodat je het goed kunt integreren met alle andere features die al af zijn. Wanneer je feature klaar is kan deze terug gemerged worden naar develop.

Vergeet niet dat alle bugs eigenlijk features zijn dus tenzij hij extreem dringent is (zie hotfix) kun je hier een feature branch voor aanmaken.

## Hotfix branches

Omdat er soms een makelijk op te lossen maar kritieke fout in een release zit het niet mogelijk is direct naar master te commiten hebben we hotfix branches.

Deze branches zijn alleen voor wijzegingen die zo kritiek zijn dat ze niet de voledige build test release cycle doorlopen.