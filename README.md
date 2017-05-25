# boinc
FR :

Script pour Linux en Bash pour boinc

suspend_calc : surveille et suspend les UT d'un projet au choix qui sont sur le point de se terminer.

resume_calc : reprend les UT d'un projet au choix qui sont en attente pour les finir à une date/heure donnée (ou immédiatement).

Pour les deux scripts : vous devez modifier la ligne au début boincdos pour y indiquer le chemin de votre dossier de travail boinc (nécessaires pour boinccmd).

*Astuce : on peut lancer plusieurs script en parallèle chacun gérant les UT d'un projet.*

N.B : Pensez que vous devez désuspendre les UT suspendues sinon votre client Boinc ne voudra pas télécharger de nouvelle UT. De même, vous devez (avant demande de nouvelle UT) ajuster vos valeurs de cache de travail. Faites attention à avoir de la marge au niveau des UT en attente dans votre cache, qu'il ne soit pas vide.

*suspend_calc -> Pour une utilisation silencieuse (pas d'interactions utilisateur, pas de question) : mettez l'URL du projet que vous voulez vérifier en argument.*

US/EN :

Script for Linux in Bash for boinc (in french for now)

suspend_calc : check and suspend all WU that have an estimated time remaining left (or less) for a given project.

resume_calc : resume WU that are suspended (by manager or suspend_calc) for a given project and at a day/time of choice or immediately.

For both : you need to edit each script and change the boincdos variable to put your boinc data directory (needed by boincccmd).

*Tips : you can execute in parallel those scripts, each for WUs of one project*

N.B : Be aware that your Boinc client won't download any new WU if some are suspended, think that you have to resume them before asking new WU (and you need to increase your cache value accordingly). Think to take more WU in your cache, do not let it empty.

*suspend_calc -> For a headless use (no user interaction, no question) : just put the project URL you want to check in argument.*
