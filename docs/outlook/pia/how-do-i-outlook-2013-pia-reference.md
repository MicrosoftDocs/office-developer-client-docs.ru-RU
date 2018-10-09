---
title: Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f05f6e9199cd474a47d36ff92e255dea92a4d5cc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407557"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a>Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)

В этой части представлены разделы, содержащие описания процедур и примеры кода на языках Visual Basic и C\#, в которых демонстрируется выполнение общих задач в приложении Outlook.

Для запуска этих примеров кода необходимо установить Outlook 2010 и Visual Studio 2008 или более поздние версии этих продуктов.

Примеры кода в этом разделе не требуют установки инструментов разработчика Office для Visual Studio. Тем не менее, сведения об использовании этих инструментов можно просмотреть в статье [Начало разработки для Office](https://developer.microsoft.com/office/docs), а некоторые базовые практические задачи, написанные в управляемом коде, — в статье [Решения Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).

В этом разделе представлены примеры кода, ориентированные как на новичков, так и на пользователей со средним уровнем знаний в предметной области. Некоторые из примеров адаптированы с использованием материалов книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).

Команда подготовки документации разработчика Office приветствует идеи, касающиеся заданий, и образцы кодов. При использовании ваших примеров кода в материалах по приложению Outlook мы укажем имя автора и разместим ссылку на ваш веб-сайт. За дополнительными сведениями обращайтесь по адресу docthis@microsoft.com.

## <a name="in-this-section"></a>В этом разделе 

[Учетные записи](accounts.md)

- [Получение сведений об учетной записи](how-to-get-account-information.md)
- [Создание отправляемого элемента для определенной учетной записи на основе текущей папки](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [Получение учетной записи для папки](how-to-get-the-account-for-a-folder.md)
- [Получение сведений о нескольких учетных записях](how-to-get-information-about-multiple-accounts.md)
- [Отправка почтового элемента с помощью учетной записи Hotmail](how-to-send-a-mail-item-by-using-a-hotmail-account.md)

[Администрирование надстроек](add-in-administration.md)

- [Определение, является ли Outlook на компьютере приложением "нажми и работай"](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[Адресная книга](address-book.md)

- [Отображение в диалоговом окне "Выбор имен" адресной книги, соответствующей папке "Контакты"](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)
- [Получение глобального списка адресов или набора списков адресов для хранилища](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [Перечисление записей в глобальном списке адресов](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [Отображение списков адресов для профиля](how-to-display-the-address-lists-for-a-profile.md)

[Встречи](appointments.md)

- [Создание встречи как события на целый день](how-to-create-an-appointment-that-is-an-all-day-event.md)
- [Создание встречи, начинающейся по тихоокеанскому времени и заканчивающейся по восточному поясному времени](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- [Задание разных типов получателей для элемента встречи](how-to-specify-different-recipient-types-for-an-appointment-item.md)
- [Создание повторяющейся встречи с использованием установленного по умолчанию шаблона повтора](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [Создание встречи, которая повторяется по недельному расписанию](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [Создание ежегодно повторяющейся встречи, в которой используется шаблон YearNth](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [Поиск определенной встречи в серии повторяющихся встреч](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [Создание встречи-исключения в серии повторяющихся встреч](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [Создание напоминания для элемента встречи](how-to-create-a-reminder-for-an-appointment-item.md)
- [Импорт XML-данных встреч в объекты встреч Outlook](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[Вложения](attachments.md)

- [Вложение файла в почтовый элемент](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [Вложение элемента контакта Outlook в сообщение электронной почты](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [Ограничение размера вложения в сообщение электронной почты Outlook](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [Изменение вложения в сообщение электронной почты Outlook](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [Программное удаление вложений второго уровня безопасности из сообщений и их сохранение на диск](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[Календарь](calendar.md)

- [Совместное использование расписания доступности в указанном периоде в календаре](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [Отправка сведений календаря по электронной почте](how-to-share-calendar-information-through-e-mail.md)
- [Отображение общего календаря получателя](how-to-display-a-shared-calendar-of-a-recipient.md)
- [Сохранение календаря на диск](how-to-save-a-calendar-to-disk.md)
- [Открытие и отображение содержимого файла iCalendar](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[Цветовые категории](color-categories.md)

- [Перечисление и добавление категорий](how-to-enumerate-and-add-categories.md)
- [Назначение категорий элементу](how-to-assign-categories-to-an-item.md)

[Контакты](contacts.md)

- [Создание элемента контакта](how-to-create-a-contact-item.md)
- [Создание настраиваемого элемента контакта](how-to-create-a-custom-contact-item.md)
- [Создание элемента контакта из файла vCard и сохранение элемента в папку](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[Беседы](conversations.md)

- [Получение и отображение элементов в беседе](how-to-get-and-display-items-in-a-conversation.md)
- [Получение и перечисление выделенных бесед](how-to-get-and-enumerate-selected-conversations.md)

[Электронные визитные карточки](electronic-business-cards.md)

- [Изменение макета электронной визитной карточки](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [Отправка почтового элемента с электронной визитной карточкой](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[Пользователи Exchange](exchange-users.md)

- [Получение сведений о текущем пользователе](how-to-get-information-about-the-current-user.md)
- [Получение сведений обо всех списках рассылки, участником которых является текущий пользователь](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [Создание списка рассылки](how-to-create-a-distribution-list.md)
- [Получение участников списка рассылки Exchange](how-to-get-members-of-an-exchange-distribution-list.md)
- [Получение сведений о руководителе текущего пользователя](how-to-get-information-about-the-current-user-s-manager.md)
- [Получение сведений о доступности для руководителя пользователя Exchange](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [Проверка ответа руководителя на приглашение на собрание](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [Получение сведений о подчиненных руководителя текущего пользователя](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[Папки](folders.md)

- [Добавление папки в список папок](how-to-add-a-folder-to-the-folder-list.md)
- [Перечисление папок](how-to-enumerate-folders.md)
- [Получение папки по умолчанию и перечисление вложенных в нее папок](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [Получение папки на основе пути к ней](how-to-get-a-folder-based-on-its-folder-path.md)
- [Выбор папки и отображение сведений о папке](how-to-select-a-folder-and-display-folder-information.md)
- [Получение класса сообщений по умолчанию для папки](how-to-get-the-default-message-class-of-a-folder.md)
- [Доступ к данным решений, хранящимся в скрытом сообщении в папке](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [Проверка поддержки настраиваемых свойств элемента в запросах на уровне папки](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[Общие элементы Outlook](general-outlook-items.md)

- [Создание вспомогательного класса для доступа к общим элементам Outlook](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [Отображение выбранных элементов в активном проводнике](how-to-display-selected-items-in-the-active-explorer.md)

[Совместное использование групп](group-sharing.md)

- [Подписка на RSS-канал](how-to-subscribe-to-an-rss-feed.md)
- [Синхронизация приложения Outlook с папкой SharePoint](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[Почта](mail.md)

- [Создание почтового элемента с помощью шаблона сообщения](how-to-create-a-mail-item-by-using-a-message-template.md)
- [Создание почтового элемента, вложение отчета и отправка почтового элемента руководителю пользователя](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [Отправка электронного сообщения по SMTP-адресу учетной записи](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [Добавление параметров голосования в почтовый элемент](how-to-add-voting-options-to-a-mail-item.md)
- [Добавление настраиваемого действия в качестве ответа на почтовый элемент](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [Получение SMTP-адреса отправителя почтового элемента](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [Задание разных типов получателей для почтового элемента](how-to-specify-different-recipient-types-for-a-mail-item.md)

[Приглашения на собрания](meeting-requests.md)

- [Создание приглашения на собрание, добавление получателей и указание расположения](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [Получение организатора собрания](how-to-get-the-organizer-of-a-meeting.md)
- [Проверка всех ответов на приглашение на собрание](how-to-check-all-responses-to-a-meeting-request.md)
- [Поиск элемента встречи, связанный с приглашением на собрание](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [Автоматическое принятие приглашения на собрание](how-to-automatically-accept-a-meeting-request.md)
- [Запрос ответа у пользователя на приглашение на собрание](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[Получатели](recipients.md)

- [Отображение диалогового окна "Выбор имен" для разрешения получателей](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)
- [Получение и назначение получателей для встречи с помощью диалогового окна "Выбор имен"](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)
- [Получение адреса электронной почты получателя](how-to-get-the-e-mail-address-of-a-recipient.md)

[Правила](rules.md)

- [Создание правила для передачи почтовых элементов от руководителя и их пометки к исполнению](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [Мгновенное выполнение правила](how-to-execute-a-rule-instantly.md)
- [Выполнение правила на локальном компьютере](how-to-execute-a-rule-on-a-local-computer.md)
- [Создание правила для назначения категорий почтовым элементам с учетом нескольких слов в теме](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[Примеры задач, в которых используются события Outlook](sample-tasks-using-outlook-events.md)

- [Реализация оболочки для инспекторов и отслеживание событий уровня элемента в каждом инспекторе](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[Поиск и фильтрация](search-and-filter.md)

- [Фильтрация и эффективное перечисление элементов в папке](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [Эффективное перечисление элементов в папке с помощью метода SetColumns](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [Эффективное перечисление элементов в папке с помощью массивов](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [Перечисление элементов в папке "Входящие" с учетом времени последнего изменения](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [Фильтрация и отображение элементов папки "Входящие", измененных в прошлом месяце](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [Фильтрация и отображение многозначных свойств при перечислении элементов в папке](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [Фильтрация и отображение вычисляемых свойств при перечислении элементов в папке](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [Перечисление скрытых элементов в папке](how-to-enumerate-hidden-items-in-a-folder.md)
- [Поиск фразы в теме во всех папках и хранилищах с помощью мгновенного поиска](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [Поиск фразы в тексте элементов в папке](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [Поиск точной фразы во вложениях элементов в папке](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [Поиск и получение встреч в диапазоне времени](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [Фильтрация повторяющихся встреч и поиск строки в теме](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [Поиск и получение элементов в общем представлении](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[Сеансы](sessions.md)

- [Получение экземпляра Outlook и вход в него](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[Хранилища](stores.md)

- [Получение сведений о хранилищах в профиле](how-to-get-information-about-stores-in-a-profile.md)
- [Добавление и удаление хранилища](how-to-add-or-remove-a-store.md)

[Задачи](tasks.md)

- [Создание элемента задачи](how-to-create-a-task-item.md)
- [Назначение задачи получателю](how-to-assign-a-task-to-a-recipient.md)
- [Отображение элементов запроса выполнения задачи, отправленных получателю](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [Ответ на элемент запроса выполнения задачи](how-to-respond-to-a-task-request-item.md)
- [Создание повторяющейся задачи](how-to-create-a-recurring-task.md)
- [Пометка почтовых элементов от руководителя к исполнению](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[Представления](views.md)

- [Создание представления](how-to-create-a-view.md)
- [Добавление полей в представление](how-to-add-fields-to-a-view.md)
- [Перечисление элементов в табличном представлении](how-to-enumerate-items-in-a-table-view.md)



