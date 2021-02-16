---
title: Файл конфигурации формы [описание] Раздел
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
# <a name="form-configuration-file-description-section"></a><span data-ttu-id="68d51-103">Файл конфигурации формы [описание] Раздел</span><span class="sxs-lookup"><span data-stu-id="68d51-103">Form Configuration File [Description] Section</span></span>
 
<span data-ttu-id="68d51-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68d51-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68d51-105">В **разделе [Описание]** перечислены все свойства формы, связанные с элементами управления в пользовательском интерфейсе формы, а также атрибуты, используемые при поиске формы.</span><span class="sxs-lookup"><span data-stu-id="68d51-105">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="68d51-106">Записи **MessageClass,** **Clsid** и **DisplayName,** которые определяют имя класса сообщений формы, его GUID и отображаемое имя класса сообщений, соответственно, являются записями, используемыми для поиска формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="68d51-106">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="68d51-107">Остальные записи являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="68d51-107">The remaining entries are optional.</span></span> <span data-ttu-id="68d51-108">Формат раздела **[Описание]:**</span><span class="sxs-lookup"><span data-stu-id="68d51-108">The format of the **[Description]** section is:</span></span> 
  
<span data-ttu-id="68d51-109">В **разделе [Описание]** перечислены все свойства формы, связанные с элементами управления в пользовательском интерфейсе формы, а также атрибуты, используемые при поиске формы.</span><span class="sxs-lookup"><span data-stu-id="68d51-109">The **[Description]** section lists all properties of the form that are associated with controls in the form's user interface, plus attributes that are used in locating the form.</span></span> <span data-ttu-id="68d51-110">Записи **MessageClass,** **Clsid** и **DisplayName,** которые определяют имя класса сообщений формы, его GUID и отображаемое имя класса сообщений, соответственно, являются записями, используемыми для поиска формы в библиотеке форм.</span><span class="sxs-lookup"><span data-stu-id="68d51-110">The **MessageClass**, **Clsid**, and **DisplayName** entries, which identify the name of the form's message class, its GUID, and the message class's display name, respectively, are required entries used to locate the form within the form library.</span></span> <span data-ttu-id="68d51-111">Остальные записи являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="68d51-111">The remaining entries are optional.</span></span> <span data-ttu-id="68d51-112">Формат раздела **[Описание]:**</span><span class="sxs-lookup"><span data-stu-id="68d51-112">The format of the **[Description]** section is:</span></span> 
  
 <span data-ttu-id="68d51-113">**[Description] MessageClass**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="68d51-113">**[Description] MessageClass** =  _string_</span></span>
  
 <span data-ttu-id="68d51-114">**Clsid**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="68d51-114">**Clsid** =  _guid_</span></span>
  
 <span data-ttu-id="68d51-115">**DisplayName**  =   _displayedstring_</span><span class="sxs-lookup"><span data-stu-id="68d51-115">**DisplayName** =  _displayedstring_</span></span>
  
 <span data-ttu-id="68d51-116">**SmallIcon**  =   _path_</span><span class="sxs-lookup"><span data-stu-id="68d51-116">**SmallIcon** =  _path_</span></span>
  
 <span data-ttu-id="68d51-117">**LargeIcon**  =   _path_</span><span class="sxs-lookup"><span data-stu-id="68d51-117">**LargeIcon** =  _path_</span></span>
  
<span data-ttu-id="68d51-118">Необязательные записи:</span><span class="sxs-lookup"><span data-stu-id="68d51-118">Optional entries are:</span></span>
  
 <span data-ttu-id="68d51-119">**Категория**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="68d51-119">**Category** =  _displayed string_</span></span>
  
 <span data-ttu-id="68d51-120">**Подкатегория**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="68d51-120">**Subcategory** =  _displayed string_</span></span>
  
 <span data-ttu-id="68d51-121">**Комментарий**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="68d51-121">**Comment** =  _displayed string_</span></span>
  
 <span data-ttu-id="68d51-122">**Владелец**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="68d51-122">**Owner** =  _displayed string_</span></span>
  
 <span data-ttu-id="68d51-123">**Number**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="68d51-123">**Number** =  _displayed string_</span></span>
  
 <span data-ttu-id="68d51-124">**Версия**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="68d51-124">**Version** =  _integer_</span></span>
  
 <span data-ttu-id="68d51-125">**Региональные органы**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="68d51-125">**Locale** =  _string_</span></span>
  
 <span data-ttu-id="68d51-126">**Hidden**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="68d51-126">**Hidden** =  _integer_</span></span>
  
 <span data-ttu-id="68d51-127">**DesignerToolName**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="68d51-127">**DesignerToolName** =  _string_</span></span>
  
 <span data-ttu-id="68d51-128">**DesignerToolGuid**  =   _clsid_</span><span class="sxs-lookup"><span data-stu-id="68d51-128">**DesignerToolGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="68d51-129">**DesignerRuntimeGuid**  =   _clsid_</span><span class="sxs-lookup"><span data-stu-id="68d51-129">**DesignerRuntimeGuid** =  _clsid_</span></span>
  
 <span data-ttu-id="68d51-130">**ComposeInFolder**  =   _0|1_</span><span class="sxs-lookup"><span data-stu-id="68d51-130">**ComposeInFolder** =  _0|1_</span></span>
  
 <span data-ttu-id="68d51-131">**ComposeCommand**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="68d51-131">**ComposeCommand** =  _string_</span></span>
  
<span data-ttu-id="68d51-132">Записи **категорий** и **подкатегорий** используются установщиками форм для настройки классификации форм по умолчанию в пользовательском интерфейсе клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="68d51-132">The **Category** and **Subcategory** entries are used by form installers to set up the default categorization of forms within client application's user interface.</span></span> <span data-ttu-id="68d51-133">Например, можно настроить иерархию, где "Help Desk" — это категория, а "Программное обеспечение" и "Оборудование" — подкатегории.</span><span class="sxs-lookup"><span data-stu-id="68d51-133">For example a hierarchy could be set up where "Help Desk" is the category and "Software" and "Hardware" were the subcategories.</span></span> <span data-ttu-id="68d51-134">Затем эта категоризация может использоваться приложениями для просмотра сообщений более уорганизацией.</span><span class="sxs-lookup"><span data-stu-id="68d51-134">This categorization can then be used by viewer applications to display messages in a more organized way.</span></span> <span data-ttu-id="68d51-135">Записи **"Комментарий", "Владелец"** и **"Номер"** — это все строки комментариев, которые отображаются в пользовательском интерфейсе клиентского приложения. </span><span class="sxs-lookup"><span data-stu-id="68d51-135">The **Comment**, **Owner**, and **Number** entries are all comment strings that appear in client application's user interface.</span></span> <span data-ttu-id="68d51-136">Это свойства конкретной формы, которые можно использовать по усмотрению разработчика формы.</span><span class="sxs-lookup"><span data-stu-id="68d51-136">These are form specific properties that can be used at the discretion of the form developer.</span></span> <span data-ttu-id="68d51-137">Например, запись **"Комментарий"** может использоваться для указать  назначение формы, запись владельца, используемую для указать лицо или организацию, ответственные за обслуживание формы, а также номер, используемый для отслеживания различных версий формы.</span><span class="sxs-lookup"><span data-stu-id="68d51-137">For example, the **Comment** entry can be used to indicate the purpose of the form, the **Owner** entry used to indicate the person or organization responsible for maintaining the form, and the number used to track different version of the form.</span></span> <span data-ttu-id="68d51-138">Для **записи** "Комментарий" можно включить до десяти строк комментариев.</span><span class="sxs-lookup"><span data-stu-id="68d51-138">For the **Comment** entry, up to ten lines of comments can be included.</span></span> <span data-ttu-id="68d51-139">В первой строке комментариев в качестве ключа используется слово "Comment", во второй строке комментариев в качестве ключа используется "Comment1" и так далее до "Comment9".</span><span class="sxs-lookup"><span data-stu-id="68d51-139">The first line of comments uses the word "Comment" as the key, the second line of comments uses "Comment1" as the key, and so on through "Comment9."</span></span> 
  
<span data-ttu-id="68d51-140">Записи **LargeIcon** и **SmallIcon** используются для указания пути к ресурсам значков, используемым для отображения значков в пользовательском интерфейсе клиентского приложения. Обычно это относится к строкам таблиц, которые содержат столбцы свойств **PR_ICON** ([PidTagIcon)](pidtagicon-canonical-property.md)или **PR_MINI_ICON** ([PidTagMiniIcon).](pidtagminiicon-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="68d51-140">The **LargeIcon** and **SmallIcon** entries are used to specify the path for the icon resources used to display icons in the client application's user interface, typically this is for table rows that include the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) or **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property columns.</span></span> <span data-ttu-id="68d51-141">Имена файлов значков могут быть указаны в виде путей относительно каталога, в котором установлен файл конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="68d51-141">Icon file names can be specified as pathnames relative to the directory where the form configuration file is installed.</span></span> <span data-ttu-id="68d51-142">Запись **"Версия"** используется для указать номер версии формы.</span><span class="sxs-lookup"><span data-stu-id="68d51-142">The **Version** entry is used to indicate the version number of the form.</span></span> <span data-ttu-id="68d51-143">**Языковой** код — это трехмерный идентификатор языка для конечной библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="68d51-143">**Locale** is the three-letter language identifier of the destination form library.</span></span> <span data-ttu-id="68d51-144">Список этих идентификаторов можно найти в справочнике _win32 Programmer.._</span><span class="sxs-lookup"><span data-stu-id="68d51-144">A list of these identifiers can be found in the  _Win32 Programmer's Reference_.</span></span>
  
<span data-ttu-id="68d51-145">**Скрытая** запись указывает, должна ли форма отображаться в пользовательском интерфейсе поставщика библиотеки форм: 1 указывает, что файл скрыт, а 0 — что форма видима.</span><span class="sxs-lookup"><span data-stu-id="68d51-145">The **Hidden** entry indicates whether the form should be displayed in a form library provider's user interface: 1 indicates that the file is hidden and 0 indicates that the form is visible.</span></span> <span data-ttu-id="68d51-146">Ниже показан пример файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="68d51-146">An example form configuration file is shown following.</span></span> 
  
<span data-ttu-id="68d51-147">Запись **ComposeInFolder** указывает, предназначена ли форма для того, чтобы поместить ее в текущую папку или в папку "Входящие" пользователя, когда пользователь сохраняет сообщение во время его составления: 1 указывает, что форма должна перейти в текущую папку, а 0 — в папку "Входящие".</span><span class="sxs-lookup"><span data-stu-id="68d51-147">The **ComposeInFolder** entry controls whether the form is designed to be placed in the current folder or in the user's Inbox when the user saves the message while composing it: 1 indicates that the form should go in the current folder and 0 indicates that it should go in the Inbox.</span></span> 
  
<span data-ttu-id="68d51-148">Запись **ComposeCommand** — это строка, помещаемая в меню составить клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="68d51-148">The **ComposeCommand** entry is the string to be placed in the client application's compose menu.</span></span> <span data-ttu-id="68d51-149">Если этот код не указан, будет использоваться запись **DisplayName.**</span><span class="sxs-lookup"><span data-stu-id="68d51-149">If this is not specified, the **DisplayName** entry will be used.</span></span> 
  
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


