Manuel:
1. Which renvoie le chemin des fichiers ou des liens qui sont passés en arguments.C'est à l'emplacement de la commande.   
Renvoie 0 si toures les commandes sont trouvées et éxécutables.  
Renvoie 1 si une (ou plusieurs) commande n'existe pas ou n'est pas exécutée.  
Renvoie 2 si une option spécifiée.    
2. Une fois dans le manuel, il suffit de tape '/' suivi du mot à rechercher. ex: /option.  
Cela aménera à la premiere occurence du mot et surlignera les prochaines occurences.  
3. Il suffit d'appuyer sur 'q' pour quitter le manuel.  
4. Il suffit d'utiliser la commande 'man 6 intro'.  

Navigation dans l’arborescence des fichiers:  
1. On utilise la commande ' cd /var/log'  
2. On utilise la commande 'cd /var'
3. On utilise cd ..  
4. On utilise la commande ' cd -'  
5. Nous n'avons la permission d'y accéder. Message : Permission denied
6. la commande sudo fait passer en superadministrateur. Le mot de passe est demandé pour le passage en super administateur.   
Cependant ça ne marche car exécute des programmes et cd n'en est pas un.
7. Creation de dossier: 'sudo mkdir dossier1 dossier2'. On utilise ce type de commande pour crer toute l'arborescence demandée.  
8. On ne peut pas supprimer fichier car on est pas dans le bon dossier. On ne peut pas supprimer le dossier avec la commande rm.  
9. La commande pour supprimer un dossier est rm -r. la suppression récursive permet de supprimer tout les fichiers dans le dossier puis le dossier lui même. Un dossier se supprome avec rmdir    
10. la commande nous fait descendre dans l'arborescence du dossier puis nous demande la confirmation de supression des fichiers un à un.  
11. On utilise sudo rm -r.  

Commandes importantes:  
1. On utilise la commande date qui affiche l'heure et la date. date quant à elle permet 
de connaitre le temps d'exécution d'une commande entrée en paramètres.  
2. La est la contraction ed ls -A qui permet d'afficher les fichier cachés. On en déduit que les fichiers commençant par un point sont cachés.  
3. On utilise la comande which ls. ce qui nous permet de trouver le chemin qui est : user/bin/ls.  
4. ll permet d'afficher les droit des différents types d'utilisateurs sur les fichiers. Il n'y a pas d'entrée ll dans le manuel. 
Avec la commande alias ll, on comprend qu'il s'agit en fait de la commande ls -alF. C'est pour ça qu'il n'y a pas d'entrée dans le manuel.  
5. On utilise la commande  ls /bin ou 
6. ls affiche le contenu d'un dossier  
7. On utilise la commande pwd  
8. La commande crée le fichier plop et écrit 'yo' dedans. Cependant le simple chevron fait que l'on écrase le contenu précédent. C'est pourquoi, si on lit le fichier, il n'ya écrit qu'une seule fois yo.  
9. Le double chevron permet de mettre le 'yo' à la fin. le fichier contient donc 3 'yo'.
10. File donne le type du fichier.    
11. On fait echo 'hello Toto' > toto pour créer le fichier. la modification du fichier toto entraine la modification de titi. Cependant la suppression de toto n'entraine pas la suppression de titi.  
12. La modification de titi entraine celle de tutu et inversement. La suppression de titi entraine la suppression de tutu et inversement.  
13. On utilise la commande cat pour afficher le contenu. On stop le defilement avec ctrl+S et on le reprend avec ctrl+Q.  
14. 5 premieres lignes : head -n 5 nomFichier, lignes 10 à 15: sed -n '10,15p' nomFichier, 15 dernieres lignes : tail -n 15
15. La commande 'dmesg|less' affiche la sortie de la premiere commande dans less qui permet l'affiche plus claire et lisible  
16. Ce fichier contient l'ensemble des utilisatuers et leurs informations (mot de passe, numéro...). On utilise man 5 passwd pour afficher le manuel.  
17. On utilise la commande cut -d: -f1 /etc/passwd | sort -r  
18. On utilise la commande wc -l /etc/passwd 
19. on utilise man -k conversion | wc -l
20. on utilise find -mane 'passwd' /


