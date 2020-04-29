---
title: Раздел "файл конфигурации формы" [описание]
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
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="e7ac0-103">Раздел "файл конфигурации формы" [описание]</span><span class="sxs-lookup"><span data-stu-id="e7ac0-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="e7ac0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7ac0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7ac0-105">В разделе **[Description]** перечислены все свойства формы, связанные с элементами управления в пользовательском интерфейсе формы, а также атрибуты, используемые при поиске формы.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="e7ac0-106">Записи **MessageClass**, **CLSID**и **DisplayName** , которые определяют имя класса сообщений формы, его GUID и отображаемое имя класса сообщения, соответственно, являются обязательными записями, используемыми для поиска формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="e7ac0-107">Остальные элементы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-107">The remaining entries are optional.</span></span> <span data-ttu-id="e7ac0-108">Формат раздела **[Description]** :</span><span class="sxs-lookup"><span data-stu-id="e7ac0-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="e7ac0-109">В разделе **[Description]** перечислены все свойства формы, связанные с элементами управления в пользовательском интерфейсе формы, а также атрибуты, используемые при поиске формы.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="e7ac0-110">Записи **MessageClass**, **CLSID**и **DisplayName** , которые определяют имя класса сообщений формы, его GUID и отображаемое имя класса сообщения, соответственно, являются обязательными записями, используемыми для поиска формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="e7ac0-111">Остальные элементы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-111">The remaining entries are optional.</span></span> <span data-ttu-id="e7ac0-112">Формат раздела **[Description]** :</span><span class="sxs-lookup"><span data-stu-id="e7ac0-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="e7ac0-113">\*\*Обзор \*\* =  _Строка_ MessageClass</span><span class="sxs-lookup"><span data-stu-id="e7ac0-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="e7ac0-114">**Clsid** =  _GUID_ CLSID</span><span class="sxs-lookup"><span data-stu-id="e7ac0-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="e7ac0-115">**DisplayName** =  _дисплайедстринг_</span><span class="sxs-lookup"><span data-stu-id="e7ac0-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="e7ac0-116">**SmallIcon** =  _Путь_ смалликон</span><span class="sxs-lookup"><span data-stu-id="e7ac0-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="e7ac0-117">**LargeIcon** =  _Путь_ ларжеикон</span><span class="sxs-lookup"><span data-stu-id="e7ac0-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="e7ac0-118">Необязательные записи:</span><span class="sxs-lookup"><span data-stu-id="e7ac0-118">Optional entries are:</span></span>
  
 <span data-ttu-id="e7ac0-119">**Category** =  _Строка, отображаемая_ в категории</span><span class="sxs-lookup"><span data-stu-id="e7ac0-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="e7ac0-120">**Subcategory** =  _Отображаемая строка_ подкатегории</span><span class="sxs-lookup"><span data-stu-id="e7ac0-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="e7ac0-121">**Comment** =  _Строка, отображаемая_ в комментарии</span><span class="sxs-lookup"><span data-stu-id="e7ac0-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="e7ac0-122">**Owner** =  _Строка, отображаемая_ владельцем</span><span class="sxs-lookup"><span data-stu-id="e7ac0-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="e7ac0-123">**Number** =  _Отображаемая строка_ числа</span><span class="sxs-lookup"><span data-stu-id="e7ac0-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="e7ac0-124">**Версия** =  _целого числа_</span><span class="sxs-lookup"><span data-stu-id="e7ac0-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="e7ac0-125">**Строка языкового стандарта** =  _string_</span><span class="sxs-lookup"><span data-stu-id="e7ac0-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="e7ac0-126">**Скрытое** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="e7ac0-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="e7ac0-127">**DesignerToolName** =  _Строка_ десигнертулнаме</span><span class="sxs-lookup"><span data-stu-id="e7ac0-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="e7ac0-128">**Десигнертулгуид** =  _CLSID_</span><span class="sxs-lookup"><span data-stu-id="e7ac0-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="e7ac0-129">**Десигнеррунтимегуид** =  _CLSID_</span><span class="sxs-lookup"><span data-stu-id="e7ac0-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="e7ac0-130">**Компосеинфолдер** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="e7ac0-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="e7ac0-131">**ComposeCommand** =  _Строка_ компосекомманд</span><span class="sxs-lookup"><span data-stu-id="e7ac0-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="e7ac0-132">Записи **категорий** и **подкатегорий** используются установщиками форм для настройки категоризации форм по умолчанию в пользовательском интерфейсе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="e7ac0-133">Например, можно настроить иерархию, где "Служба технической поддержки" — Категория, а "программное обеспечение" и "оборудование" — подкатегории.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="e7ac0-134">Эту классификацию можно использовать в приложениях средств просмотра для более организованного отображения сообщений.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="e7ac0-135">Записи **comment**, **owner**и **Number** — это все строки комментариев, которые отображаются в пользовательском интерфейсе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="e7ac0-136">Это специальные свойства, которые могут использоваться разработчиками форм по собственному усмотрению.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="e7ac0-137">Например, запись **комментария** можно использовать для указания цели формы, записи **владельца** , которая указывает человека или организацию, ответственной за сопровождение формы, а также число, используемое для отслеживания разных версий формы.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="e7ac0-138">Для записи **комментария** можно включить до десяти строк комментариев.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="e7ac0-139">Первая строка комментариев использует слово "Comment" в качестве ключа, вторая строка комментариев — "Comment1" в качестве ключа и так далее через "Comment9".</span><span class="sxs-lookup"><span data-stu-id="e7ac0-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="e7ac0-140">Записи **ларжеикон** и **смалликон** используются для указания пути для ресурсов значков, используемых для отображения значков в пользовательском интерфейсе клиентского приложения, обычно это относится к строкам таблицы, включающим столбцы свойств **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) или **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e7ac0-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="e7ac0-141">Имена файлов значков могут быть указаны в виде путей относительно каталога, в котором установлен файл конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="e7ac0-142">Запись **Version** используется для указания номера версии формы.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="e7ac0-143">**Locale** — это трехбуквенный идентификатор языка конечной библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="e7ac0-144">Список этих идентификаторов можно найти в _справочнике программиста Win32_.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="e7ac0-145">**Скрытая** запись указывает, следует ли отображать форму в пользовательском интерфейсе поставщика библиотеки форм: значение 1 указывает, что файл скрыт, а 0 указывает на то, что форма отображается.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="e7ac0-146">Ниже приведен пример файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="e7ac0-147">Запись **компосеинфолдер** определяет, будет ли форма размещаться в текущей папке или в папке "Входящие" пользователя, когда пользователь сохраняет сообщение при его создании: 1 указывает, что форма должна находиться в текущей папке, а 0 — в папке "Входящие".</span><span class="sxs-lookup"><span data-stu-id="e7ac0-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="e7ac0-148">Запись **компосекомманд** — это строка, которую необходимо поместить в меню создания клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="e7ac0-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="e7ac0-149">Если этот параметр не указан, будет использоваться запись **DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="e7ac0-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


