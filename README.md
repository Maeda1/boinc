# VERSION 1.1
US : please see at the bottom

## FR :

NOTE : La détection de l'approche de la fin d'une unité de travail est maintenant basée sur la portion effectuée 'fraction done'.

### But
Script pour Linux en Bash pour automatiser (planifier) des actions sur boinc

### suspend_calc
-> surveille et suspend les UT d'un projet au choix qui sont sur le point de se terminer.

### resume_calc
-> reprend les UT d'un projet au choix qui sont en attente pour les finir à une date/heure donnée (ou immédiatement).

### PRE-REQUIS
Pour les deux scripts : vous devez modifier la ligne au début boincdos pour y indiquer le chemin de votre dossier de travail boinc (nécessaire pour boinccmd).

*Astuce : on peut lancer plusieurs script en parallèle chacun gérant les UT d'un projet.*

N.B : Pensez que vous devez désuspendre les UT suspendues sinon votre client Boinc ne voudra pas télécharger de nouvelle UT. De même, vous devez (avant demande de nouvelle UT) ajuster vos valeurs de cache de travail. Faites attention à avoir de la marge au niveau des UT en attente dans votre cache, qu'il ne soit pas vide.

### Utilisation :

Au premier lancement, le script vérifie et crée (s'il n'existe pas) un fichier de configuration à coté du script, avec par défaut pour tous projets une limite à 95% (0.95). Libre à vous de rajouter vos URL de projet puis vos limites.

#### Exemple de fichier suspend_calc_conf :
```
#url projet;% réalisé (0.95 = 95%)
default;0.95
http://pogs.theskynet.org/pogs/;0.85
```

#### Ligne de commande pour un lancement sans interaction utilisateur :
```bash
suspend_calc url_du_projet

resume_calc url_projet "mm/jj/aaaa hh:mm" PID_de_suspend_calc
```
*La date a juste besoin d'etre reconnue par le système, donc prendre le format qui convient*

## US/EN :

NOTE : The suspend engine detection is now based on the "fraction done" setting from boinccmd --get_task.

### Goal 
Script for Linux in Bash for boinc to schedule tasks (in french for now, please feel free to ask if you need that the output of script texts needs to be translated)

### suspend_calc
-> Check and suspend all WU that have an estimated time remaining left (or less) for a given project.

### resume_calc
-> Resume WU that are suspended (by manager or suspend_calc) for a given project and at a day/time of choice or immediately.

### PRE-REQUISITES
For both : you need to edit each script and change the boincdos variable to put your boinc data directory (needed by boincccmd).

*Tips : you can execute in parallel those scripts, each for WUs of one project*

N.B : Be aware that your Boinc client won't download any new WU if some are suspended, think that you have to resume them before asking new WU (and you need to increase your cache value accordingly). Think to take more WU in your cache, do not let it empty.

### USAGE :

At the very first suspend_calc start, the script checks and create (if it doesn't exists) a configuration file next to the script, containing a default limits for all projects set to 95% (0.95). Feel free to add your project's URL and limits.

#### suspend_calc_conf example :
```
#project;fraction done (0.95 = 95%)
default;0.95
http://pogs.theskynet.org/pogs/;0.85
```
#### Command line argument to get a quiet script :
```bash
suspend_calc project_url

resume_calc project_url "mm/dd/yyyy hh:mm" suspend_calc_PID
```
*Date have to be interpreted by your system, then write a valid syntax*
