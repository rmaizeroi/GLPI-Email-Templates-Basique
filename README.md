# GLPI : Modèle de notifications

Les modèles de notification par défaut de GLPI n'étant pas très "lisibles", j’ai donc repris le travail de "eduardomozart/GLPI-Email-Templates", lui-même inspiré des templates de [hmarthe/TCAT-M-osTicket-Email-Templates](https://github.com/hmarthe/TCAT-M-osTicket-Email-Templates), pour en proposer une version simpliste et adaptée en français.

Ce modèle a été testé avec succès sur :

1. Microsoft Outlook (Online / OWA)
1. Mozilla Thunderbird version 128.14

## Screenshots

![Novo acompanhamento (New ticket)](/screenshots/new-ticket.png?raw=true "Novo acompanhamento (New ticket)")

*Novo chamado (New ticket).*
 
![Novo acompanhamento (New followup)](/screenshots/new-followup.png?raw=true "Novo acompanhamento (New followup)/Atualização de um acompanhamento (Update of a ticket)")

*Novo acompanhamento (New followup)/Atualização de um acompanhamento (Update of a followup).*

![Novo acompanhamento (New followup)](/screenshots/new-or-update-task.png?raw=true "Nova tarefa (New task)/Atualização de uma tarefa (Update of a task)")

*Nova tarefa (New task)/Atualização de uma tarefa (Update of a task).*

![Chamado solucionado (Ticket solved)](/screenshots/solution.png?raw=true "Chamado solucionado (Ticket solved)")

*Chamado solucionado (Ticket solved).*

![Pesquisa de satisfação (Satisfaction survey)](/screenshots/ticket-satisfaction.png?raw=true "Pesquisa de satisfação (Satisfaction survey)")

*Pesquisa de satisfação (Satisfaction survey).*

![Resposta da pesquisa de satisfação (Satisfaction survey answer)](/screenshots/ticket-satisfaction-response.png?raw=true "Resposta da pesquisa de satisfação (Satisfaction survey answer)")

*Resposta da pesquisa de satisfação (Satisfaction survey).*

## Translation

These templates rely on ``ticket.action`` to adapt the message body (HTML) to correspond to the notification type (new ticket, new followup, etc), but this method rely on translated strings, e.g. to detect that the message refers to a "New ticket", the template detects it with ``##IFticket.action=Novo chamado##``. **Novo chamado** is the translation to "New ticket" in "Português do Brasil".

Another function that has depends on translated strings are ``ticket.isprivate``, e.g. to detect that a followup or task has been marked as private, it uses the function ``##IFticket.isprivate=Não##``. "**Não**" is the translation to "No" in "Português do Brasil".

You'll need to translate all ``ticket.action`` and ``ticket.isprivate`` function calls into the template files according to your language before deploying it into your GLPI instance if you're not using the language "Português do Brasil" by default into your environment.

## Installation

As cited on "**Translation**" section, it relies on translated strings to detect the notification type (new ticket, new followup, etc) and to detect if a task or followup has been marked as private, so you'll need to create a specific notification template for each language that you would like to support.

### Tickets Template

1. In **Setup** > **Notifications** > **Notification Templates**, click on **Tickets** in the list.
1. Click on **Template translations** > **Add a New Translation**.
1. Select your language into **Language** dropdown, e.g. "Português do Brasil".
1. Enter the **Subject** of the notification template (Default: ``##ticket.action## ##ticket.title##``)
1. In **Email text body**, paste the content of the ``Tickets.txt`` template.
1. In **Email HTML body**, click on the option "Source code" and paste the HTML body of the ``Tickets.html`` template.

### Ticket Satisfaction Template

1. In **Setup** > **Notifications** > **Notification Templates**, click on **Tickets Satisfaction** in the list.
1. Click on **Template translations** > **Add a New Translation**.
1. Select your language into **Language** dropdown, e.g. "Português do Brasil".
1. Enter the **Subject** of the notification template (Default: ``##ticket.action## ##ticket.title##``)
1. In **Email text body**, paste the content of the ``Ticket Satisfaction.txt`` template.
1. In **Email HTML body**, click on the option "Source code" and paste the HTML body of the ``Tickets Satisfaction.html`` template.

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
