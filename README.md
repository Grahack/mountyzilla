#�What is MountyZilla ?
=======================

MountyZilla is a Firefox add-on providing extra features for the on-line game [MountyHall](http://www.mountyhall.com/). This game is avaliable in French only (actually, in Belgian only), and the whole community around it is French speaking. So sorry but the rest of this ReadMe file, as well as every single file in this repo, will be in French.


#�Notes � l'intention des d�veloppeurs
======================================

## Fonctionnement g�n�ral de l'extension
----------------------------------------

MountyZilla est constitu� d'un __module interne__ (add-on Firefox), ainsi que d'une s�rie de __scripts distants__.

Le __module interne__ doit �tre une simple base de travail, qui doit �tre la plus fixe possible, tout en contenant tout ce qui est n�cessaure au bon fonctionnement des scripts distants.

L'�l�ment le plus susceptible de changer dans le module interne est le __script ma�tre__ : c'est lui qui d�cide, en fonction de la page charg�e dans le navigateur, � quel script distant il doit confier le post-traitement de la page.

Les __scripts distants__ sont h�berg�s sur un [serveur d�di�](http://mountyzilla.tilk.info/), et contiennent les actions � effectuer sur chaque page. En g�n�ral, chaque script n'est appel� que sur la page pour laquelle il a �t� sp�cifiquement con�u. (� quelques exceptions pr�s : la biblioth�que de fonctions `libs_FF.js` est par exemple appel�e sur toutes les pages.)


##�Environnement de travail pour le d�veloppement
-------------------------------------------------

###�Codage ponctuel : cr�ez votre propre script ma�tre.

Le plus simple si vous �tes un codeur occasionnel, est de commenter les lignes du script ma�tre associ�es aux pages sur lesquelles vous travaillez, et d'ajouter votre script comme un script compl�mentaire. Simple et efficace.

### Codage avanc� : recr�er un MountyHall local

Si vous souhaitez vous investir davantage dans le d�veloppement, il vous faudra probablement faire de tr�s nombreux tests sur de tr�s nombreuses pages : impossible d�s lors de tester en live sur MountyHall.
Le plus simple dans ce cas est de monter un serveur local pour simuler le jeu et y faire vos tests. Cr�ez-vous un serveur d�di�, et d�posez-y une batterie de pages Mountyhall modifiables � l'envi pour vos tests.


## Quelques consignes avant de contribuer
-----------------------------------------

Pour le moment, sont disponibles en ligne uniquement les scripts distants. Voici quelques consignes que je tente de respecter lorsque je code. Ce ne sont pas des r�gles absolues, mais tant qu'� faire si on peut harmoniser la syntaxe, c'est pas plus mal...

1. _Soyez patient._ MountyZilla est un agglom�rat de participations de codeurs d'origine et de niveaux divers et vari�s. Vous n'aurez donc pas affaire � un code suroptimis� �crit par des professionnels du javascript. Pr�parez-vous, vous n'�tes pas � l'abri de portions de code perdurant depuis l'�re des dinosaures...
2. _Faites simple._ Ne cherchez pas � produire un code diaboliquement intelligent. Il deviendra illisible et la moindre modification ult�rieure demandera de r��crire la totalit� de votre contribution.
3. _Commentez._ M�me si la notation `pdcdlcopf` est tr�s claire pour vous (port�e-de-la-charge-dans-le-cas-o�-il-n'y-a-pas-de-fatigue`), dites-vous bien que ce ne sera pas le cas pour tout le monde. Au besoin, cr�ez une doc externe.
4. _Faites compact._ Pas de ligne de 200 caract�res impossible � afficher et � d�crypter. Les r�gles de d�veloppement chez Mozilla sont :
 * des lignes de 80 caract�res maximum,
 * avec des tabulations �quivalant � 2 caract�res.
Ce sont me semble-t-il des choix de limites raisonnables � se fixer.
5. _Codez en javascript._ Le langage Javascript, en particulier celui embarqu� par les navigateurs, fourmille d'un million de fa�ons diff�rentes d'effectuer une m�me action. Si vous devez choisir entre diverses m�thodes, efforcez-vous de donner priorit� � la syntaxe __javascript__.


##�Licence
----------

MountyZilla est distribu� sous Licence GNU GPLv2.
Si vous comptiez en tirer profit, la sortie est par l� --> [].
