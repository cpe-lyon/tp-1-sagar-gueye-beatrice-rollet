Manuel:
1. A l’aide du manuel, identifiez le rôle de la commande which:  
 Which renvoie le chemin des fichiers ou des liens qui sont passés en arguments.C'est à l'emplacement de la commande.   
Renvoie 0 si toures les commandes sont trouvées et éxécutables.  
Renvoie 1 si une (ou plusieurs) commande n'existe pas ou n'est pas exécutée.  
Renvoie 2 si une option spécifiée.    
2. Quand on consulte une page du manuel, comment peut-on rechercher un terme (par exemple, chercher
le terme option dans la page de manuel de which ?
Une fois dans le manuel, il suffit de tape '/' suivi du mot à rechercher. ex: /option.  
Cela aménera à la premiere occurence du mot et surlignera les prochaines occurences.  
3.Comment quitte-t-on le manuel ?  Il suffit d'appuyer sur 'q' pour quitter le manuel.  
4. Chaque section du manuel a une première page, qui présente le contenu de la section. Afficher la
première page de la section 6 ; de quoi parle cette section ?  Il suffit d'utiliser la commande 'man 6 intro'.  

Navigation dans l’arborescence des fichiers:  
1.allez dans le dossier /var/log   On utilise la commande ' cd /var/log'  
2.remontez dans le dossier parent (/var) en utilisant un chemin relatif   On utilise la commande 'cd /var'
3.retournez dans le dossier personnel   On utilise cd ..  
4. revenez au dossier précédent (/var) sans utiliser de chemin  On utilise la commande ' cd -'  
5. essayez d’accéder au dossier /root ; que se passe-t-il ?  Nous n'avons la permission d'y accéder. Message : Permission denied
6. essayez la commande sudo cd /root ; que se passe-t-il ? Expliquez  La commande sudo fait passer en superadministrateur. Le mot de passe est demandé pour le passage en super administateur.   
Cependant ça ne marche car exécute des programmes et cd n'en est pas un.
7.  à partir de votre dossier personnel, créez l’arborescence suivante :  Creation de dossier: 'sudo mkdir dossier1 dossier2'. On utilise ce type de commande pour crer toute l'arborescence demandée.  
8. revenez dans votre dossier personnel ; à l’aide de la commande rm, essayez de supprimer Fichier1, puis
Dossier1 ; que se passe-t-il ?   On ne peut pas supprimer fichier car on est pas dans le bon dossier. On ne peut pas supprimer le dossier avec la commande rm.  
9.quelle commande permet de supprimer un dossier   La commande pour supprimer un dossier est rm -r. la suppression récursive permet de supprimer tout les fichiers dans le dossier puis le dossier lui même. Un dossier se supprome avec rmdir    
10.que se passe-t-il quand on applique cette commande à Dossier2 ?   la commande nous fait descendre dans l'arborescence du dossier puis nous demande la confirmation de supression des fichiers un à un.  
11. comment supprimer en une seule commande Dossier2 et son contenu ?  On utilise sudo rm -r.  

Commandes importantes:  
1. Quelle commande permet d’afficher l’heure ? A quoi sert la commande time ?  
On utilise la commande date qui affiche l'heure et la date. date quant à elle permet de connaitre le temps d'exécution d'une commande entrée en paramètres.  
2.Dans votre dossier personnel, tapez successivement les commandes ls puis la ; que peut-on en déduire
sur les fichiers commençant par un point ? La est la contraction ed ls -A qui permet d'afficher les fichier cachés. On en déduit que les fichiers commençant par un point sont cachés.  
3. Où se situe le programme ls ? On utilise la comande which ls. ce qui nous permet de trouver le chemin qui est : user/bin/ls.  
4.Essayez la commande ll. Existe-t-il une entrée de manuel pour cette commande ? Utilisez les commandes alias ou alias pour en savoir plus sur la nature de cette commande. ll permet d'afficher les droit des différents types d'utilisateurs sur les fichiers. Il n'y a pas d'entrée ll dans le manuel. 
Avec la commande alias ll, on comprend qu'il s'agit en fait de la commande ls -alF. C'est pour ça qu'il n'y a pas d'entrée dans le manuel.  
5. Quelle commande permet d’afficher les fichiers contenus dans le dossier /bin ?On utilise la commande  ls /bin ou 
6. Que fait la commande ls .. ?ls affiche le contenu d'un dossier  
7. Quelle commande donne le chemin complet du dossier courant ?On utilise la commande pwd  
8. Que fait la commande echo 'yo' > plop exécutée 2 fois ?
La commande crée le fichier plop et écrit 'yo' dedans. Cependant le simple chevron fait que l'on écrase le contenu précédent. C'est pourquoi, si on lit le fichier, il n'ya écrit qu'une seule fois yo.  
9. Que fait la commande echo 'yo' >> plop exécutée 2 fois ?Le double chevron permet de mettre le 'yo' à la fin. le fichier contient donc 3 'yo'.
10. A quoi sert la commande file ? Essayez la sur des fichiers de types différents.File donne le type du fichier.    
11. Créez un fichier toto qui contient la chaîne Hello Toto ! ; créer ensuite un lien titi vers ce fichier
avec la commande ln toto titi. Modifiez à présent le contenu de toto et affichez le contenu de titi :
qu’observe-t-on ? Supprimez le fichier toto ; quelle conséquence cela a-t-il sur titi ?
On fait echo 'hello Toto' > toto pour créer le fichier. la modification du fichier toto entraine la modification de titi. Cependant la suppression de toto n'entraine pas la suppression de titi.  
12.Créez à présent un lien symbolique tutu sur titi avec la commande ln -s titi tutu. Modifiez le
contenu de titi ; quelle conséquence pour tutu ? Et inversement ? Supprimez le fichier titi ; quelle
conséquence cela a-t-il sur tutu ? La modification de titi entraine celle de tutu et inversement. La suppression de titi entraine la suppression de tutu et inversement.  
13. . Affichez à l’écran le fichier /var/log/syslog. Quels raccourcis clavier permettent d’interrompre et
reprendre le défilement à l’écran ?
On utilise la commande cat pour afficher le contenu. On stop le defilement avec ctrl+S et on le reprend avec ctrl+Q.  
14. Affichez les 5 premières lignes du fichier /var/log/syslog, puis les 15 dernières, puis seulement les
lignes 10 à 20.
5 premieres lignes : head -n 5 nomFichier, lignes 10 à 15: sed -n '10,15p' nomFichier, 15 dernieres lignes : tail -n 15
15.Que fait la commande dmesg | less ? La commande 'dmesg|less' affiche la sortie de la premiere commande dans less qui permet l'affiche plus claire et lisible  
16. . Affichez à l’écran le fichier /etc/passwd ; que contient-il ? Quelle commande permet d’afficher la page
de manuel de ce fichier ?Ce fichier contient l'ensemble des utilisatuers et leurs informations (mot de passe, numéro...). On utilise man 5 passwd pour afficher le manuel.  
17. Affichez seulement la première colonne triée par ordre alphabétique inverseOn utilise la commande cut -d: -f1 /etc/passwd | sort -r  
18.Quelle commande nous donne le nombre d’utilisateurs ayant un compte sur cette machine (pas seulement les utilisateurs connectés) ?
 On utilise la commande wc -l /etc/passwd 
19. . Combien de pages de manuel comportent le mot-clé conversion dans leur description ?
on utilise man -k conversion | wc -l
20. A l’aide de la commande find, recherchez tous les fichiers se nommant passwd présents sur la machine on utilise find -mane 'passwd' /
21. . Modifiez la commande précédente pour que la liste des fichiers trouvés soit enregistrée dans le fichier
~/list_passwd_files.txt et que les erreurs soient redirigées vers le fichier spécial /dev/null
 on utilise la commande find / -name passwd >~/list_passwd_list.txt 2>/dev/null
22. Dans votre dossier personnel, utilisez la commande grep pour chercher où est défini l’alias ll vu
précédemment
 grep retourne chaque occurrence de la chaine de caractères précisée, dans notre cas ll. Parmi ces occurence on trouve que l'alias se situe dans .bashrc
23. Utilisez la commande locate pour trouver le fichier history.log. on utilise locate history.log qui nous retourne /var/log/apt/history.log
24. Créer un fichier dans votre dossier personnel puis utilisez locate pour le trouver. Apparaît-il ? Pourquoi ? Locate ne fonctionne pas car cette commande ne scanne que les fichiers de la base de données qui se mets à jour quotidiennement.
Le fichier sera donc visible au ^prochain update.
