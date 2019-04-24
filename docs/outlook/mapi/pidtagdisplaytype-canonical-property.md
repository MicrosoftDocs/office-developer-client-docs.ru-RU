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
# <a name="pidtagdisplaytype-canonical-property"></a><span data-ttu-id="82538-103">Каноническое свойство PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="82538-103">PidTagDisplayType Canonical Property</span></span>

  
  
<span data-ttu-id="82538-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82538-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82538-105">Содержит значение, используемое для связи значка с определенной строкой таблицы.</span><span class="sxs-lookup"><span data-stu-id="82538-105">Contains a value used to associate an icon with a particular row of a table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="82538-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="82538-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="82538-107">ПР_ДИСПЛАЙ_ТИПЕ</span><span class="sxs-lookup"><span data-stu-id="82538-107">PR_DISPLAY_TYPE</span></span>  <br/> |
|<span data-ttu-id="82538-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="82538-108">Identifier:</span></span>  <br/> |<span data-ttu-id="82538-109">0x3900</span><span class="sxs-lookup"><span data-stu-id="82538-109">0x3900</span></span>  <br/> |
|<span data-ttu-id="82538-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="82538-110">Data type:</span></span>  <br/> |<span data-ttu-id="82538-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="82538-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="82538-112">Область:</span><span class="sxs-lookup"><span data-stu-id="82538-112">Area:</span></span>  <br/> |<span data-ttu-id="82538-113">Адресная книга MAPI</span><span class="sxs-lookup"><span data-stu-id="82538-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82538-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="82538-114">Remarks</span></span>

<span data-ttu-id="82538-115">Это свойство содержит длинное целое число, которое упрощает специальную обработку записи в таблице на основе ее типа.</span><span class="sxs-lookup"><span data-stu-id="82538-115">This property contains a long integer that facilitates special treatment of the table entry based on its type.</span></span> <span data-ttu-id="82538-116">Эта специальная обработка обычно состоит из отображения значка или другого элемента отображения, связанного с типом отображения.</span><span class="sxs-lookup"><span data-stu-id="82538-116">This special treatment typically consists of displaying an icon, or other display element, associated with the display type.</span></span> 
  
<span data-ttu-id="82538-117">Это свойство не используется в таблицах содержимого папок.</span><span class="sxs-lookup"><span data-stu-id="82538-117">This property is not used in folder contents tables.</span></span> <span data-ttu-id="82538-118">Клиентские приложения должны использовать свойство **пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) сообщения и соответствующий интерфейс [имапиформинфо](imapiforminfoimapiprop.md) для получения **пр_икон** ([PidTagIcon](pidtagicon-canonical-property.md)) и **пр_мини_икон** ([ PidTagMiniIcon](pidtagminiicon-canonical-property.md)) свойства этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="82538-118">Client applications should use a message's **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property and appropriate [IMAPIFormInfo](imapiforminfoimapiprop.md) interface to get the **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) and **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) properties for that message.</span></span> 
  
<span data-ttu-id="82538-119">Это свойство может иметь только одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="82538-119">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="82538-120">ДТ_АЖЕНТ</span><span class="sxs-lookup"><span data-stu-id="82538-120">DT_AGENT</span></span> 
  
> <span data-ttu-id="82538-121">Автоматический агент, например, отображение квоты или диаграммы погоды.</span><span class="sxs-lookup"><span data-stu-id="82538-121">An automated agent, such as Quote-Of-The-Day or a weather chart display.</span></span>
    
<span data-ttu-id="82538-122">ДТ_ДИСТЛИСТ</span><span class="sxs-lookup"><span data-stu-id="82538-122">DT_DISTLIST</span></span> 
  
> <span data-ttu-id="82538-123">Список рассылки.</span><span class="sxs-lookup"><span data-stu-id="82538-123">A distribution list.</span></span>
    
<span data-ttu-id="82538-124">ДТ_ФОЛДЕР</span><span class="sxs-lookup"><span data-stu-id="82538-124">DT_FOLDER</span></span> 
  
> <span data-ttu-id="82538-125">Отображение значка папки по умолчанию рядом с папкой.</span><span class="sxs-lookup"><span data-stu-id="82538-125">Display default folder icon adjacent to folder.</span></span>
    
<span data-ttu-id="82538-126">ДТ_ФОЛДЕР_ЛИНК</span><span class="sxs-lookup"><span data-stu-id="82538-126">DT_FOLDER_LINK</span></span> 
  
> <span data-ttu-id="82538-127">Отображать значок ссылки на папку по умолчанию рядом с папкой, а не значком папки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="82538-127">Display default folder link icon adjacent to folder rather than the default folder icon.</span></span>
    
<span data-ttu-id="82538-128">ДТ_ФОЛДЕР_СПЕЦИАЛ</span><span class="sxs-lookup"><span data-stu-id="82538-128">DT_FOLDER_SPECIAL</span></span> 
  
> <span data-ttu-id="82538-129">Значок для папки с различием, характерным для приложения, например специальным типом общедоступной папки.</span><span class="sxs-lookup"><span data-stu-id="82538-129">Display icon for a folder with an application-specific distinction, such as a special type of public folder.</span></span>
    
<span data-ttu-id="82538-130">ДТ_ФОРУМ</span><span class="sxs-lookup"><span data-stu-id="82538-130">DT_FORUM</span></span> 
  
> <span data-ttu-id="82538-131">Форум, например служба доски объявлений или общедоступная или общая папка.</span><span class="sxs-lookup"><span data-stu-id="82538-131">A forum, such as a bulletin board service or a public or shared folder.</span></span>
    
<span data-ttu-id="82538-132">ДТ_ГЛОБАЛ</span><span class="sxs-lookup"><span data-stu-id="82538-132">DT_GLOBAL</span></span> 
  
> <span data-ttu-id="82538-133">Глобальная адресная книга.</span><span class="sxs-lookup"><span data-stu-id="82538-133">A global address book.</span></span>
    
<span data-ttu-id="82538-134">ДТ_ЛОКАЛ</span><span class="sxs-lookup"><span data-stu-id="82538-134">DT_LOCAL</span></span> 
  
> <span data-ttu-id="82538-135">Локальная адресная книга, к которой вы предоставляете доступ из небольшой рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="82538-135">A local address book that you share with a small workgroup.</span></span>
    
<span data-ttu-id="82538-136">ДТ_МАИЛУСЕР</span><span class="sxs-lookup"><span data-stu-id="82538-136">DT_MAILUSER</span></span> 
  
> <span data-ttu-id="82538-137">Типичный пользователь обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="82538-137">A typical messaging user.</span></span>
    
<span data-ttu-id="82538-138">ДТ_МОДИФИАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="82538-138">DT_MODIFIABLE</span></span> 
  
> <span data-ttu-id="82538-139">Допуска контейнер должен быть отмечен как изменяемый в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="82538-139">Modifiable; the container should be denoted as modifiable in the user interface.</span></span>
    
<span data-ttu-id="82538-140">ДТ_НОТ_СПЕЦИФИК</span><span class="sxs-lookup"><span data-stu-id="82538-140">DT_NOT_SPECIFIC</span></span> 
  
> <span data-ttu-id="82538-141">Не совпадают с другими параметрами.</span><span class="sxs-lookup"><span data-stu-id="82538-141">Does not match any of the other settings.</span></span>
    
<span data-ttu-id="82538-142">ДТ_ОРГАНИЗАТИОН</span><span class="sxs-lookup"><span data-stu-id="82538-142">DT_ORGANIZATION</span></span> 
  
> <span data-ttu-id="82538-143">Специальный псевдоним, определенный для большой группы, например служба технической поддержки, учетная запись или координатор крови.</span><span class="sxs-lookup"><span data-stu-id="82538-143">A special alias defined for a large group, such as helpdesk, accounting, or blood-drive coordinator.</span></span>
    
<span data-ttu-id="82538-144">ДТ_ПРИВАТЕ_ДИСТЛИСТ</span><span class="sxs-lookup"><span data-stu-id="82538-144">DT_PRIVATE_DISTLIST</span></span> 
  
> <span data-ttu-id="82538-145">Частный административный список рассылки.</span><span class="sxs-lookup"><span data-stu-id="82538-145">A private, personally administered distribution list.</span></span>
    
<span data-ttu-id="82538-146">ДТ_РЕМОТЕ_МАИЛУСЕР</span><span class="sxs-lookup"><span data-stu-id="82538-146">DT_REMOTE_MAILUSER</span></span> 
  
> <span data-ttu-id="82538-147">Получатель, который известен из внешней или удаленной системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="82538-147">A recipient known to be from a foreign or remote messaging system.</span></span>
    
<span data-ttu-id="82538-148">ДТ_ВАН</span><span class="sxs-lookup"><span data-stu-id="82538-148">DT_WAN</span></span> 
  
> <span data-ttu-id="82538-149">Адресная книга глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="82538-149">A wide area network address book.</span></span>
    
<span data-ttu-id="82538-150">В таблицах содержимого адресных книг используются значения ДТ_АЖЕНТ, ДТ_ДИСТЛИСТ, ДТ_ФОРУМ, ДТ_МАИЛУСЕР, ДТ_ОРГАНИЗАТИОН, ДТ_ПРИВАТЕ_ДИСТЛИСТ и ДТ_РЕМОТЕ_МАИЛУСЕР.</span><span class="sxs-lookup"><span data-stu-id="82538-150">Address book contents tables use the DT_AGENT, DT_DISTLIST, DT_FORUM, DT_MAILUSER, DT_ORGANIZATION, DT_PRIVATE_DISTLIST, and DT_REMOTE_MAILUSER values.</span></span> <span data-ttu-id="82538-151">В таблицах иерархии адресных книг и в одноразовых таблицах используются значения ДТ_ГЛОБАЛ, ДТ_ЛОКАЛ, ДТ_МОДИФИАБЛЕ, ДТ_НОТ_СПЕЦИФИК и ДТ_ВАН.</span><span class="sxs-lookup"><span data-stu-id="82538-151">Address book hierarchy tables and one-off tables use the DT_GLOBAL, DT_LOCAL, DT_MODIFIABLE, DT_NOT_SPECIFIC, and DT_WAN values.</span></span> <span data-ttu-id="82538-152">В таблицах иерархии папок используются значения ДТ_ФОЛДЕР, ДТ_ФОЛДЕР_ЛИНК и ДТ_ФОЛДЕР_СПЕЦИАЛ.</span><span class="sxs-lookup"><span data-stu-id="82538-152">Folder hierarchy tables use the DT_FOLDER, DT_FOLDER_LINK, and DT_FOLDER_SPECIAL values.</span></span> 
  
<span data-ttu-id="82538-153">Если это свойство не задано, клиент должен предполагать тип по умолчанию, который подходит для таблицы, обычно ДТ_ФОЛДЕР, ДТ_ЛОКАЛ или ДТ_МАИЛУСЕР.</span><span class="sxs-lookup"><span data-stu-id="82538-153">If this property is not set, the client should assume the default type appropriate for the table, typically DT_FOLDER, DT_LOCAL, or DT_MAILUSER.</span></span> 
  
 <span data-ttu-id="82538-154">**Note (Примечание** ) Все значения, которые не задокументированы, зарезервированы для MAPI.</span><span class="sxs-lookup"><span data-stu-id="82538-154">**Note** All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="82538-155">Клиентские приложения не должны определять новые значения и должны быть готовы к работе с недокументированным значением.</span><span class="sxs-lookup"><span data-stu-id="82538-155">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="82538-156">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="82538-156">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="82538-157">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="82538-157">Protocol specifications</span></span>

<span data-ttu-id="82538-158">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82538-158">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82538-159">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="82538-159">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="82538-160">[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82538-160">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82538-161">Обрабатывает объекты сообщений и вложений.</span><span class="sxs-lookup"><span data-stu-id="82538-161">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="82538-162">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82538-162">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82538-163">Задает свойства и операции, допустимые для шаблонов адресных книг.</span><span class="sxs-lookup"><span data-stu-id="82538-163">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
<span data-ttu-id="82538-164">[[MS — ОКСЛДАП]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="82538-164">[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="82538-165">Включает доступ к каталогу.</span><span class="sxs-lookup"><span data-stu-id="82538-165">Enables directory access.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="82538-166">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="82538-166">Header files</span></span>

<span data-ttu-id="82538-167">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="82538-167">Mapidefs.h</span></span>
  
> <span data-ttu-id="82538-168">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="82538-168">Provides data type definitions.</span></span>
    
<span data-ttu-id="82538-169">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="82538-169">Mapitags.h</span></span>
  
> <span data-ttu-id="82538-170">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="82538-170">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="82538-171">См. также</span><span class="sxs-lookup"><span data-stu-id="82538-171">See also</span></span>



[<span data-ttu-id="82538-172">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="82538-172">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="82538-173">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="82538-173">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="82538-174">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="82538-174">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="82538-175">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="82538-175">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

