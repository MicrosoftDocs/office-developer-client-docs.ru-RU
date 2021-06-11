---
title: Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)
TOCTitle: How do I...
ms:assetid: ff647d52-bd32-4945-afa4-5b97d9a0d7dd
ms:mtpsurl: https://msdn.microsoft.com/library/Bb612741(v=office.15)
ms:contentKeyID: 55119792
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bc4e19271e2747f5ffa8586b9f2ab226d6658b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355799"
---
# <a name="how-do-i-outlook-2013-pia-reference"></a><span data-ttu-id="acec0-102">Инструкции (справочник по основной сборке взаимодействия для Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="acec0-102">How do I... (Outlook 2013 PIA reference)</span></span>

<span data-ttu-id="acec0-103">В этой части представлены разделы, содержащие описания процедур и примеры кода на языках Visual Basic и C\#, в которых демонстрируется выполнение общих задач в приложении Outlook.</span><span class="sxs-lookup"><span data-stu-id="acec0-103">This section contains procedural tasks topics and code examples in Visual Basic and C\# that demonstrate how to perform some common tasks in Outlook.</span></span>

<span data-ttu-id="acec0-104">Для запуска этих примеров кода необходимо установить Outlook 2010 и Visual Studio 2008 или более поздние версии этих продуктов.</span><span class="sxs-lookup"><span data-stu-id="acec0-104">To run these code examples, you must have installed Outlook 2010 and Visual Studio 2008, or a later version of these products.</span></span>

<span data-ttu-id="acec0-105">Примеры кода в этом разделе не требуют установки инструментов разработчика Office для Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="acec0-105">The code examples in this section do not require that you have installed Office Developer Tools for Visual Studio.</span></span> <span data-ttu-id="acec0-106">Тем не менее, сведения об использовании этих инструментов можно просмотреть в статье [Начало разработки для Office](https://developer.microsoft.com/office/docs), а некоторые базовые практические задачи, написанные в управляемом коде, — в статье [Решения Outlook](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="acec0-106">However, you can refer to the [Getting started with Office development](https://developer.microsoft.com/office/docs) portal for information about using the tools, and refer to [Outlook solutions](https://docs.microsoft.com/visualstudio/vsto/outlook-solutions?view=vs-2017) for some basic how-to tasks written in managed code.</span></span>

<span data-ttu-id="acec0-107">В этом разделе представлены примеры кода, ориентированные как на новичков, так и на пользователей со средним уровнем знаний в предметной области. Некоторые из примеров адаптированы с использованием материалов книги [Программирование приложений для Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).</span><span class="sxs-lookup"><span data-stu-id="acec0-107">Code examples in this section range from the beginner to the intermediate levels, and some of them are adapted from the book [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=utf8%26tag=msmsdn-20%26linkcode=as2%26camp=1789%26creative=9325%26creativeasin=0735622493).</span></span>

<span data-ttu-id="acec0-108">Команда подготовки документации разработчика Office приветствует идеи, касающиеся заданий, и образцы кодов.</span><span class="sxs-lookup"><span data-stu-id="acec0-108">The Office Developer Documentation team welcomes your task ideas and code samples.</span></span> <span data-ttu-id="acec0-109">При использовании ваших примеров кода в материалах по приложению Outlook мы укажем имя автора и разместим ссылку на ваш веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="acec0-109">If we use your code samples in Outlook content, we will recognize your work with a byline and a link to your website.</span></span> <span data-ttu-id="acec0-110">За дополнительными сведениями обращайтесь по адресу docthis@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="acec0-110">For more information, contact us at docthis@microsoft.com.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="acec0-111">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="acec0-111">In this section</span></span> 

[<span data-ttu-id="acec0-112">Учетные записи</span><span class="sxs-lookup"><span data-stu-id="acec0-112">Accounts</span></span>](accounts.md)

- [<span data-ttu-id="acec0-113">Получение сведений об учетной записи</span><span class="sxs-lookup"><span data-stu-id="acec0-113">Get account information</span></span>](how-to-get-account-information.md)
- [<span data-ttu-id="acec0-114">Создание отправляемого элемента для определенной учетной записи на основе текущей папки</span><span class="sxs-lookup"><span data-stu-id="acec0-114">Create a sendable item for a specific account based on the current folder</span></span>](how-to-create-a-sendable-item-for-a-specific-account-based-on-the-current-folder.md)
- [<span data-ttu-id="acec0-115">Получение учетной записи для папки</span><span class="sxs-lookup"><span data-stu-id="acec0-115">Get the account for a folder</span></span>](how-to-get-the-account-for-a-folder.md)
- [<span data-ttu-id="acec0-116">Получение сведений о нескольких учетных записях</span><span class="sxs-lookup"><span data-stu-id="acec0-116">Get information about multiple accounts</span></span>](how-to-get-information-about-multiple-accounts.md)
- [<span data-ttu-id="acec0-117">Отправка почтового элемента с помощью учетной записи Hotmail</span><span class="sxs-lookup"><span data-stu-id="acec0-117">Send a mail item by using a Hotmail account</span></span>](how-to-send-a-mail-item-by-using-a-hotmail-account.md)

[<span data-ttu-id="acec0-118">Администрирование надстроек</span><span class="sxs-lookup"><span data-stu-id="acec0-118">Add-in administration</span></span>](add-in-administration.md)

- [<span data-ttu-id="acec0-119">Определение, является ли Outlook на компьютере приложением "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="acec0-119">Determine whether Outlook is a Click-to-Run application on a computer</span></span>](how-to-determine-whether-outlook-is-a-click-to-run-application-on-a-computer.md)


[<span data-ttu-id="acec0-120">Адресная книга</span><span class="sxs-lookup"><span data-stu-id="acec0-120">Address book</span></span>](address-book.md)

- [<span data-ttu-id="acec0-121">Отображение в диалоговом окне "Выбор имен" адресной книги, соответствующей папке "Контакты"</span><span class="sxs-lookup"><span data-stu-id="acec0-121">Display in the Select Names dialog box the address book corresponding to a Contacts folder</span></span>](how-to-display-in-the-select-names-dialog-box-the-address-book-corresponding-to-a-contacts-folder.md)
- [<span data-ttu-id="acec0-122">Получение глобального списка адресов или набора списков адресов для хранилища</span><span class="sxs-lookup"><span data-stu-id="acec0-122">Get the Global Address List or a set of address lists for a store</span></span>](how-to-get-the-global-address-list-or-a-set-of-address-lists-for-a-store.md)
- [<span data-ttu-id="acec0-123">Перечисление записей в глобальном списке адресов</span><span class="sxs-lookup"><span data-stu-id="acec0-123">Enumerate the entries in the Global Address List</span></span>](how-to-enumerate-the-entries-in-the-global-address-list.md)
- [<span data-ttu-id="acec0-124">Отображение списков адресов для профиля</span><span class="sxs-lookup"><span data-stu-id="acec0-124">Display the address lists for a profile</span></span>](how-to-display-the-address-lists-for-a-profile.md)

[<span data-ttu-id="acec0-125">Встречи</span><span class="sxs-lookup"><span data-stu-id="acec0-125">Appointments</span></span>](appointments.md)

- [<span data-ttu-id="acec0-126">Создание встречи как события на целый день</span><span class="sxs-lookup"><span data-stu-id="acec0-126">Create an appointment that is an all-day event</span></span>](how-to-create-an-appointment-that-is-an-all-day-event.md)
- [<span data-ttu-id="acec0-127">Создание встречи, начинающейся по тихоокеанскому времени и заканчивающейся по восточному поясному времени</span><span class="sxs-lookup"><span data-stu-id="acec0-127">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>](how-to-create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone.md)
- [<span data-ttu-id="acec0-128">Задание разных типов получателей для элемента встречи</span><span class="sxs-lookup"><span data-stu-id="acec0-128">Specify different recipient types for an appointment item</span></span>](how-to-specify-different-recipient-types-for-an-appointment-item.md)
- [<span data-ttu-id="acec0-129">Создание повторяющейся встречи с использованием установленного по умолчанию шаблона повтора</span><span class="sxs-lookup"><span data-stu-id="acec0-129">Create a recurring appointment by using the default recurrence pattern</span></span>](how-to-create-a-recurring-appointment-by-using-the-default-recurrence-pattern.md)
- [<span data-ttu-id="acec0-130">Создание встречи, которая повторяется по недельному расписанию</span><span class="sxs-lookup"><span data-stu-id="acec0-130">Create a recurring appointment that has a weekly pattern</span></span>](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)
- [<span data-ttu-id="acec0-131">Создание ежегодно повторяющейся встречи, в которой используется шаблон YearNth</span><span class="sxs-lookup"><span data-stu-id="acec0-131">Create an annual recurring appointment that uses a YearNth pattern</span></span>](how-to-create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern.md)
- [<span data-ttu-id="acec0-132">Поиск определенной встречи в серии повторяющихся встреч</span><span class="sxs-lookup"><span data-stu-id="acec0-132">Find a specific appointment in a recurring appointment series</span></span>](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="acec0-133">Создание встречи-исключения в серии повторяющихся встреч</span><span class="sxs-lookup"><span data-stu-id="acec0-133">Create an exception appointment in a recurring appointment series</span></span>](how-to-create-an-exception-appointment-in-a-recurring-appointment-series.md)
- [<span data-ttu-id="acec0-134">Создание напоминания для элемента встречи</span><span class="sxs-lookup"><span data-stu-id="acec0-134">Create a reminder for an appointment item</span></span>](how-to-create-a-reminder-for-an-appointment-item.md)
- [<span data-ttu-id="acec0-135">Импорт XML-данных встреч в объекты встреч Outlook</span><span class="sxs-lookup"><span data-stu-id="acec0-135">Import appointment XML data into Outlook appointment objects</span></span>](how-to-import-appointment-xml-data-into-outlook-appointment-objects.md)

[<span data-ttu-id="acec0-136">Вложения</span><span class="sxs-lookup"><span data-stu-id="acec0-136">Attachments</span></span>](attachments.md)

- [<span data-ttu-id="acec0-137">Вложение файла в почтовый элемент</span><span class="sxs-lookup"><span data-stu-id="acec0-137">Attach a file to a mail item</span></span>](https://docs.microsoft.com/office/vba/outlook/How-to/Items-Folders-and-Stores/attach-a-file-to-a-mail-item)
- [<span data-ttu-id="acec0-138">Вложение элемента контакта Outlook в электронное письмо</span><span class="sxs-lookup"><span data-stu-id="acec0-138">Attach an Outlook Contact item to an email message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/attach-an-outlook-contact-item-to-an-email-message)
- [<span data-ttu-id="acec0-139">Ограничение размера вложения в сообщение электронной почты Outlook</span><span class="sxs-lookup"><span data-stu-id="acec0-139">Limit the size of an attachment to an Outlook email message</span></span>](https://docs.microsoft.com/office/vba/outlook/Concepts/Attachments/limit-the-size-of-an-attachment-to-an-outlook-email-message)
- [<span data-ttu-id="acec0-140">Изменение вложения в электронное письмо Outlook</span><span class="sxs-lookup"><span data-stu-id="acec0-140">Modify an attachment of an Outlook email message</span></span>](https://docs.microsoft.com/office/vba/outlook/concepts/attachments/modify-an-attachment-of-an-outlook-email-message)
- [<span data-ttu-id="acec0-141">Программное удаление вложений второго уровня безопасности из сообщений и их сохранение на диск</span><span class="sxs-lookup"><span data-stu-id="acec0-141">Programmatically remove security level 2 attachments from messages and save them to disk</span></span>](how-to-programmatically-remove-security-level-2-attachments-from-messages-and-save-them-to-disk.md)

[<span data-ttu-id="acec0-142">Календарь</span><span class="sxs-lookup"><span data-stu-id="acec0-142">Calendar</span></span>](calendar.md)

- [<span data-ttu-id="acec0-143">Совместное использование расписания доступности в указанном периоде в календаре</span><span class="sxs-lookup"><span data-stu-id="acec0-143">Share Free/Busy schedule within a specified period in a calendar</span></span>](how-to-share-free-busy-schedule-within-a-specified-period-in-a-calendar.md)
- [<span data-ttu-id="acec0-144">Отправка сведений календаря по электронной почте</span><span class="sxs-lookup"><span data-stu-id="acec0-144">Share calendar information through email</span></span>](how-to-share-calendar-information-through-e-mail.md)
- [<span data-ttu-id="acec0-145">Отображение общего календаря получателя</span><span class="sxs-lookup"><span data-stu-id="acec0-145">Display a shared calendar of a recipient</span></span>](how-to-display-a-shared-calendar-of-a-recipient.md)
- [<span data-ttu-id="acec0-146">Сохранение календаря на диск</span><span class="sxs-lookup"><span data-stu-id="acec0-146">Save a calendar to disk</span></span>](how-to-save-a-calendar-to-disk.md)
- [<span data-ttu-id="acec0-147">Открытие и отображение содержимого файла iCalendar</span><span class="sxs-lookup"><span data-stu-id="acec0-147">Open and display the contents of an iCalendar file</span></span>](how-to-open-and-display-the-contents-of-an-icalendar-file.md)

[<span data-ttu-id="acec0-148">Цветовые категории</span><span class="sxs-lookup"><span data-stu-id="acec0-148">Color categories</span></span>](color-categories.md)

- [<span data-ttu-id="acec0-149">Перечисление и добавление категорий</span><span class="sxs-lookup"><span data-stu-id="acec0-149">Enumerate and add categories</span></span>](how-to-enumerate-and-add-categories.md)
- [<span data-ttu-id="acec0-150">Назначение категорий элементу</span><span class="sxs-lookup"><span data-stu-id="acec0-150">Assign categories to an item</span></span>](how-to-assign-categories-to-an-item.md)

[<span data-ttu-id="acec0-151">Контакты</span><span class="sxs-lookup"><span data-stu-id="acec0-151">Contacts</span></span>](contacts.md)

- [<span data-ttu-id="acec0-152">Создание элемента контакта</span><span class="sxs-lookup"><span data-stu-id="acec0-152">Create a Contact item</span></span>](how-to-create-a-contact-item.md)
- [<span data-ttu-id="acec0-153">Создание настраиваемого элемента контакта</span><span class="sxs-lookup"><span data-stu-id="acec0-153">Create a custom Contact item</span></span>](how-to-create-a-custom-contact-item.md)
- [<span data-ttu-id="acec0-154">Создание элемента контакта из файла vCard и сохранение элемента в папку</span><span class="sxs-lookup"><span data-stu-id="acec0-154">Create a Contact item from a vCard file and save the item in a folder</span></span>](how-to-create-a-contact-item-from-a-vcard-file-and-save-the-item-in-a-folder.md)

[<span data-ttu-id="acec0-155">Беседы</span><span class="sxs-lookup"><span data-stu-id="acec0-155">Conversations</span></span>](conversations.md)

- [<span data-ttu-id="acec0-156">Получение и отображение элементов в беседе</span><span class="sxs-lookup"><span data-stu-id="acec0-156">Get and display items in a conversation</span></span>](how-to-get-and-display-items-in-a-conversation.md)
- [<span data-ttu-id="acec0-157">Получение и перечисление выделенных бесед</span><span class="sxs-lookup"><span data-stu-id="acec0-157">Get and enumerate selected conversations</span></span>](how-to-get-and-enumerate-selected-conversations.md)

[<span data-ttu-id="acec0-158">Электронные визитные карточки</span><span class="sxs-lookup"><span data-stu-id="acec0-158">Electronic business cards</span></span>](electronic-business-cards.md)

- [<span data-ttu-id="acec0-159">Изменение макета электронной визитной карточки</span><span class="sxs-lookup"><span data-stu-id="acec0-159">Modify the layout of an electronic business card</span></span>](how-to-modify-the-layout-of-an-electronic-business-card.md)
- [<span data-ttu-id="acec0-160">Отправка почтового элемента с электронной визитной карточкой</span><span class="sxs-lookup"><span data-stu-id="acec0-160">Send a mail item with an electronic business card</span></span>](how-to-send-a-mail-item-with-an-electronic-business-card.md)

[<span data-ttu-id="acec0-161">Пользователи Exchange</span><span class="sxs-lookup"><span data-stu-id="acec0-161">Exchange users</span></span>](exchange-users.md)

- [<span data-ttu-id="acec0-162">Получение сведений о текущем пользователе</span><span class="sxs-lookup"><span data-stu-id="acec0-162">Get information about the current user</span></span>](how-to-get-information-about-the-current-user.md)
- [<span data-ttu-id="acec0-163">Получение сведений обо всех списках рассылки, участником которых является текущий пользователь</span><span class="sxs-lookup"><span data-stu-id="acec0-163">Get information about all distribution lists of which the current user is a member</span></span>](how-to-get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member.md)
- [<span data-ttu-id="acec0-164">Создание списка рассылки</span><span class="sxs-lookup"><span data-stu-id="acec0-164">Create a distribution list</span></span>](how-to-create-a-distribution-list.md)
- [<span data-ttu-id="acec0-165">Получение участников списка рассылки Exchange</span><span class="sxs-lookup"><span data-stu-id="acec0-165">Get members of an Exchange distribution list</span></span>](how-to-get-members-of-an-exchange-distribution-list.md)
- [<span data-ttu-id="acec0-166">Получение сведений о руководителе текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="acec0-166">Get information about the current user's manager</span></span>](how-to-get-information-about-the-current-user-s-manager.md)
- [<span data-ttu-id="acec0-167">Получение сведений о доступности для руководителя пользователя Exchange</span><span class="sxs-lookup"><span data-stu-id="acec0-167">Get availability information for an Exchange user's manager</span></span>](how-to-get-availability-information-for-an-exchange-user-s-manager.md)
- [<span data-ttu-id="acec0-168">Проверка ответа руководителя на приглашение на собрание</span><span class="sxs-lookup"><span data-stu-id="acec0-168">Check a manager's response to a meeting request</span></span>](how-to-check-a-manager-s-response-to-a-meeting-request.md)
- [<span data-ttu-id="acec0-169">Получение сведений о подчиненных руководителя текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="acec0-169">Get information about direct reports of the current user's manager</span></span>](how-to-get-information-about-direct-reports-of-the-current-user-s-manager.md)

[<span data-ttu-id="acec0-170">Папки</span><span class="sxs-lookup"><span data-stu-id="acec0-170">Folders</span></span>](folders.md)

- [<span data-ttu-id="acec0-171">Добавление папки в список папок</span><span class="sxs-lookup"><span data-stu-id="acec0-171">Add a folder to the folder list</span></span>](how-to-add-a-folder-to-the-folder-list.md)
- [<span data-ttu-id="acec0-172">Перечисление папок</span><span class="sxs-lookup"><span data-stu-id="acec0-172">Enumerate folders</span></span>](how-to-enumerate-folders.md)
- [<span data-ttu-id="acec0-173">Получение папки по умолчанию и перечисление вложенных в нее папок</span><span class="sxs-lookup"><span data-stu-id="acec0-173">Get a default folder and enumerate its subfolders</span></span>](how-to-get-a-default-folder-and-enumerate-its-subfolders.md)
- [<span data-ttu-id="acec0-174">Получение папки на основе пути к ней</span><span class="sxs-lookup"><span data-stu-id="acec0-174">Get a folder based on its folder path</span></span>](how-to-get-a-folder-based-on-its-folder-path.md)
- [<span data-ttu-id="acec0-175">Выбор папки и отображение сведений о папке</span><span class="sxs-lookup"><span data-stu-id="acec0-175">Select a folder and display folder information</span></span>](how-to-select-a-folder-and-display-folder-information.md)
- [<span data-ttu-id="acec0-176">Получение класса сообщений по умолчанию для папки</span><span class="sxs-lookup"><span data-stu-id="acec0-176">Get the default message class of a folder</span></span>](how-to-get-the-default-message-class-of-a-folder.md)
- [<span data-ttu-id="acec0-177">Доступ к данным решений, хранящимся в скрытом сообщении в папке</span><span class="sxs-lookup"><span data-stu-id="acec0-177">Access solution-specific data stored as a hidden message in a folder</span></span>](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)
- [<span data-ttu-id="acec0-178">Проверка поддержки настраиваемых свойств элемента в запросах на уровне папки</span><span class="sxs-lookup"><span data-stu-id="acec0-178">Ensure that custom item properties are supported in folder-level queries</span></span>](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md)

[<span data-ttu-id="acec0-179">Общие элементы Outlook</span><span class="sxs-lookup"><span data-stu-id="acec0-179">General Outlook items</span></span>](general-outlook-items.md)

- [<span data-ttu-id="acec0-180">Создание вспомогательного класса для доступа к общим элементам Outlook</span><span class="sxs-lookup"><span data-stu-id="acec0-180">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="acec0-181">Отображение выбранных элементов в активном проводнике</span><span class="sxs-lookup"><span data-stu-id="acec0-181">Display selected items in the active Explorer</span></span>](how-to-display-selected-items-in-the-active-explorer.md)

[<span data-ttu-id="acec0-182">Совместное использование групп</span><span class="sxs-lookup"><span data-stu-id="acec0-182">Group sharing</span></span>](group-sharing.md)

- [<span data-ttu-id="acec0-183">Подписка на RSS-канал</span><span class="sxs-lookup"><span data-stu-id="acec0-183">Subscribe to an RSS feed</span></span>](how-to-subscribe-to-an-rss-feed.md)
- [<span data-ttu-id="acec0-184">Синхронизация приложения Outlook с папкой SharePoint</span><span class="sxs-lookup"><span data-stu-id="acec0-184">Synchronize Outlook with a SharePoint folder</span></span>](how-to-synchronize-outlook-with-a-sharepoint-folder.md)

[<span data-ttu-id="acec0-185">Почта</span><span class="sxs-lookup"><span data-stu-id="acec0-185">Mail</span></span>](mail.md)

- [<span data-ttu-id="acec0-186">Создание почтового элемента с помощью шаблона сообщения</span><span class="sxs-lookup"><span data-stu-id="acec0-186">Create a mail item by using a message template</span></span>](how-to-create-a-mail-item-by-using-a-message-template.md)
- [<span data-ttu-id="acec0-187">Создание почтового элемента, вложение отчета и отправка почтового элемента руководителю пользователя</span><span class="sxs-lookup"><span data-stu-id="acec0-187">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>](how-to-create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-user-s-manager.md)
- [<span data-ttu-id="acec0-188">Отправка электронного сообщения по SMTP-адресу учетной записи</span><span class="sxs-lookup"><span data-stu-id="acec0-188">Send an email given the SMTP address of an account</span></span>](how-to-send-an-e-mail-given-the-smtp-address-of-an-account.md)
- [<span data-ttu-id="acec0-189">Добавление параметров голосования в почтовый элемент</span><span class="sxs-lookup"><span data-stu-id="acec0-189">Add voting options to a mail item</span></span>](how-to-add-voting-options-to-a-mail-item.md)
- [<span data-ttu-id="acec0-190">Добавление настраиваемого действия в качестве ответа на почтовый элемент</span><span class="sxs-lookup"><span data-stu-id="acec0-190">Add a custom action as a response to a mail item</span></span>](how-to-add-a-custom-action-as-a-response-to-a-mail-item.md)
- [<span data-ttu-id="acec0-191">Получение SMTP-адреса отправителя почтового элемента</span><span class="sxs-lookup"><span data-stu-id="acec0-191">Get the SMTP address of the sender of a mail item</span></span>](how-to-get-the-smtp-address-of-the-sender-of-a-mail-item.md)
- [<span data-ttu-id="acec0-192">Задание разных типов получателей для почтового элемента</span><span class="sxs-lookup"><span data-stu-id="acec0-192">Specify different recipient types for a mail item</span></span>](how-to-specify-different-recipient-types-for-a-mail-item.md)

[<span data-ttu-id="acec0-193">Приглашения на собрания</span><span class="sxs-lookup"><span data-stu-id="acec0-193">Meeting requests</span></span>](meeting-requests.md)

- [<span data-ttu-id="acec0-194">Создание приглашения на собрание, добавление получателей и указание расположения</span><span class="sxs-lookup"><span data-stu-id="acec0-194">Create a meeting request, add recipients, and specify a location</span></span>](how-to-create-a-meeting-request-add-recipients-and-specify-a-location.md)
- [<span data-ttu-id="acec0-195">Получение организатора собрания</span><span class="sxs-lookup"><span data-stu-id="acec0-195">Get the organizer of a meeting</span></span>](how-to-get-the-organizer-of-a-meeting.md)
- [<span data-ttu-id="acec0-196">Проверка всех ответов на приглашение на собрание</span><span class="sxs-lookup"><span data-stu-id="acec0-196">Check all responses to a meeting request</span></span>](how-to-check-all-responses-to-a-meeting-request.md)
- [<span data-ttu-id="acec0-197">Поиск элемента встречи, связанный с приглашением на собрание</span><span class="sxs-lookup"><span data-stu-id="acec0-197">Find the appointment item associated with a meeting request</span></span>](how-to-find-the-appointment-item-associated-with-a-meeting-request.md)
- [<span data-ttu-id="acec0-198">Автоматическое принятие приглашения на собрание</span><span class="sxs-lookup"><span data-stu-id="acec0-198">Automatically accept a meeting request</span></span>](how-to-automatically-accept-a-meeting-request.md)
- [<span data-ttu-id="acec0-199">Запрос ответа у пользователя на приглашение на собрание</span><span class="sxs-lookup"><span data-stu-id="acec0-199">Prompt a user to respond to a meeting request</span></span>](how-to-prompt-a-user-to-respond-to-a-meeting-request.md)

[<span data-ttu-id="acec0-200">Получатели</span><span class="sxs-lookup"><span data-stu-id="acec0-200">Recipients</span></span>](recipients.md)

- [<span data-ttu-id="acec0-201">Отображение диалогового окна "Выбор имен" для разрешения получателей</span><span class="sxs-lookup"><span data-stu-id="acec0-201">Display the Select Names dialog box to resolve recipients</span></span>](how-to-display-the-select-names-dialog-box-to-resolve-recipients.md)
- [<span data-ttu-id="acec0-202">Получение и назначение получателей для встречи с помощью диалогового окна "Выбор имен"</span><span class="sxs-lookup"><span data-stu-id="acec0-202">Use the Select Names dialog box to obtain and assign recipients to an appointment</span></span>](how-to-use-the-select-names-dialog-box-to-obtain-and-assign-recipients-to-an-appointment.md)
- [<span data-ttu-id="acec0-203">Получение адреса электронной почты получателя</span><span class="sxs-lookup"><span data-stu-id="acec0-203">Get the email address of a recipient</span></span>](how-to-get-the-e-mail-address-of-a-recipient.md)

[<span data-ttu-id="acec0-204">Правила</span><span class="sxs-lookup"><span data-stu-id="acec0-204">Rules</span></span>](rules.md)

- [<span data-ttu-id="acec0-205">Создание правила для передачи почтовых элементов от руководителя и их пометки к исполнению</span><span class="sxs-lookup"><span data-stu-id="acec0-205">Create a rule to file mail items from a manager and flag them for follow-up</span></span>](how-to-create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up.md)
- [<span data-ttu-id="acec0-206">Мгновенное выполнение правила</span><span class="sxs-lookup"><span data-stu-id="acec0-206">Execute a rule instantly</span></span>](how-to-execute-a-rule-instantly.md)
- [<span data-ttu-id="acec0-207">Выполнение правила на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="acec0-207">Execute a rule on a local computer</span></span>](how-to-execute-a-rule-on-a-local-computer.md)
- [<span data-ttu-id="acec0-208">Создание правила для назначения категорий почтовым элементам с учетом нескольких слов в теме</span><span class="sxs-lookup"><span data-stu-id="acec0-208">Create a rule to assign categories to mail items based on multiple words in the subject</span></span>](how-to-create-a-rule-to-assign-categories-to-mail-items-based-on-multiple-words-in-the-subject.md)


[<span data-ttu-id="acec0-209">Примеры задач, в которых используются события Outlook</span><span class="sxs-lookup"><span data-stu-id="acec0-209">Sample tasks using Outlook events</span></span>](sample-tasks-using-outlook-events.md)

- [<span data-ttu-id="acec0-210">Реализация оболочки для инспекторов и отслеживание событий уровня элемента в каждом инспекторе</span><span class="sxs-lookup"><span data-stu-id="acec0-210">Implement a wrapper for inspectors and track item-level events in each inspector</span></span>](how-to-implement-a-wrapper-for-inspectors-and-track-item-level-events-in-each-inspector.md)

[<span data-ttu-id="acec0-211">Поиск и фильтрация</span><span class="sxs-lookup"><span data-stu-id="acec0-211">Search and filter</span></span>](search-and-filter.md)

- [<span data-ttu-id="acec0-212">Фильтрация и эффективное перечисление элементов в папке</span><span class="sxs-lookup"><span data-stu-id="acec0-212">Filter and efficiently enumerate items in a folder</span></span>](how-to-filter-and-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="acec0-213">Эффективное перечисление элементов в папке с помощью метода SetColumns</span><span class="sxs-lookup"><span data-stu-id="acec0-213">Use SetColumns to efficiently enumerate items in a folder</span></span>](how-to-use-setcolumns-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="acec0-214">Эффективное перечисление элементов в папке с помощью массивов</span><span class="sxs-lookup"><span data-stu-id="acec0-214">Use arrays to efficiently enumerate items in a folder</span></span>](how-to-use-arrays-to-efficiently-enumerate-items-in-a-folder.md)
- [<span data-ttu-id="acec0-215">Перечисление элементов в папке "Входящие" с учетом времени последнего изменения</span><span class="sxs-lookup"><span data-stu-id="acec0-215">Enumerate items in the Inbox based on the last modification time</span></span>](how-to-enumerate-items-in-the-inbox-based-on-the-last-modification-time.md)
- [<span data-ttu-id="acec0-216">Фильтрация и отображение элементов папки "Входящие", измененных в прошлом месяце</span><span class="sxs-lookup"><span data-stu-id="acec0-216">Filter and display Inbox items modified in the last month</span></span>](how-to-filter-and-display-inbox-items-modified-in-the-last-month.md)
- [<span data-ttu-id="acec0-217">Фильтрация и отображение многозначных свойств при перечислении элементов в папке</span><span class="sxs-lookup"><span data-stu-id="acec0-217">Filter and display multivalued properties when enumerating items in a folder</span></span>](how-to-filter-and-display-multivalued-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="acec0-218">Фильтрация и отображение вычисляемых свойств при перечислении элементов в папке</span><span class="sxs-lookup"><span data-stu-id="acec0-218">Filter and display computed properties when enumerating items in a folder</span></span>](how-to-filter-and-display-computed-properties-when-enumerating-items-in-a-folder.md)
- [<span data-ttu-id="acec0-219">Перечисление скрытых элементов в папке</span><span class="sxs-lookup"><span data-stu-id="acec0-219">Enumerate hidden items in a folder</span></span>](how-to-enumerate-hidden-items-in-a-folder.md)
- [<span data-ttu-id="acec0-220">Поиск фразы в теме во всех папках и хранилищах с помощью мгновенного поиска</span><span class="sxs-lookup"><span data-stu-id="acec0-220">Use instant search to search all folders and all stores for a phrase in the subject</span></span>](how-to-use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject.md)
- [<span data-ttu-id="acec0-221">Поиск фразы в тексте элементов в папке</span><span class="sxs-lookup"><span data-stu-id="acec0-221">Search for a phrase in the body of items in a folder</span></span>](how-to-search-for-a-phrase-in-the-body-of-items-in-a-folder.md)
- [<span data-ttu-id="acec0-222">Поиск точной фразы во вложениях элементов в папке</span><span class="sxs-lookup"><span data-stu-id="acec0-222">Search attachments of items in a folder for an exact phrase</span></span>](how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase.md)
- [<span data-ttu-id="acec0-223">Поиск и получение встреч в диапазоне времени</span><span class="sxs-lookup"><span data-stu-id="acec0-223">Search and obtain appointments in a time range</span></span>](how-to-search-and-obtain-appointments-in-a-time-range.md)
- [<span data-ttu-id="acec0-224">Фильтрация повторяющихся встреч и поиск строки в теме</span><span class="sxs-lookup"><span data-stu-id="acec0-224">Filter recurring appointments and search for a string in the subject</span></span>](how-to-filter-recurring-appointments-and-search-for-a-string-in-the-subject.md)
- [<span data-ttu-id="acec0-225">Поиск и получение элементов в общем представлении</span><span class="sxs-lookup"><span data-stu-id="acec0-225">Search and obtain items in an aggregated view</span></span>](how-to-search-and-obtain-items-in-an-aggregated-view.md)

[<span data-ttu-id="acec0-226">Сеансы</span><span class="sxs-lookup"><span data-stu-id="acec0-226">Sessions</span></span>](sessions.md)

- [<span data-ttu-id="acec0-227">Получение экземпляра Outlook и вход в него</span><span class="sxs-lookup"><span data-stu-id="acec0-227">Get and sign in to an instance of Outlook</span></span>](how-to-get-and-log-on-to-an-instance-of-outlook.md)

[<span data-ttu-id="acec0-228">Хранилища</span><span class="sxs-lookup"><span data-stu-id="acec0-228">Stores</span></span>](stores.md)

- [<span data-ttu-id="acec0-229">Получение сведений о хранилищах в профиле</span><span class="sxs-lookup"><span data-stu-id="acec0-229">Get information about stores in a profile</span></span>](how-to-get-information-about-stores-in-a-profile.md)
- [<span data-ttu-id="acec0-230">Добавление и удаление хранилища</span><span class="sxs-lookup"><span data-stu-id="acec0-230">Add or remove a store</span></span>](how-to-add-or-remove-a-store.md)

[<span data-ttu-id="acec0-231">Задачи</span><span class="sxs-lookup"><span data-stu-id="acec0-231">Tasks</span></span>](tasks.md)

- [<span data-ttu-id="acec0-232">Создание элемента задачи</span><span class="sxs-lookup"><span data-stu-id="acec0-232">Create a task item</span></span>](how-to-create-a-task-item.md)
- [<span data-ttu-id="acec0-233">Назначение задачи получателю</span><span class="sxs-lookup"><span data-stu-id="acec0-233">Assign a task to a recipient</span></span>](how-to-assign-a-task-to-a-recipient.md)
- [<span data-ttu-id="acec0-234">Отображение элементов запроса выполнения задачи, отправленных получателю</span><span class="sxs-lookup"><span data-stu-id="acec0-234">Display the task request items sent to a recipient</span></span>](how-to-display-the-task-request-items-sent-to-a-recipient.md)
- [<span data-ttu-id="acec0-235">Ответ на элемент запроса выполнения задачи</span><span class="sxs-lookup"><span data-stu-id="acec0-235">Respond to a task request item</span></span>](how-to-respond-to-a-task-request-item.md)
- [<span data-ttu-id="acec0-236">Создание повторяющейся задачи</span><span class="sxs-lookup"><span data-stu-id="acec0-236">Create a recurring task</span></span>](how-to-create-a-recurring-task.md)
- [<span data-ttu-id="acec0-237">Пометка почтовых элементов от руководителя к исполнению</span><span class="sxs-lookup"><span data-stu-id="acec0-237">Flag mail items from a manager for follow-up</span></span>](how-to-flag-mail-items-from-a-manager-for-follow-up.md)

[<span data-ttu-id="acec0-238">Представления</span><span class="sxs-lookup"><span data-stu-id="acec0-238">Views</span></span>](views.md)

- [<span data-ttu-id="acec0-239">Создание представления</span><span class="sxs-lookup"><span data-stu-id="acec0-239">Create a view</span></span>](how-to-create-a-view.md)
- [<span data-ttu-id="acec0-240">Добавление полей в представление</span><span class="sxs-lookup"><span data-stu-id="acec0-240">Add fields to a view</span></span>](how-to-add-fields-to-a-view.md)
- [<span data-ttu-id="acec0-241">Перечисление элементов в табличном представлении</span><span class="sxs-lookup"><span data-stu-id="acec0-241">Enumerate items in a table view</span></span>](how-to-enumerate-items-in-a-table-view.md)



