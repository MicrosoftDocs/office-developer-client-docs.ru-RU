---
title: Каноническое свойство PidTagMessageRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355687"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="af140-103">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="af140-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="af140-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af140-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af140-105">Содержит таблицу ограничений, которые можно применить к таблице содержимого, чтобы найти все сообщения, содержащие вложенные объекты получателей, соответствующие ограничениям.</span><span class="sxs-lookup"><span data-stu-id="af140-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="af140-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="af140-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="af140-107">ПР_МЕССАЖЕ_РЕЦИПИЕНТС</span><span class="sxs-lookup"><span data-stu-id="af140-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="af140-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="af140-108">Identifier:</span></span>  <br/> |<span data-ttu-id="af140-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="af140-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="af140-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="af140-110">Data type:</span></span>  <br/> |<span data-ttu-id="af140-111">ПТ_ОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="af140-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="af140-112">Область:</span><span class="sxs-lookup"><span data-stu-id="af140-112">Area:</span></span>  <br/> |<span data-ttu-id="af140-113">Общий обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="af140-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af140-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="af140-114">Remarks</span></span>

<span data-ttu-id="af140-115">Это свойство можно исключить в [IMAPIProp:: операции CopyTo](imapiprop-copyto.md) или включено в [IMAPIProp:: копипропс](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="af140-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="af140-116">Как свойство типа **пт_обжект**, оно не может быть успешно получено методом [IMAPIProp::](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="af140-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="af140-117">К его содержимому должен получать доступ метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , запрашивающий идентификатор интерфейса **иид_имапитабле** .</span><span class="sxs-lookup"><span data-stu-id="af140-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="af140-118">Поставщики услуг должны сообщить о ней методу [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , если он задан, но при необходимости можно сообщить ему, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="af140-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="af140-119">Чтобы получить содержимое таблицы, клиентское приложение должно вызвать метод [iMessage:: жетреЦипиенттабле](imessage-getrecipienttable.md) .</span><span class="sxs-lookup"><span data-stu-id="af140-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="af140-120">Это свойство можно использовать для ограничения подобъекта, указав его в структуре [ссубрестриктион](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="af140-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="af140-121">Это позволяет клиенту ограничить представление контейнера сообщениями, получателями которых удовлетворяют заданные условия.</span><span class="sxs-lookup"><span data-stu-id="af140-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="af140-122">Сообщение просматривается в том случае, если в таблице получателей по крайней мере одна строка, то есть один получатель удовлетворяет ограничению этого подобъекта.</span><span class="sxs-lookup"><span data-stu-id="af140-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="af140-123">**Note (Примечание** ) Использование результатов ограничения для подобъектов эквивалентно вызову [IMAPISession:: OpenEntry](imapisession-openentry.md) для каждого сообщения в таблице.</span><span class="sxs-lookup"><span data-stu-id="af140-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="af140-124">В зависимости от клиентского приложения и количества сообщений, в которых выполняется поиск, это может повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="af140-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="af140-125">Свойство **пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) и это свойство похожи в использовании.</span><span class="sxs-lookup"><span data-stu-id="af140-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="af140-126">Несколько свойств MAPI предоставляют доступ к таблицам:</span><span class="sxs-lookup"><span data-stu-id="af140-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="af140-127">**Property**</span><span class="sxs-lookup"><span data-stu-id="af140-127">**Property**</span></span>|<span data-ttu-id="af140-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="af140-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="af140-129">**Пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="af140-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="af140-130">Таблица содержимого</span><span class="sxs-lookup"><span data-stu-id="af140-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="af140-131">**Пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="af140-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="af140-132">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="af140-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="af140-133">**Пр_фолдер_ассоЦиатед_контентс** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="af140-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="af140-134">Связанная таблица содержимого</span><span class="sxs-lookup"><span data-stu-id="af140-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="af140-135">**Пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="af140-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="af140-136">Таблица вложений</span><span class="sxs-lookup"><span data-stu-id="af140-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="af140-137">ПР_МЕССАЖЕ_РЕЦИПИЕНТС</span><span class="sxs-lookup"><span data-stu-id="af140-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="af140-138">Таблица получателей</span><span class="sxs-lookup"><span data-stu-id="af140-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="af140-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="af140-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="af140-140">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="af140-140">Protocol specifications</span></span>

<span data-ttu-id="af140-141">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af140-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af140-142">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="af140-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="af140-143">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af140-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af140-144">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="af140-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="af140-145">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af140-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af140-146">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="af140-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="af140-147">[[MS — ОКСКСПАМ]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af140-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af140-148">Разрешает обработку списков разрешений и блокировок, а также определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="af140-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="af140-149">[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="af140-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="af140-150">Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.</span><span class="sxs-lookup"><span data-stu-id="af140-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="af140-151">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="af140-151">Header files</span></span>

<span data-ttu-id="af140-152">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="af140-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="af140-153">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="af140-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="af140-154">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="af140-154">Mapitags.h</span></span>
  
> <span data-ttu-id="af140-155">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="af140-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="af140-156">См. также</span><span class="sxs-lookup"><span data-stu-id="af140-156">See also</span></span>



[<span data-ttu-id="af140-157">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="af140-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="af140-158">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="af140-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="af140-159">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="af140-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="af140-160">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="af140-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

