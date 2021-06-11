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
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="1d34c-103">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="1d34c-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="1d34c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d34c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d34c-105">Содержит таблицу ограничений, которые можно применить к таблице содержимого, чтобы найти все сообщения, содержащие подобекцы получателей, которые соответствуют ограничениям.</span><span class="sxs-lookup"><span data-stu-id="1d34c-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d34c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1d34c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d34c-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="1d34c-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="1d34c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1d34c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1d34c-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="1d34c-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="1d34c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1d34c-110">Data type:</span></span>  <br/> |<span data-ttu-id="1d34c-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="1d34c-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="1d34c-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1d34c-112">Area:</span></span>  <br/> |<span data-ttu-id="1d34c-113">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="1d34c-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d34c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="1d34c-114">Remarks</span></span>

<span data-ttu-id="1d34c-115">Это свойство можно исключить в [операциях IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в [операции IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="1d34c-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="1d34c-116">Как свойство типа **PT_OBJECT,** его невозможно успешно получить [методом IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="1d34c-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="1d34c-117">Его содержимое должно быть доступны [методом IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивая **идентификатор IID_IMAPITable** интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1d34c-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="1d34c-118">Поставщики услуг должны сообщить об этом [методу IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он за установлен, но может сообщить об этом или нет, если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="1d34c-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="1d34c-119">Чтобы получить содержимое таблицы, клиентская заявка должна вызвать [метод IMessage::GetRecipientTable.](imessage-getrecipienttable.md)</span><span class="sxs-lookup"><span data-stu-id="1d34c-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="1d34c-120">Это свойство можно использовать для ограничения субобекции, указав его в [структуре SSubRestriction.](ssubrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="1d34c-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="1d34c-121">Это позволяет клиенту ограничить представление контейнера сообщениями с данными критериями для получателей.</span><span class="sxs-lookup"><span data-stu-id="1d34c-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="1d34c-122">Сообщение имеет право на просмотр, если хотя бы одна строка в таблице получателей, то есть один получатель удовлетворяет ограничению subobject.</span><span class="sxs-lookup"><span data-stu-id="1d34c-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="1d34c-123">**Примечание** Использование результатов ограничения subobject эквивалентно вызову [IMAPISession::OpenEntry](imapisession-openentry.md) для каждого сообщения в таблице.</span><span class="sxs-lookup"><span data-stu-id="1d34c-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="1d34c-124">В зависимости от клиентского приложения и количества сообщений, которые будут искаться, это может повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="1d34c-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="1d34c-125">Свойство **PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)и это свойство аналогично по использованию.</span><span class="sxs-lookup"><span data-stu-id="1d34c-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="1d34c-126">Несколько свойств MAPI предоставляют доступ к таблицам:</span><span class="sxs-lookup"><span data-stu-id="1d34c-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="1d34c-127">**Property**</span><span class="sxs-lookup"><span data-stu-id="1d34c-127">**Property**</span></span>|<span data-ttu-id="1d34c-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="1d34c-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d34c-129">**PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1d34c-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d34c-130">Таблица контента</span><span class="sxs-lookup"><span data-stu-id="1d34c-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="1d34c-131">**PR_CONTAINER_HIERARCHY** [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1d34c-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d34c-132">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="1d34c-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="1d34c-133">**PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1d34c-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d34c-134">Связанная таблица контента</span><span class="sxs-lookup"><span data-stu-id="1d34c-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="1d34c-135">**PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="1d34c-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1d34c-136">Таблица вложений</span><span class="sxs-lookup"><span data-stu-id="1d34c-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="1d34c-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="1d34c-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="1d34c-138">Таблица получателей</span><span class="sxs-lookup"><span data-stu-id="1d34c-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1d34c-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1d34c-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1d34c-140">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1d34c-140">Protocol specifications</span></span>

<span data-ttu-id="1d34c-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d34c-141">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d34c-142">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="1d34c-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1d34c-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d34c-143">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d34c-144">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1d34c-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="1d34c-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d34c-145">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d34c-146">Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.</span><span class="sxs-lookup"><span data-stu-id="1d34c-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="1d34c-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d34c-147">[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d34c-148">Включает обработку списков разрешить или блокировать и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="1d34c-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="1d34c-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d34c-149">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d34c-150">Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.</span><span class="sxs-lookup"><span data-stu-id="1d34c-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1d34c-151">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="1d34c-151">Header files</span></span>

<span data-ttu-id="1d34c-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d34c-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d34c-153">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1d34c-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="1d34c-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1d34c-154">Mapitags.h</span></span>
  
> <span data-ttu-id="1d34c-155">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1d34c-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d34c-156">См. также</span><span class="sxs-lookup"><span data-stu-id="1d34c-156">See also</span></span>



[<span data-ttu-id="1d34c-157">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1d34c-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d34c-158">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1d34c-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d34c-159">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1d34c-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d34c-160">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="1d34c-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

