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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320988"
---
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="98e42-103">Раздел "файл конфигурации формы" [описание]</span><span class="sxs-lookup"><span data-stu-id="98e42-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="98e42-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98e42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98e42-105">В разделе **[Description]** перечислены все свойства формы, связанные с элементами управления в пользовательском интерфейсе формы, а также атрибуты, используемые при поиске формы.</span><span class="sxs-lookup"><span data-stu-id="98e42-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="98e42-106">Записи **MessageClass**, **CLSID**и **DisplayName** , которые идентифицируют имя класса сообщений формы, его GUID и отображаемое имя класса сообщения, соответственно, являются обязательными записями, используемыми для поиска формы в библиотеке форм. .</span><span class="sxs-lookup"><span data-stu-id="98e42-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="98e42-107">Остальные элементы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="98e42-107">The remaining entries are optional.</span></span> <span data-ttu-id="98e42-108">Формат раздела **[Description]** :</span><span class="sxs-lookup"><span data-stu-id="98e42-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="98e42-109">В разделе **[Description]** перечислены все свойства формы, связанные с элементами управления в пользовательском интерфейсе формы, а также атрибуты, используемые при поиске формы.</span><span class="sxs-lookup"><span data-stu-id="98e42-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="98e42-110">Записи **MessageClass**, **CLSID**и **DisplayName** , которые идентифицируют имя класса сообщений формы, его GUID и отображаемое имя класса сообщения, соответственно, являются обязательными записями, используемыми для поиска формы в библиотеке форм. .</span><span class="sxs-lookup"><span data-stu-id="98e42-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="98e42-111">Остальные элементы являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="98e42-111">The remaining entries are optional.</span></span> <span data-ttu-id="98e42-112">Формат раздела **[Description]** :</span><span class="sxs-lookup"><span data-stu-id="98e42-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="98e42-113">\*\*Обзор \*\* =  _Строка_ MessageClass</span><span class="sxs-lookup"><span data-stu-id="98e42-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="98e42-114">\*\*\*\* =  _GUID_ CLSID</span><span class="sxs-lookup"><span data-stu-id="98e42-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="98e42-115">**DisplayName** =  _дисплайедстринг_</span><span class="sxs-lookup"><span data-stu-id="98e42-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="98e42-116">\*\*\*\* =  _Путь_ смалликон</span><span class="sxs-lookup"><span data-stu-id="98e42-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="98e42-117">\*\*\*\* =  _Путь_ ларжеикон</span><span class="sxs-lookup"><span data-stu-id="98e42-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="98e42-118">НеОбязательные записи:</span><span class="sxs-lookup"><span data-stu-id="98e42-118">Optional entries are:</span></span>
  
 <span data-ttu-id="98e42-119">\*\*\*\* =  _Строка_ , отображаемая в категории</span><span class="sxs-lookup"><span data-stu-id="98e42-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="98e42-120">\*\*\*\* =  _Отображаемая строка_ подкатегории</span><span class="sxs-lookup"><span data-stu-id="98e42-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="98e42-121">\*\*\*\* =  _Строка_ , отображаемая в комментарии</span><span class="sxs-lookup"><span data-stu-id="98e42-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="98e42-122">\*\*\*\* =  _Строка_ , отображаемая владельцем</span><span class="sxs-lookup"><span data-stu-id="98e42-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="98e42-123">\*\*\*\* =  _Отображаемая строка_ числа</span><span class="sxs-lookup"><span data-stu-id="98e42-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="98e42-124">**Версия** =  _целого числа_</span><span class="sxs-lookup"><span data-stu-id="98e42-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="98e42-125">\*\*\*\* =  _Строка_ языкового стандарта</span><span class="sxs-lookup"><span data-stu-id="98e42-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="98e42-126">**Скрытое** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="98e42-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="98e42-127">\*\*\*\* =  _Строка_ десигнертулнаме</span><span class="sxs-lookup"><span data-stu-id="98e42-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="98e42-128">**Десигнертулгуид** =  _CLSID_</span><span class="sxs-lookup"><span data-stu-id="98e42-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="98e42-129">**Десигнеррунтимегуид** =  _CLSID_</span><span class="sxs-lookup"><span data-stu-id="98e42-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="98e42-130">**Компосеинфолдер** =  _0 | 1_</span><span class="sxs-lookup"><span data-stu-id="98e42-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="98e42-131">\*\*\*\* =  _Строка_ компосекомманд</span><span class="sxs-lookup"><span data-stu-id="98e42-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="98e42-132">Записи **категорий** и **подкатегорий** используются установщиками форм для настройки категоризации форм по умолчанию в пользовательском интерфейсе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="98e42-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="98e42-133">Например, можно настроить иерархию, где "Служба технической поддержки" — Категория, а "программное обеспечение" и "оборудование" — подкатегории.</span><span class="sxs-lookup"><span data-stu-id="98e42-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="98e42-134">Эту классификацию можно использовать в приложениях средств просмотра для более организованного отображения сообщений.</span><span class="sxs-lookup"><span data-stu-id="98e42-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="98e42-135">Записи **comment**, **owner**и **Number** — это все строки комментариев, которые отображаются в пользовательском интерфейсе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="98e42-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="98e42-136">Это специальные свойства, которые могут использоваться разработчиками форм по собственному усмотрению.</span><span class="sxs-lookup"><span data-stu-id="98e42-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="98e42-137">Например, запись **комментария** можно использовать для указания цели формы, записи **владельца** , которая указывает человека или организацию, ответственной за сопровождение формы, а также число, используемое для отслеживания разных версий формы.</span><span class="sxs-lookup"><span data-stu-id="98e42-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="98e42-138">Для записи **комментария** можно включить до десяти строк комментариев.</span><span class="sxs-lookup"><span data-stu-id="98e42-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="98e42-139">Первая строка комментариев использует слово "Comment" в качестве ключа, вторая строка комментариев — "Comment1" в качестве ключа и так далее через "Comment9".</span><span class="sxs-lookup"><span data-stu-id="98e42-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="98e42-140">Записи **ларжеикон** и **смалликон** используются для указания пути к ресурсам значков, используемым для отображения значков в пользовательском интерфейсе клиентского приложения, обычно это относится к строкам таблицы, включающим **пр_икон** ([PidTagIcon](pidtagicon-canonical-property.md)). столбцы свойств или **пр_мини_икон** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="98e42-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="98e42-141">Имена файлов значков могут быть указаны в виде путей относительно каталога, в котором установлен файл конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="98e42-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="98e42-142">Запись **Version** используется для указания номера версии формы.</span><span class="sxs-lookup"><span data-stu-id="98e42-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="98e42-143">**Locale** — это трехбуквенный идентификатор языка конечной библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="98e42-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="98e42-144">Список этих идентификаторов можно найти в справочнике программиста _Win32_.</span><span class="sxs-lookup"><span data-stu-id="98e42-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="98e42-145">**Скрытая** запись указывает, следует ли отображать форму в пользовательском интерфейсе поставщика библиотеки форм: значение 1 указывает, что файл скрыт, а 0 указывает на то, что форма отображается.</span><span class="sxs-lookup"><span data-stu-id="98e42-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="98e42-146">Ниже приведен пример файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="98e42-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="98e42-147">Запись **компосеинфолдер** определяет, будет ли форма размещается в текущей папке или в папке "Входящие" пользователя, когда пользователь сохраняет сообщение при его создании: 1 указывает, что форма должна перейти в текущую папку, а 0 — Перейдите в папку "Входящие".</span><span class="sxs-lookup"><span data-stu-id="98e42-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="98e42-148">Запись **компосекомманд** — это строка, которую необходимо поместить в меню создания клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="98e42-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="98e42-149">Если этот параметр не указан, будет использоваться запись **DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="98e42-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


