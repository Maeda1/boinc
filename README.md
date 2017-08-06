# VERSION 0.1

US : please see at the bottom

## FR : 
*note : cette version 0.1 n'est plus maintenue.*

Script pour Linux en Bash pour boinc

suspend_calc : surveille et suspend les UT d'un projet au choix qui sont sur le point de se terminer.

resume_calc : reprend les UT d'un projet au choix qui sont en attente pour les finir à une date/heure donnée (ou immédiatement).

Pour les deux scripts : vous devez modifier la ligne au début boincdos pour y indiquer le chemin de votre dossier de travail boinc (nécessaires pour boinccmd).

*Astuce : on peut lancer plusieurs script en parallèle chacun gérant les UT d'un projet.*

N.B : Pensez que vous devez désuspendre les UT suspendues sinon votre client Boinc ne voudra pas télécharger de nouvelle UT. De même, vous devez (avant demande de nouvelle UT) ajuster vos valeurs de cache de travail. Faites attention à avoir de la marge au niveau des UT en attente dans votre cache, qu'il ne soit pas vide.

Utilisation :
Il faut modifier dans le script suspend_calc, les parties *form* afin de rajouter vos exceptions, la durée par défaut est le dernier cas avec l'étoile indique le temps par défaut =99s = 1min39
Exemple :
```
       http://universeathome.pl/universe/) #URL du projet
               limite="1699s" #Temps limite en secondes
               form="$chcom[1][0-6][0-9][0-9]\.|$chcom[0-9][0-9][0-9]\.|$chcom[0-9][0-9]\.|$chcom[0-9]\." ;; #mettre sous la forme 1699 ou moins (jusqu'à 1000) ou 999 ou moins (jusqu'à 100) ou 99 ou moins (jusqu'à 10) ou 9 ou moins (jusqu'à 0). Ca couvre tous les temps restants possibles en-dessous de 1699 secondes.
```

## US/EN :
*note : 0.1 version is not maintained anymore.*

Script for Linux in Bash for boinc (in french for now)

suspend_calc : check and suspend all WU that have an estimated time remaining left (or less) for a given project.

resume_calc : resume WU that are suspended (by manager or suspend_calc) for a given project and at a day/time of choice or immediately.

For both : you need to edit each script and change the boincdos variable to put your boinc data directory (needed by boincccmd).

*Tips : you can execute in parallel those scripts, each for WUs of one project*

N.B : Be aware that your Boinc client won't download any new WU if some are suspended, think that you have to resume them before asking new WU (and you need to increase your cache value accordingly). Think to take more WU in your cache, do not let it empty.

Usage :
You need to change in suspend_calc script, the *form* var in order to put your per projects limit, duration is by default, the last case with star (99s = 1min39s).

Example :
```
       http://universeathome.pl/universe/) #Project's URL
               limite="1699s" #Limit in secs
               form="$chcom[1][0-6][0-9][0-9]\.|$chcom[0-9][0-9][0-9]\.|$chcom[0-9][0-9]\.|$chcom[0-9]\." ;; #Here, it means : 1699s or less (until 1000) or 999 or less (until 100) or 99 ou less (until 10) or 9 or less (until 0). It covers all cases of time left that are lesser than 1699s.
```

