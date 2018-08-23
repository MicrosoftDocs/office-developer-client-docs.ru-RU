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
ms.openlocfilehash: 6d0d2c07355140e89ffb24095d1ca3a302f6e5ce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568450"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="6d655-103">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="6d655-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="6d655-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d655-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d655-105">Содержит таблицу ограничения, которые могут быть применены к таблице содержимого для поиска всех сообщений, которые содержат получателей вложенных объектов, необходимых для ограничения.</span><span class="sxs-lookup"><span data-stu-id="6d655-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6d655-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6d655-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d655-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="6d655-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="6d655-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6d655-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d655-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="6d655-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="6d655-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6d655-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d655-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="6d655-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="6d655-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6d655-112">Area:</span></span>  <br/> |<span data-ttu-id="6d655-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="6d655-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d655-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6d655-114">Remarks</span></span>

<span data-ttu-id="6d655-115">Это свойство можно в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) для включения или исключения в [IMAPIProp::CopyProps](imapiprop-copyprops.md) операции.</span><span class="sxs-lookup"><span data-stu-id="6d655-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="6d655-116">Как свойство типа **PT_OBJECT**его нельзя отменить успешно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="6d655-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="6d655-117">Его содержимое должен осуществляться с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , запрашивающего идентификатор интерфейса **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="6d655-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="6d655-118">Поставщиков услуг должен сообщить о его в метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) если оно установлено, но может сообщать о его или не в том случае, если не указано.</span><span class="sxs-lookup"><span data-stu-id="6d655-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="6d655-119">Чтобы извлечь содержимое таблицы, клиентское приложение следует вызовите метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) .</span><span class="sxs-lookup"><span data-stu-id="6d655-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="6d655-120">Это свойство можно использовать для ограничения вложенные объекты, указав в структуре [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="6d655-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="6d655-121">Это позволяет клиента для ограничения представления контейнера для сообщений с получателями собрания заданному критерию.</span><span class="sxs-lookup"><span data-stu-id="6d655-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="6d655-122">Сообщение имеет право на просмотр, если хотя бы одна строка в таблице получателей, то есть, один получатель удовлетворяет ограничениям вложенные объекты.</span><span class="sxs-lookup"><span data-stu-id="6d655-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="6d655-123">**Примечание** Использование результатов ограничение вложенные объекты — это эквивалент [IMAPISession::OpenEntry](imapisession-openentry.md) вызвать для каждого сообщения в таблице.</span><span class="sxs-lookup"><span data-stu-id="6d655-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="6d655-124">В зависимости от того, в клиентском приложении и количество сообщений для поиска он может повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="6d655-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="6d655-125">Свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) и это свойство похожи в использовании.</span><span class="sxs-lookup"><span data-stu-id="6d655-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="6d655-126">Несколько свойств MAPI предоставляют доступ к таблицы:</span><span class="sxs-lookup"><span data-stu-id="6d655-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="6d655-127">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="6d655-127">**Property**</span></span>|<span data-ttu-id="6d655-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="6d655-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d655-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d655-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d655-130">Содержимое таблицы</span><span class="sxs-lookup"><span data-stu-id="6d655-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="6d655-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d655-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d655-132">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="6d655-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="6d655-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d655-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d655-134">Связанное содержимое таблицы</span><span class="sxs-lookup"><span data-stu-id="6d655-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="6d655-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6d655-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="6d655-136">В таблице вложений</span><span class="sxs-lookup"><span data-stu-id="6d655-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="6d655-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="6d655-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="6d655-138">В таблице получателей</span><span class="sxs-lookup"><span data-stu-id="6d655-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6d655-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6d655-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6d655-140">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="6d655-140">Protocol specifications</span></span>

<span data-ttu-id="6d655-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d655-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d655-142">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6d655-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6d655-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d655-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d655-144">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="6d655-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="6d655-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d655-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d655-146">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="6d655-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="6d655-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d655-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d655-148">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="6d655-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="6d655-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6d655-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6d655-150">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="6d655-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6d655-151">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="6d655-151">Header files</span></span>

<span data-ttu-id="6d655-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d655-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d655-153">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6d655-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d655-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d655-154">Mapitags.h</span></span>
  
> <span data-ttu-id="6d655-155">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6d655-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d655-156">См. также</span><span class="sxs-lookup"><span data-stu-id="6d655-156">See also</span></span>



[<span data-ttu-id="6d655-157">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d655-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d655-158">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d655-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d655-159">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6d655-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d655-160">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6d655-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

