## DESCRIPTION

<=====================================================>
Ce site est une plateforme educative proposant des cours sujets et corrections ayant trait aux concours des grandes ecoles du pays, ceci en vue de permettre aux jeunes de mieux se preparer a les affronter.
<=====================================================>

## INDICATIONS

	                   En cas d'ajout d'une nouvelle ecole, suivre les etapes suivantes:
 
    -Acceder a l'interface utilisateur de Django et ajouter l'image de l'ecole ainsi que son titre
    -Rescencer le lien de la nouvelle ecole dans la page "epreuve-correction.html"( Ceci a la fin dans le script JS )
    -Creer la page de la nouvelle ecole en s'inspirant du meme modele que les autres pages
    -Definir la fonction associee a la page ainsi creee dans "views.py" et rajouter le chemin de ladite page dans le fichier "urls.py"
    -Ajouter le lien vers la page en question dans toutes les autres pages( Au niveau de la rubrique "Acceder a une autre ecole?" )
    -Dans les fichiers "voir_ep.html" et "voir_cr.html", rajouter le bloc correspondant a la nouvelle page en se servant des autres modeles



                        Signification et role de quelques variables:

        * actualiser_epreuve: accede et agit sur l'attribut "src" de la balise "iframe" afin de definir le 
                              chemin d'acces vers le fichier PDF d'une epreuve
        * actualiser_corrige: accede et agit sur l'attribut "src" de la balise "iframe" afin de definir le 
                              chemin d'acces vers le fichier PDF d'une correction.
        * annee_concours_svt/annee_concours_c/annee_concours_m/...: accede a une annee precise pour une 
                                                                    discipline  d'une ecole.
        * bloc: accede au block affichant les differentes disciplines d'une ecole, ainsi que les annees disponibles.
        * changement_texte: accede et agit sur le texte proposant de consulter un(e) sujet/correction
                            d'une autre ecole.
        * for_c/for_cg/for_if/...: variable définie en local dans le navigateur (elle referencie la discipline)
                                   avec la clé "nom_m" et portant la valeur "ep-x 20y"/"cr-x 20y"/(y=0,1,2,...| 
                                   x=p,m.cg,... | "p" pour "physique", "m" pour "mathematiques", ...). 
                                   Sa valeur sera recupérée dans une variable "recuper_m_e" et contribuera 
                                   à la définition du chemin d'acces vers le fichier PDF. Celle-ci fait 
                                   allusion au fait que le PDF soit une epreuve ou une correction.
        * grille_annees: accede au block contenant toutes les annees disponibles pour une specialite
                         d'une ecole.                    
        * img_ecole: variable agissant sur le logo d'une ecole dans la page "epreuve-correction.html"                                                    
        * indicateur: variable définie en local dans le navigateur avec la clé "nom_ep"/"nom_cr" et portant la 
                      valeur "ecole"(ecole=ens_bta,iut_dla,...). Dans la page "voir_ep.html", sa valeur sera 
                      recupérée dans une variable "recuper_e_e" et contribuera à la définition du chemin 
                      d'acces vers le fichier PDF. ( Cette variable referencie l'ecole choisie.)
        * lien_epreuve/lien_correction: variable qui referencie le sous menu "epreuve" ou "correction"
        * lien_e_local: variable qui se definie lorsqu'on clique sur le sous menu epreuves( avec la cle "ep-cr"
                        et la valeur "click_on_ep")
        * lien_cr_local: variable qui se definie lorsqu'on clique sur le sous menu corrections( avec la cle 
                         "ep-cr" et la valeur "click_on_cr")
        * lien_vue: accede et agit sur la destination de l'image-lien conduisant a la visualisation d'une
                    epreuve ou correction 
        * lien_download_e: accede et agit sur la destination de l'image-lien conduisant au telechargement d'une
                           epreuve
        * lien_download_c: accede et agit sur la destination de l'image-lien conduisant au telechargement d'une
                           correction
        * lien_recupere: valeur recupérée de la variable portant la cle "ep-cr" ( les valeurs
                         possibles sont "click_on_ep" et click_on_cr ). La modification de la destination de 
                         l'image-lien conduisant au telechargement d'une epreuve/correction dependra de celle-ci.       
        * nom_matiere: accede et agit sur le nom d'une discipline d'une ecole.        
        * nom_annee: agit sur l'affichage du nom de la discipline et de l'annee d'une ecole( a gauche dans 
                     ecole.html; ecole=iut_d,ensp_y) 
        * recuper_e_e: valeur recupérée de la variable portant la cle "nom_ep" ( les valeurs
                        possibles sont "iut_bd", "ens_bta", ... ). La definition du chemin d'acces vers le PDF 
                        de l'epreuve dependra de celle-ci.
        * recuper_cr_e: valeur recupérée de la variable portant la cle "nom_cr" ( les valeurs
                        possibles sont "iut_bd", "ens_bta", ... ). La definition du chemin d'acces vers le PDF 
                        du corrige dependra de celle-ci.
        * recuper_m_e: valeur recupérée de la variable portant la cle "nom_m" ( les valeurs
                        possibles sont "ep-m 2003", "ep-cg 2015", "cr-c 2007" ... ). La definition du chemin 
                        d'acces vers le PDF du sujet/corrige dependra de celle-ci.
        * titre_ecole: variable agissant sur le titre d'une ecole dans la page "epreuve-correction.html"
        * voir_corrige: accede et agit sur la destination du lien proposant de consulter le corigé d'un 
                        sujet ( lorsqu'on peut deja voir ledit sujet)
        * voir_epreuve: accede et agit sur la destination du lien proposant de consulter le sujet d'un 
                        corrigé ( ceci, lorsqu'on peut deja voir ladite correction)
        * voir_cours: accede et agit sur la destination du lien proposant de consulter le cours lié à un 
                      sujet ( lorsqu'on peut deja voir ledit sujet)
        
        