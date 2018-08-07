---
title: 'Файл конфигурации формы: раздел [Описание]'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4ce91a65-17db-4ee2-ad59-01fd5b1f1ea7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d3673c3b10afb55121339e335163ce9b2e5937e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808463"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="10927-103">Файл конфигурации формы: раздел [Описание]</span><span class="sxs-lookup"><span data-stu-id="10927-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="10927-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10927-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10927-105">В разделе **[Описание]** перечислены все свойства формы, связанные с элементами управления в форму пользовательского интерфейса, а также атрибуты, используемые при поиске формы.</span><span class="sxs-lookup"><span data-stu-id="10927-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="10927-106">**MessageClass**, **отображаемое имя** записи, которые идентифицируют имя класса сообщений формы, его GUID и отображаемое имя класса сообщения, соответственно и **Clsid**, необходимые записи, используемые для нахождения формы в библиотеке форм .</span><span class="sxs-lookup"><span data-stu-id="10927-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="10927-107">Оставшиеся записи являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="10927-107">The remaining entries are optional.</span></span> <span data-ttu-id="10927-108">Имеет формат в разделе **[Описание]** :</span><span class="sxs-lookup"><span data-stu-id="10927-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="10927-109">В разделе **[Описание]** перечислены все свойства формы, связанные с элементами управления в форму пользовательского интерфейса, а также атрибуты, используемые при поиске формы.</span><span class="sxs-lookup"><span data-stu-id="10927-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="10927-110">**MessageClass**, **отображаемое имя** записи, которые идентифицируют имя класса сообщений формы, его GUID и отображаемое имя класса сообщения, соответственно и **Clsid**, необходимые записи, используемые для нахождения формы в библиотеке форм .</span><span class="sxs-lookup"><span data-stu-id="10927-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="10927-111">Оставшиеся записи являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="10927-111">The remaining entries are optional.</span></span> <span data-ttu-id="10927-112">Имеет формат в разделе **[Описание]** :</span><span class="sxs-lookup"><span data-stu-id="10927-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="10927-113">**[Описание] MessageClass** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="10927-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="10927-114">**CLSID** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="10927-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="10927-115">**Отображаемое имя** =  _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="10927-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="10927-116">**SmallIcon** =  _путь_</span><span class="sxs-lookup"><span data-stu-id="10927-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="10927-117">**LargeIcon** =  _путь_</span><span class="sxs-lookup"><span data-stu-id="10927-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="10927-118">Необязательный записи являются:</span><span class="sxs-lookup"><span data-stu-id="10927-118">Optional entries are:</span></span>
  
 <span data-ttu-id="10927-119">**Категория** =  _отображается строка_</span><span class="sxs-lookup"><span data-stu-id="10927-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="10927-120">**Подкатегория** =  _отображается строка_</span><span class="sxs-lookup"><span data-stu-id="10927-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="10927-121">**Комментарий** =  _отображается строка_</span><span class="sxs-lookup"><span data-stu-id="10927-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="10927-122">**Владелец** =  _отображается строка_</span><span class="sxs-lookup"><span data-stu-id="10927-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="10927-123">**Номер** =  _отображается строка_</span><span class="sxs-lookup"><span data-stu-id="10927-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="10927-124">**Версия** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="10927-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="10927-125">**Языковой стандарт** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="10927-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="10927-126">**Скрытые** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="10927-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="10927-127">**DesignerToolName** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="10927-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="10927-128">**DesignerToolGuid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="10927-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="10927-129">**DesignerRuntimeGuid** =  _clsid_</span><span class="sxs-lookup"><span data-stu-id="10927-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="10927-130">**ComposeInFolder** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="10927-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="10927-131">**ComposeCommand** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="10927-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="10927-132">**Категории** и **подкатегории** записи используются для настройки по умолчанию категоризации форм в клиентском приложении пользовательский интерфейс с формы программы установки.</span><span class="sxs-lookup"><span data-stu-id="10927-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="10927-133">Пример иерархии могут быть настроены где категории «Help Desk» и «Software» и «Hardware» были подкатегории.</span><span class="sxs-lookup"><span data-stu-id="10927-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="10927-134">Данная классификация может использоваться приложениями средства просмотра для отображения сообщения в более организованные способом.</span><span class="sxs-lookup"><span data-stu-id="10927-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="10927-135">**Комментарий**, **владельца**и **номер** отображаются все строки комментариев, которые отображаются в клиентском приложении пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="10927-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="10927-136">Это формы определенные свойства, которые могут использоваться в соответствии с разработчик формы.</span><span class="sxs-lookup"><span data-stu-id="10927-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="10927-137">Например запись **комментария** можно использовать для назначению формы, запись **владельца** , служит для указания лицо или организация, ответственность за обеспечение формы и номер, используемый для отслеживания различных версию формы.</span><span class="sxs-lookup"><span data-stu-id="10927-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="10927-138">**Комментарий** можно включить запись до десяти строк комментариев.</span><span class="sxs-lookup"><span data-stu-id="10927-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="10927-139">Первая строка комментарии использует word «Примечания» как ключ, во второй строке комментарии «Comment1» как ключ, и так далее до «Comment9».</span><span class="sxs-lookup"><span data-stu-id="10927-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="10927-140">Записи **LargeIcon** и **SmallIcon** используются для указания пути значок ресурсов, используемых для отображения значков в клиентском приложении пользовательский интерфейс, обычно используется для строк таблицы, включая **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) или столбцы свойств **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="10927-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="10927-141">Имена файлов значков могут быть присвоены пути к каталогу, где установлен файл конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="10927-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="10927-142">Запись **версии** используется для указания номера версии формы.</span><span class="sxs-lookup"><span data-stu-id="10927-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="10927-143">**Языковой стандарт** — это идентификатор языка трех букв библиотеки форм назначения.</span><span class="sxs-lookup"><span data-stu-id="10927-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="10927-144">Список этих идентификаторов можно найти в _Справочник программиста Win32_.</span><span class="sxs-lookup"><span data-stu-id="10927-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="10927-145">Запись **Hidden** указывает, отображаются ли форма в пользовательском интерфейсе поставщика библиотеки форм: 1 означает, что файл является скрытым и 0 указывает, что форма отображается.</span><span class="sxs-lookup"><span data-stu-id="10927-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="10927-146">Ниже представлен пример файла конфигурации формы отображается после.</span><span class="sxs-lookup"><span data-stu-id="10927-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="10927-147">Запись **ComposeInFolder** определяет, предназначен ли форма должна размещаться в текущую папку или в папку Входящие», когда пользователь сохраняет сообщения при его создании: 1 означает, что форма добавляется в текущую папку и 0 указывает, что следует Перейдите в папку "Входящие".</span><span class="sxs-lookup"><span data-stu-id="10927-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="10927-148">Запись **ComposeCommand** — это строка должна размещаться в клиентском приложении 's создания меню.</span><span class="sxs-lookup"><span data-stu-id="10927-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="10927-149">Если этот параметр не указан, будет использоваться запись **DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="10927-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


