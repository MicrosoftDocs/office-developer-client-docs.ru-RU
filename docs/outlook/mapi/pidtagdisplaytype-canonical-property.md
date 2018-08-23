---
title: Каноническое свойство PidTagDisplayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5b067b3bc38df978cd0f4c52beb37579619edc24
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583514"
---
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="bef78-103">Каноническое свойство PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="bef78-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="bef78-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bef78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bef78-105">Содержит значение, используемое для сопоставления значка с конкретной строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="bef78-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bef78-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="bef78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bef78-107">PR_DISPLAY_TYPE</span><span class="sxs-lookup"><span data-stu-id="bef78-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="bef78-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bef78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bef78-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="bef78-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="bef78-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="bef78-110">Data type:</span></span>  <br/> |<span data-ttu-id="bef78-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="bef78-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="bef78-112">Область:</span><span class="sxs-lookup"><span data-stu-id="bef78-112">Area:</span></span>  <br/> |<span data-ttu-id="bef78-113">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="bef78-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bef78-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="bef78-114">Remarks</span></span>

<span data-ttu-id="bef78-115">Это свойство содержит длинное целое, которая упрощает специальная обработка записи таблицы, на основе этого типа.</span><span class="sxs-lookup"><span data-stu-id="bef78-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="bef78-116">Эта специальная обработка обычно состоит из отображения значка или других отображения элемента, связанного с типа отображения.</span><span class="sxs-lookup"><span data-stu-id="bef78-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="bef78-117">Это свойство не используется в таблицах содержимое папки.</span><span class="sxs-lookup"><span data-stu-id="bef78-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="bef78-118">Для получения **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) и **PR_MINI_ICON** ([ клиентских приложений следует использовать свойство **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) и соответствующий интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) сообщения PidTagMiniIcon](pidtagminiicon-canonical-property.md)) свойства для этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="bef78-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="bef78-119">Это свойство может иметь только один из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="bef78-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="bef78-120">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="bef78-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="bef78-121">Автоматическая отправка агента, такие как квоты день или отображение диаграмм прогноза погоды.</span><span class="sxs-lookup"><span data-stu-id="bef78-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="bef78-122">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="bef78-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="bef78-123">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="bef78-123">A distribution list.</span></span>
    
<span data-ttu-id="bef78-124">DT_FOLDER</span><span class="sxs-lookup"><span data-stu-id="bef78-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="bef78-125">Отображение значка папки по умолчанию рядом с папки.</span><span class="sxs-lookup"><span data-stu-id="bef78-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="bef78-126">DT_FOLDER_LINK</span><span class="sxs-lookup"><span data-stu-id="bef78-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="bef78-127">Отображение по умолчанию папки ссылок значок рядом с папки, а не значок папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bef78-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="bef78-128">DT_FOLDER_SPECIAL</span><span class="sxs-lookup"><span data-stu-id="bef78-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="bef78-129">Отображение значка для папки с различие конкретного приложения, такие как особый тип общей папки.</span><span class="sxs-lookup"><span data-stu-id="bef78-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="bef78-130">DT_FORUM</span><span class="sxs-lookup"><span data-stu-id="bef78-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="bef78-131">Форум, таких как служба досках или общедоступный или общей папки.</span><span class="sxs-lookup"><span data-stu-id="bef78-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="bef78-132">DT_GLOBAL</span><span class="sxs-lookup"><span data-stu-id="bef78-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="bef78-133">Глобальной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bef78-133">A global address book.</span></span>
    
<span data-ttu-id="bef78-134">DT_LOCAL</span><span class="sxs-lookup"><span data-stu-id="bef78-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="bef78-135">Локальной адресной книги, совместно с небольшой рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="bef78-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="bef78-136">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="bef78-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="bef78-137">Обычной пользовательской обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="bef78-137">A typical messaging user.</span></span>
    
<span data-ttu-id="bef78-138">DT_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="bef78-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="bef78-139">Можно изменить; контейнер должен идентификаторами как можно изменить в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="bef78-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="bef78-140">DT_NOT_SPECIFIC</span><span class="sxs-lookup"><span data-stu-id="bef78-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="bef78-141">Не соответствует другие параметры.</span><span class="sxs-lookup"><span data-stu-id="bef78-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="bef78-142">DT_ORGANIZATION</span><span class="sxs-lookup"><span data-stu-id="bef78-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="bef78-143">Специальные псевдоним, определенных для больших групп, такие как служба технической поддержки, учета или координатора кровь диска.</span><span class="sxs-lookup"><span data-stu-id="bef78-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="bef78-144">DT_PRIVATE_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="bef78-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="bef78-145">Частный, раскрывающие личность администрировать с помощью списка рассылки.</span><span class="sxs-lookup"><span data-stu-id="bef78-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="bef78-146">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="bef78-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="bef78-147">Получатель, известно, из внешнего или удаленных систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="bef78-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="bef78-148">DT_WAN</span><span class="sxs-lookup"><span data-stu-id="bef78-148">DT_WAN</span></span> 
  
> <span data-ttu-id="bef78-149">В глобальной сети адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="bef78-149">A wide area network address book.</span></span>
    
<span data-ttu-id="bef78-150">Содержимое таблиц адресной книги используются значения DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST и DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="bef78-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="bef78-151">Используйте значения DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC и DT_WAN в одноразовых таблиц и таблиц иерархии адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bef78-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="bef78-152">Таблиц иерархии папок используйте значения DT_FOLDER, DT_FOLDER_LINK и DT_FOLDER_SPECIAL.</span><span class="sxs-lookup"><span data-stu-id="bef78-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="bef78-153">Если это свойство не задано, клиент должен использовать тип по умолчанию для таблицы, обычно DT_FOLDER, DT_LOCAL или DT_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="bef78-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="bef78-154">**Примечание** Все значения не задокументирован зарезервированы для MAPI.</span><span class="sxs-lookup"><span data-stu-id="bef78-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="bef78-155">Клиентские приложения не должны определить все новые значения и должны быть готовы для смягчения последствий недокументированного значения.</span><span class="sxs-lookup"><span data-stu-id="bef78-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="bef78-156">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="bef78-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bef78-157">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="bef78-157">Protocol specifications</span></span>

<span data-ttu-id="bef78-158">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bef78-158">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bef78-159">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bef78-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bef78-160">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bef78-160">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bef78-161">Обрабатывает объекты сообщения и вложения.</span><span class="sxs-lookup"><span data-stu-id="bef78-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="bef78-162">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bef78-162">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bef78-163">Задает свойства и операции, допустимые для шаблонов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="bef78-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="bef78-164">[[MS-OXLDAP]](http://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bef78-164">[[MS-OXLDAP]](http://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bef78-165">Обеспечивает доступ к каталогу.</span><span class="sxs-lookup"><span data-stu-id="bef78-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bef78-166">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="bef78-166">Header files</span></span>

<span data-ttu-id="bef78-167">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bef78-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="bef78-168">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="bef78-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="bef78-169">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bef78-169">Mapitags.h</span></span>
  
> <span data-ttu-id="bef78-170">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="bef78-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bef78-171">См. также</span><span class="sxs-lookup"><span data-stu-id="bef78-171">See also</span></span>



[<span data-ttu-id="bef78-172">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bef78-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bef78-173">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="bef78-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bef78-174">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="bef78-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bef78-175">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="bef78-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

