# boinc
FR :

Script pour Linux en Bash pour boinc

suspend_calc : surveille et suspend les UT d'un projet au choix qui sont sur le point de se terminer.

resume_calc : reprend les UT d'un projet au choix qui sont en attente pour les finir à une date/heure donnée.

Pour les deux scripts : vous devez modifier la ligne au début boincdos pour y indiquer le chemin de votre dossier de travail boinc (nécessaires pour boinccmd).


US/EN :

Script for Linux in Bash for boinc (in french for now)

suspend_calc : check and suspend all WU that have an estimated time remaining left (or less) for a given project.

resume_calc : resume WU that are suspended (by manager or suspend_calc) for a given project and at a day/time of choice.

For both : you need to edit each script and change the boincdos variable to put your boinc data directory (needed by boincccmd).
