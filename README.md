# GLPI : Modèle de notifications

Les modèles de notification par défaut de GLPI n'étant pas très "lisibles", j’ai donc repris le travail de [eduardomozart/GLPI-Email-Templates](https://github.com/eduardomozart/GLPI-Email-Templates), lui-même inspiré des templates de [hmarthe/TCAT-M-osTicket-Email-Templates](https://github.com/hmarthe/TCAT-M-osTicket-Email-Templates), pour en proposer une version simpliste et adaptée en français.

Ce modèle a été testé avec succès sur :

1. Microsoft Outlook (Online / OWA)
1. Mozilla Thunderbird version 128.14

## Screenshots

![Nouveau ticket](/imgs/Captures/01_nouveau_ticket.png?raw=true "Nouveau Ticket")

*Nouveau ticket*
 
![Nouveau Suivi](/imgs/Captures/02_nouveau_suivi.png?raw=true "Nouveau suivi")

*Nouveau Suivi*

![Nouvelle tache](/imgs/Captures/03_nouvelle_tache.png?raw=true "Nouvelle tache")

*Nouvelle tache*

![Ticket résolu](/imgs/Captures/04_résolution.png?raw=true "Résolution")

*Résolution*

## Informations

Contrairement aux modèles originaux, ma version se base exclusivement sur l’état du ticket pour déterminer le contenu des messages.
Note : je n’ai pas réussi à “imbriquer” les tâches et les suivis dans le récapitulatif du ticket.

### Installation

1. Dans Configuration > Notifications > Modèles de notification, cliquez sur Tickets dans la liste.
2. Cliquez sur Traductions du modèle > Ajouter une nouvelle traduction.
3. Sélectionnez la langue dans le menu déroulant
4. Saisissez l’objet du modèle de notification (par défaut : ##ticket.action## ##ticket.title##).
5. Dans Corps du message (HTML), collez le contenu du fichier glpi-mail-xxx.html

## License

[GNU General Public License v3.0](LICENSE) License.
