---
title: Раздел Конфигурация формы [Описание]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ddc59d6c503d44a0575679fce694cc34499d8e2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433096"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="aec58-103">Раздел Конфигурация формы [Описание]</span><span class="sxs-lookup"><span data-stu-id="aec58-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="aec58-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aec58-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aec58-105">В **разделе [Описание]** перечислены все свойства формы, связанные с элементами управления в пользовательском интерфейсе формы, а также атрибуты, используемые при поиске формы.</span><span class="sxs-lookup"><span data-stu-id="aec58-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="aec58-106">Записи **MessageClass,** **Clsid** и **DisplayName,** которые определяют имя класса сообщений формы, его GUID и отображаемого имени класса сообщений, соответственно, требуются записи, используемые для определения формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="aec58-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="aec58-107">Остальные записи необязательны.</span><span class="sxs-lookup"><span data-stu-id="aec58-107">The remaining entries are optional.</span></span> <span data-ttu-id="aec58-108">Формат раздела **[Описание]:**</span><span class="sxs-lookup"><span data-stu-id="aec58-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="aec58-109">В **разделе [Описание]** перечислены все свойства формы, связанные с элементами управления в пользовательском интерфейсе формы, а также атрибуты, используемые при поиске формы.</span><span class="sxs-lookup"><span data-stu-id="aec58-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="aec58-110">Записи **MessageClass,** **Clsid** и **DisplayName,** которые определяют имя класса сообщений формы, его GUID и отображаемого имени класса сообщений, соответственно, требуются записи, используемые для определения формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="aec58-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="aec58-111">Остальные записи необязательны.</span><span class="sxs-lookup"><span data-stu-id="aec58-111">The remaining entries are optional.</span></span> <span data-ttu-id="aec58-112">Формат раздела **[Описание]:**</span><span class="sxs-lookup"><span data-stu-id="aec58-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="aec58-113">**[Описание] MessageClass**  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="aec58-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="aec58-114">**Clsid**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="aec58-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="aec58-115">**DisplayName**  =   _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="aec58-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="aec58-116">**SmallIcon**  =   _путь_</span><span class="sxs-lookup"><span data-stu-id="aec58-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="aec58-117">**LargeIcon**  =   _путь_</span><span class="sxs-lookup"><span data-stu-id="aec58-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="aec58-118">Необязательные записи:</span><span class="sxs-lookup"><span data-stu-id="aec58-118">Optional entries are:</span></span>
  
 <span data-ttu-id="aec58-119">**Категория**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="aec58-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="aec58-120">**Subcategory**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="aec58-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="aec58-121">**Комментарий**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="aec58-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="aec58-122">**Владелец**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="aec58-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="aec58-123">**Номер**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="aec58-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="aec58-124">**Версия**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="aec58-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="aec58-125">**Locale**  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="aec58-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="aec58-126">**Скрытые**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="aec58-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="aec58-127">**DesignerToolName**  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="aec58-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="aec58-128">**DesignerToolGuid**  =   _clsid_</span><span class="sxs-lookup"><span data-stu-id="aec58-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="aec58-129">**DesignerRuntimeGuid**  =   _clsid_</span><span class="sxs-lookup"><span data-stu-id="aec58-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="aec58-130">**ComposeInFolder**  =   _0|1_</span><span class="sxs-lookup"><span data-stu-id="aec58-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="aec58-131">**ComposeCommand**  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="aec58-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="aec58-132">Записи **Category** и **Subcategory** используются установщиками форм для настройки классификации форм по умолчанию в пользовательском интерфейсе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="aec58-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="aec58-133">Например, можно настроить иерархию, в которой подкатегории — "Стол поддержки", а подкатегории — "Программное обеспечение" и "Оборудование".</span><span class="sxs-lookup"><span data-stu-id="aec58-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="aec58-134">Эта классификация может использоваться приложениями просмотра для отображения сообщений более организованным образом.</span><span class="sxs-lookup"><span data-stu-id="aec58-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="aec58-135">Записи **Comment,** **Owner** и **Number** — это строки комментариев, которые отображаются в пользовательском интерфейсе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="aec58-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="aec58-136">Это конкретные свойства форм, которые можно использовать по усмотрению разработчика форм.</span><span class="sxs-lookup"><span data-stu-id="aec58-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="aec58-137">Например, запись **Comment** можно использовать для указать цель  формы, запись Владельца, используемую для указать лицо или организацию, ответственные за сохранение формы, и номер, используемый для отслеживания различных версий формы.</span><span class="sxs-lookup"><span data-stu-id="aec58-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="aec58-138">Для **записи Комментарий** можно включить до десяти строк комментариев.</span><span class="sxs-lookup"><span data-stu-id="aec58-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="aec58-139">В первой строке комментариев в качестве ключа используется слово "Комментарий", во второй строке в качестве ключа используется "Comment1" и так далее через "Comment9".</span><span class="sxs-lookup"><span data-stu-id="aec58-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="aec58-140">Записи **LargeIcon** и SmallIcon используются для указания пути для ресурсов значков, используемых для отображения значков в пользовательском интерфейсе клиентского приложения, как правило, это для строк таблицы, которые включают **столбцы свойств PR_ICON** [(PidTagIcon)](pidtagicon-canonical-property.md)или **PR_MINI_ICON** [(PidTagMiniIcon).](pidtagminiicon-canonical-property.md) </span><span class="sxs-lookup"><span data-stu-id="aec58-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="aec58-141">Имена файлов icon можно укаменовать как имена путей относительно каталога, в котором установлен файл конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="aec58-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="aec58-142">Запись **Версия** используется для указать номер версии формы.</span><span class="sxs-lookup"><span data-stu-id="aec58-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="aec58-143">**Locale** — это идентификатор языка с тремя буквами в библиотеке форм назначения.</span><span class="sxs-lookup"><span data-stu-id="aec58-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="aec58-144">Список этих идентификаторов можно найти в справке  _программиста Win32_.</span><span class="sxs-lookup"><span data-stu-id="aec58-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="aec58-145">**Скрытая** запись указывает, должна ли форма отображаться в пользовательском интерфейсе поставщика библиотеки форм: 1 указывает, что файл скрыт, а 0 указывает, что форма видна.</span><span class="sxs-lookup"><span data-stu-id="aec58-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="aec58-146">Пример файла конфигурации формы показан ниже.</span><span class="sxs-lookup"><span data-stu-id="aec58-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="aec58-147">Запись **ComposeInFolder** контролирует, предназначена ли форма для размещения в текущей папке или в папке "Входящие" пользователя, когда пользователь сохраняет сообщение при его записи: 1 указывает, что форма должна идти в текущей папке, а 0 указывает, что она должна быть в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="aec58-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="aec58-148">Запись **ComposeCommand** — это строка, которая будет помещена в меню составить приложение клиента.</span><span class="sxs-lookup"><span data-stu-id="aec58-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="aec58-149">Если это не указано, будет использоваться запись **DisplayName.**</span><span class="sxs-lookup"><span data-stu-id="aec58-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
```cpp
[Description]
MessageClass = IPM.Help
Clsid = {00020D31-0000-0000-C000-000000000046}
DisplayName = Help Desk Request Form
;optional entries
Category = Help Desk Requests
Subcategory = New Requests
Comment = Use this form to request network assistance
Owner = Help Desk
Number = 1
SmallIcon = C:\WINDOWS|EFORMS\HELPDESK\HDSMALL.ICO
LargeIcon = C:\WINDOWS|EFORMS\HELPDESK\HDLARGE.ICO
Version = 1.00
Locale = enu
Hidden = 0
ComposeInFolder = 0
ComposeCommand = &Help Desk Request
 
```


