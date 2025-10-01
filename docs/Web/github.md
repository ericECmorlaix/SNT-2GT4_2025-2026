## Mes sites web de SNT sur GitHub

Cette partie présente une démarche qui vous permettra de développer vos sites web avec l'éditeur Visual Studio Code de CodeSpaces en ligne et de les héberger dans GitHub pour les publier hors de la KhanAcademy et de Capytale...

### Créer un dépot GitHub
Créer un compte sur GitHub (Sign up) depuis un navigateur à l'adresse [https://github.com/](https://github.com/){target="_blank"} :

<figure>
    <img src="https://ericecmorlaix.github.io/img/GitHub00a.png" width=50% alt="inscription GitHub">
</figure>

Ou identifier vous (Sign in) si vous avez déjà un compte :

<figure>
    <img src="https://ericecmorlaix.github.io/img/GitHub00b.png" width=50% alt="identification GitHub">
</figure>

A l'adresse [https://github.com/new](https://github.com/new){target="_blank"} créer un nouveau répertoire de dépot nommé, par exemple `mon_premier_site` :

<figure>
    <img src="https://ericecmorlaix.github.io/img/GitHub01d.png" alt="nouveau repository GitHub">
</figure>

Cocher la case **"Initialize this repository with a README"** puis cliquer sur le bouton **"Create repository"**.

> Voilà, vous faites maintenant parti d'un autre [réseau social mondial celui des développeurs qui partage leur code](https://medium.com/coding-days/focus-sur-github-le-r%C3%A9seau-social-des-d%C3%A9veloppeurs-165a2978ea9e){target="_blank"}...


### Utiliser VSC en ligne pour gérer votre dépot GitHub depuis CodeSpaces

#### Préparation de CodeSpaces

Pour faire fonctionner l'[IDE](https://fr.wikipedia.org/wiki/Environnement_de_d%C3%A9veloppement){target=_blank} Visual Studio Code dans un navigateur et ainsi développer et maintenir des dépôts GitHub depuis n’importe quelle machine sans installation locale on peut utiliser [Codespaces](https://github.com/features/codespaces){target=_blank}
        
1. A la racine de votre dépot GitHub **cliquer** sur le bouton vert `<> Code` ;
2. **Choisir** l'onglet `Codespaces` ;
3. **Cliquer** sur le bouton vert `Create codespace on main`...

<figure>
    <img src="https://ericecmorlaix.github.io/img/Codespaces00.png" alt="Codespaces">
</figure> 


> Tous les dossiers et fichiers de votre dépot sont alors éditables dans l'environnement de développement Visual Studio Code intégré à CodeSpaces en ligne.

<figure>
    <img src="https://ericecmorlaix.github.io/img/GitPod01d.png" alt="VSC Explorer">
</figure>

#### Développement d'une page dans VSC

- Dans la zone de l'explorateur (_bleu_), **créer** un nouveau fichier (_jaune 1_) nommé `index.html` ;
- Dans la zone d'édition du fichier, **saisir** un `!` et **valider** la proposition _"Emmet Abbreviation"_ de VSC :
<code><pre>
&lt;!DOCTYPE html&gt;
&lt;html lang="en"&gt;
&lt;head&gt;
    &lt;meta charset="UTF-8"&gt;
    &lt;meta http-equiv="X-UA-Compatible" content="IE=edge"&gt;
    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0"&gt;
    &lt;title&gt;Document&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;        
&lt;/body&gt;
&lt;/html&gt;
</code></pre>

- Dans le code ainsi obtenu, **remplacer** `"en"` par `"fr"` et **donner** un titre à la page d'accueil de votre futur site ;
- **Compléter** le `body` avec les balises de contenu que vous souhaitez voir s'afficher sur cette page ;
- Dans un terminal, **saisir** `python -m http.server`, puis **cliquer** sur le bouton `Open Browser` (ou sur port pour afficher votre page dans un nouvel onglet de votre navigateur) ;
- **Compléter** le code HTML de votre page et **vérifier** le résultat obtenu en rafraichissant régulièrement l'affichage de cet onglet du navigateur ;

### Publier votre site sur GitHub

- Dans la zone Source Control (_bleu_), **cliquer** sur le `+` (_jaune_) pour ajouter les fichiers modifiés à mettre en attente (à indexer) à ce stade du développement, **ajouter** un message (_rose_) avant de **commiter** (_orange_), puis **synchroniser** vos modifications ;

<figure>
    <img src="https://ericecmorlaix.github.io/img/GitPod02d.png" alt="VSC Source">
</figure>

- **Paramétrer** GitHub pour qu'il affiche votre site Web : dans `Settings`, choisir `Pages` puis sélectionner la branche `main` et cliquer sur le bouton `Save` :

![Settings>Pages>main>Save](https://ericecmorlaix.github.io/img/GitHub02.png){.center width=80%}

- Enfin, après quelques minutes, dans un navigateur, rendez vous à une adresse telle que <https://username.github.io/nom-de-votre-site/>...


### ==La routine pour maintenir votre site Git avec un éditeur VSC en ligne se résume à :==

??? summary "I - Modifier vos fichiers sur la machine virtuelle distante :"
    ![GitPod VSC Explorer](https://ericecmorlaix.github.io/img/GitPod01d.png){align=right width= 20%} Depuis l'Explorateur (`Explorer` ++"Ctrl"+"Maj"+"E"++) de VSC (_bleu_) :

    - cliquer sur un dossier pour afficher la liste de son contenu ;
    - cliquer sur les icônes (_jaunes_) pour créer un nouveau fichier (_1_) et/ou un nouveau dossier (_2_) ;
    - maintenir le clic (= clic droit) sur un fichier (ou un dossier) pour renommer son chemin et ainsi le déplacer dans l'arborescence ;
    - cliquer sur un fichier pour l'ouvrir dans l'éditeur afin de le modifier ;
    - maintenir le clic (= clic droit) sur un fichier `.md` et choisir `Open preview` pour le prévisualiser ;
    - démarrer un serveur `python -m http.server` depuis un terminal pour visualiser un fichier `.html`

??? summary "II - Indexer vos changements :"
    ![GitPod VSC Source](https://ericecmorlaix.github.io/img/GitPod02d.png){align=right width= 20%}Depuis le "Contrôle de code source" (_bleu_) (`Source Control` ++"Ctrl"+"Maj"+"G"++),
     dans "Changements" (`Changes`) cliquer sur le `+` (_jaune_) pour ajouter les fichiers modifiés
      à mettre en attente (indexer) dans cette phase (stage) de développement ;

??? summary "III - Committer, valider vos modifications :"
    ![GitPod VSC Source](https://ericecmorlaix.github.io/img/GitPod02d.png){align=right width= 20%}Ajouter un message sous "CONTRÔLE DE CODE SOURCE" (`SOURCE CONTROL`) (_rose_)
     pour définir ces modifications à ce stade de votre développement,
      puis cliquer sur `✓` (_orange_) pour valider ce commit ;

??? summary "IV - Pousser les modifications vers votre dépôt distant :"
    Cliquer sur les `...` en face de `CONTRÔLE DE CODE SOURCE`
    et choisir `Push` ;

<figure>
    <img src="../images/undraw_web_devices_re_m8sc.svg" alt="web_devices">
</figure>