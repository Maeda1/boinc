# VERSION 1.0
## FR :

Script pour Linux en Bash pour automatiser (planifier) des actions sur boinc

**suspend_calc** : surveille et suspend les UT d'un projet au choix qui sont sur le point de se terminer.

**resume_calc** : reprend les UT d'un projet au choix qui sont en attente pour les finir à une date/heure donnée (ou immédiatement).

**PRE-REQUIS** : pour les deux scripts : vous devez modifier la ligne au début boincdos pour y indiquer le chemin de votre dossier de travail boinc (nécessaire pour boinccmd).

*Astuce : on peut lancer plusieurs script en parallèle chacun gérant les UT d'un projet.*

N.B : Pensez que vous devez désuspendre les UT suspendues sinon votre client Boinc ne voudra pas télécharger de nouvelle UT. De même, vous devez (avant demande de nouvelle UT) ajuster vos valeurs de cache de travail. Faites attention à avoir de la marge au niveau des UT en attente dans votre cache, qu'il ne soit pas vide.

### Utilisation :

**Ligne de commande pour un lancement sans interaction utilisateur :**
```bash
suspend_calc url_du_projet

resume_calc url_projet "mm/jj/aaaa hh:mm" PID_de_suspend_calc
```
*La date a juste besoin d'etre reconnue par le système, donc prendre le format qui convient*

## US/EN :

Script for Linux in Bash for boinc to schedule tasks (in french for now, please feel free to ask if you need that the output of script texts needs to be translated)

**suspend_calc** : check and suspend all WU that have an estimated time remaining left (or less) for a given project.

**resume_calc** : resume WU that are suspended (by manager or suspend_calc) for a given project and at a day/time of choice or immediately.

PRE-REQUISITES : for both : you need to edit each script and change the boincdos variable to put your boinc data directory (needed by boincccmd).

*Tips : you can execute in parallel those scripts, each for WUs of one project*

N.B : Be aware that your Boinc client won't download any new WU if some are suspended, think that you have to resume them before asking new WU (and you need to increase your cache value accordingly). Think to take more WU in your cache, do not let it empty.

### USAGE :

**Command line argument to get a quiet script :**
```bash
suspend_calc project_url

resume_calc project_url "mm/dd/yyyy hh:mm" suspend_calc_PID
```
*Date have to be interpreted by your system, then write a valid syntax*
