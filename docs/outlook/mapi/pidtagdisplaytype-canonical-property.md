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
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360783"
---
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="1861f-103">Каноническое свойство PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="1861f-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="1861f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1861f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1861f-105">Содержит значение, используемого для связи значка с определенной строкой таблицы.</span><span class="sxs-lookup"><span data-stu-id="1861f-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1861f-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1861f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1861f-107">PR_DISPLAY_TYPE</span><span class="sxs-lookup"><span data-stu-id="1861f-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="1861f-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1861f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1861f-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="1861f-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="1861f-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1861f-110">Data type:</span></span>  <br/> |<span data-ttu-id="1861f-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1861f-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1861f-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1861f-112">Area:</span></span>  <br/> |<span data-ttu-id="1861f-113">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="1861f-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1861f-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1861f-114">Remarks</span></span>

<span data-ttu-id="1861f-115">Это свойство содержит длинный набор, который облегчает специальную обработку записи таблицы в зависимости от ее типа.</span><span class="sxs-lookup"><span data-stu-id="1861f-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="1861f-116">Это специальное лечение обычно состоит из отображения значка или другого элемента отображения, связанного с типом отображения.</span><span class="sxs-lookup"><span data-stu-id="1861f-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="1861f-117">Это свойство не используется в таблицах содержимого папок.</span><span class="sxs-lookup"><span data-stu-id="1861f-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="1861f-118">Клиентские приложения должны использовать свойство **PR_MESSAGE_CLASS** [(PidTagMessageClass)](pidtagmessageclass-canonical-property.md)и соответствующий интерфейс [IMAPIFormInfo](imapiforminfoimapiprop.md) для получения свойств **PR_ICON** [(PidTagIcon)](pidtagicon-canonical-property.md)и **PR_MINI_ICON** [(PidTagMiniIcon).](pidtagminiicon-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1861f-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="1861f-119">Это свойство может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="1861f-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="1861f-120">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="1861f-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="1861f-121">Автоматический агент, например Quote-Of-The-Day или отображение диаграммы погоды.</span><span class="sxs-lookup"><span data-stu-id="1861f-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="1861f-122">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="1861f-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="1861f-123">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="1861f-123">A distribution list.</span></span>
    
<span data-ttu-id="1861f-124">DT_FOLDER</span><span class="sxs-lookup"><span data-stu-id="1861f-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="1861f-125">Отображение значка папки по умолчанию рядом с папкой.</span><span class="sxs-lookup"><span data-stu-id="1861f-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="1861f-126">DT_FOLDER_LINK</span><span class="sxs-lookup"><span data-stu-id="1861f-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="1861f-127">Отображение значка ссылки папки по умолчанию рядом с папкой, а не значком папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1861f-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="1861f-128">DT_FOLDER_SPECIAL</span><span class="sxs-lookup"><span data-stu-id="1861f-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="1861f-129">Отображение значка для папки с различиями, определенными приложениями, такими как специальный тип общедоступных папок.</span><span class="sxs-lookup"><span data-stu-id="1861f-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="1861f-130">DT_FORUM</span><span class="sxs-lookup"><span data-stu-id="1861f-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="1861f-131">Форум, например служба доски объявлений, публичная или общая папка.</span><span class="sxs-lookup"><span data-stu-id="1861f-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="1861f-132">DT_GLOBAL</span><span class="sxs-lookup"><span data-stu-id="1861f-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="1861f-133">Глобальная адресная книга.</span><span class="sxs-lookup"><span data-stu-id="1861f-133">A global address book.</span></span>
    
<span data-ttu-id="1861f-134">DT_LOCAL</span><span class="sxs-lookup"><span data-stu-id="1861f-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="1861f-135">Локализованная адресная книга, которую вы делитесь с небольшой группы.</span><span class="sxs-lookup"><span data-stu-id="1861f-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="1861f-136">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="1861f-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="1861f-137">Типичный пользователь обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1861f-137">A typical messaging user.</span></span>
    
<span data-ttu-id="1861f-138">DT_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="1861f-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="1861f-139">Модификабель; контейнер должен быть обозначаться как модификабельный в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="1861f-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="1861f-140">DT_NOT_SPECIFIC</span><span class="sxs-lookup"><span data-stu-id="1861f-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="1861f-141">Не соответствует другим настройкам.</span><span class="sxs-lookup"><span data-stu-id="1861f-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="1861f-142">DT_ORGANIZATION</span><span class="sxs-lookup"><span data-stu-id="1861f-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="1861f-143">Специальный псевдоним, определенный для большой группы, например helpdesk, accounting или blood-drive coordinator.</span><span class="sxs-lookup"><span data-stu-id="1861f-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="1861f-144">DT_PRIVATE_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="1861f-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="1861f-145">Частный, лично управляемый список рассылки.</span><span class="sxs-lookup"><span data-stu-id="1861f-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="1861f-146">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="1861f-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="1861f-147">Получатель, как известно, из иностранной или удаленной системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="1861f-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="1861f-148">DT_WAN</span><span class="sxs-lookup"><span data-stu-id="1861f-148">DT_WAN</span></span> 
  
> <span data-ttu-id="1861f-149">Широкая адресная книга сетевой сети.</span><span class="sxs-lookup"><span data-stu-id="1861f-149">A wide area network address book.</span></span>
    
<span data-ttu-id="1861f-150">В таблицах контента адресной книги используются значения DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST и DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="1861f-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="1861f-151">Таблицы иерархии адресных книг и разовые таблицы используют значения DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC и DT_WAN.</span><span class="sxs-lookup"><span data-stu-id="1861f-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="1861f-152">Таблицы иерархии папок используют значения DT_FOLDER, DT_FOLDER_LINK и DT_FOLDER_SPECIAL.</span><span class="sxs-lookup"><span data-stu-id="1861f-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="1861f-153">Если это свойство не установлено, клиент должен считать тип по умолчанию подходящим для таблицы, как правило, DT_FOLDER, DT_LOCAL или DT_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="1861f-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="1861f-154">**Примечание** Все значения, не задокументированные, зарезервированы для MAPI.</span><span class="sxs-lookup"><span data-stu-id="1861f-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="1861f-155">Клиентские приложения не должны определять новые значения и должны быть готовы к обращению с недокументным значением.</span><span class="sxs-lookup"><span data-stu-id="1861f-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1861f-156">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1861f-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1861f-157">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1861f-157">Protocol specifications</span></span>

<span data-ttu-id="1861f-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1861f-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1861f-159">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="1861f-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1861f-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1861f-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1861f-161">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="1861f-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="1861f-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1861f-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1861f-163">Указывает свойства и операции, допустимые для шаблонов адресной книги.</span><span class="sxs-lookup"><span data-stu-id="1861f-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="1861f-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1861f-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1861f-165">Включает доступ к каталогам.</span><span class="sxs-lookup"><span data-stu-id="1861f-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1861f-166">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="1861f-166">Header files</span></span>

<span data-ttu-id="1861f-167">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1861f-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="1861f-168">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1861f-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="1861f-169">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1861f-169">Mapitags.h</span></span>
  
> <span data-ttu-id="1861f-170">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1861f-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1861f-171">См. также</span><span class="sxs-lookup"><span data-stu-id="1861f-171">See also</span></span>



[<span data-ttu-id="1861f-172">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1861f-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1861f-173">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1861f-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1861f-174">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1861f-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1861f-175">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="1861f-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

