# GLPI : Modèle de notifications

Les modèles de notification par défaut de GLPI n'étant pas très "lisibles", j’ai donc repris le travail de "eduardomozart/GLPI-Email-Templates", lui-même inspiré des templates de [hmarthe/TCAT-M-osTicket-Email-Templates](https://github.com/hmarthe/TCAT-M-osTicket-Email-Templates), pour en proposer une version simpliste et adaptée en français.

Ce modèle a été testé avec succès sur :

1. Microsoft Outlook (Online / OWA)
1. Mozilla Thunderbird version 128.14

## Screenshots

![Nouveau ticket](/imgs/Captures/01_nouveau_ticket.png?raw=true "Nouveau Ticket")

*Nouveau ticket*
 
![Nouveau Suivi](/imgs/Captures/02_nouveau_suivi.png?raw=true "Nouveau suivi")

*Nouveau Suivi*

![Nouvelle tache](/imgs/Captures/03_nouvelle_tache.png?raw=true "Nouveau tache")

*Nouveau tache*

![Ticket résolu](/imgs/Captures/04_résolution.png?raw=true "Ticket résolu")

*Ticket résolu*

## Informations

Contrairement aux modèles originaux, ma version se base exclusivement sur l’état du ticket pour déterminer le contenu des messages.
Note : je n’ai pas réussi à “imbriquer” les tâches et les suivis dans le récapitulatif du ticket.

### Installation

1. Dans Configuration > Notifications > Modèles de notification, cliquez sur Tickets dans la liste.
2. Cliquez sur Traductions du modèle > Ajouter une nouvelle traduction.
3. Sélectionnez la langue dans le menu déroulant
4. Saisissez l’objet du modèle de notification (par défaut : ##ticket.action## ##ticket.title##).
5. Dans Corps du message (HTML), collez le contenu du fichier glpi-mail-suivi.html

## License

[GNU General Public License v3.0](LICENSE) License.

## Useful Links

1. [GLPI - Notification Tags](https://pt.scribd.com/document/248614338/2GLPI-Lista-de-Tags-Disponiveis).
1. [Template de notificações para o GLPI responsivo](https://falati.com.br/template-email-responsivo-glpi/). Fala TI.
1. [Adicionando template de notificações via email personalizados no GLPI (Abertura, Acompanhamento e Encerramento de chamados)](http://nattanielafonso.com.br/adicionando-template-de-notificacoes-via-email-personalizados-no-glpi-abertura-acompanhamento-e-encerramento-de-chamados/). Nattaniel Afonso.
1. [Notificações no GLPI em HTML e CSS que funciona no Gmail](http://www.thiagopassamani.com.br/tags/glpi-notification-template-mail). Thiago Passamani.
1. [Scripts for Email Template](https://community.spiceworks.com/scripts?category=15). Spiceworks.
1. [Free HTML Email Templates for SaaS and Startups](https://www.htmlemailtemplates.net/free-stuff/free-html-email-templates/). HTML Email Templates for SaaS and Startups.
1. [Email template](https://www.helpdesk.com/help/email-template/). HelpDesk Help Center.
1. [Free Responsive Simple HTML Email Template](https://github.com/leemunroe/responsive-html-email-template). GitHub.
1. [Email Template Examples](https://github.com/zendesklabs/email_template_examples). ZendeskLabs (GitHub).
