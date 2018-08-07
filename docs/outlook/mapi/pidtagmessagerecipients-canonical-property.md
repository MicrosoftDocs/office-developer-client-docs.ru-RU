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
ms.openlocfilehash: 980b1b81a0afbfe05fee915ddd730aad31811132
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811369"
---
# <a name="pidtagmessagerecipients-canonical-property"></a><span data-ttu-id="f6a57-103">Каноническое свойство PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="f6a57-103">PidTagMessageRecipients Canonical Property</span></span>

  
  
<span data-ttu-id="f6a57-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f6a57-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f6a57-105">Содержит таблицу ограничения, которые могут быть применены к таблице содержимого для поиска всех сообщений, которые содержат получателей вложенных объектов, необходимых для ограничения.</span><span class="sxs-lookup"><span data-stu-id="f6a57-105">Contains a table of restrictions that can be applied to a contents table to find all messages that contain recipient subobjects that meet the restrictions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6a57-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f6a57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f6a57-107">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="f6a57-107">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |
|<span data-ttu-id="f6a57-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f6a57-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f6a57-109">0x0E12</span><span class="sxs-lookup"><span data-stu-id="f6a57-109">0x0E12</span></span>  <br/> |
|<span data-ttu-id="f6a57-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f6a57-110">Data type:</span></span>  <br/> |<span data-ttu-id="f6a57-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="f6a57-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="f6a57-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f6a57-112">Area:</span></span>  <br/> |<span data-ttu-id="f6a57-113">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="f6a57-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f6a57-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f6a57-114">Remarks</span></span>

<span data-ttu-id="f6a57-115">Это свойство можно в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) для включения или исключения в [IMAPIProp::CopyProps](imapiprop-copyprops.md) операции.</span><span class="sxs-lookup"><span data-stu-id="f6a57-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="f6a57-116">Как свойство типа **PT_OBJECT**его нельзя отменить успешно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="f6a57-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="f6a57-117">Его содержимое должен осуществляться с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , запрашивающего идентификатор интерфейса **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="f6a57-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="f6a57-118">Поставщиков услуг должен сообщить о его в метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) если оно установлено, но может сообщать о его или не в том случае, если не указано.</span><span class="sxs-lookup"><span data-stu-id="f6a57-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="f6a57-119">Чтобы извлечь содержимое таблицы, клиентское приложение следует вызовите метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) .</span><span class="sxs-lookup"><span data-stu-id="f6a57-119">To retrieve table contents, a client application should call the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method.</span></span> 
  
<span data-ttu-id="f6a57-120">Это свойство можно использовать для ограничения вложенные объекты, указав в структуре [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="f6a57-120">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="f6a57-121">Это позволяет клиента для ограничения представления контейнера для сообщений с получателями собрания заданному критерию.</span><span class="sxs-lookup"><span data-stu-id="f6a57-121">This enables a client to limit the view of a container to messages with recipients meeting given criteria.</span></span> <span data-ttu-id="f6a57-122">Сообщение имеет право на просмотр, если хотя бы одна строка в таблице получателей, то есть, один получатель удовлетворяет ограничениям вложенные объекты.</span><span class="sxs-lookup"><span data-stu-id="f6a57-122">A message qualifies for viewing if at least one row in its recipient table, that is, one recipient satisfies the subobject restriction.</span></span> 
  
 <span data-ttu-id="f6a57-123">**Примечание** Использование результатов ограничение вложенные объекты — это эквивалент [IMAPISession::OpenEntry](imapisession-openentry.md) вызвать для каждого сообщения в таблице.</span><span class="sxs-lookup"><span data-stu-id="f6a57-123">**Note** Using subobject restriction results is the equivalent of an [IMAPISession::OpenEntry](imapisession-openentry.md) call on every message in the table.</span></span> <span data-ttu-id="f6a57-124">В зависимости от того, в клиентском приложении и количество сообщений для поиска он может повлиять на производительность.</span><span class="sxs-lookup"><span data-stu-id="f6a57-124">Depending on the client application and the number of messages to be searched, it can affect performance.</span></span> 
  
<span data-ttu-id="f6a57-125">Свойство **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) и это свойство похожи в использовании.</span><span class="sxs-lookup"><span data-stu-id="f6a57-125">The **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) property and this property are similar in usage.</span></span> <span data-ttu-id="f6a57-126">Несколько свойств MAPI предоставляют доступ к таблицы:</span><span class="sxs-lookup"><span data-stu-id="f6a57-126">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="f6a57-127">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="f6a57-127">**Property**</span></span>|<span data-ttu-id="f6a57-128">**Table**</span><span class="sxs-lookup"><span data-stu-id="f6a57-128">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f6a57-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6a57-129">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6a57-130">Содержимое таблицы</span><span class="sxs-lookup"><span data-stu-id="f6a57-130">Contents table</span></span>  <br/> |
|<span data-ttu-id="f6a57-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6a57-131">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6a57-132">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="f6a57-132">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="f6a57-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6a57-133">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6a57-134">Связанное содержимое таблицы</span><span class="sxs-lookup"><span data-stu-id="f6a57-134">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="f6a57-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="f6a57-135">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f6a57-136">В таблице вложений</span><span class="sxs-lookup"><span data-stu-id="f6a57-136">Attachment table</span></span>  <br/> |
|<span data-ttu-id="f6a57-137">PR_MESSAGE_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="f6a57-137">PR_MESSAGE_RECIPIENTS</span></span>  <br/> |<span data-ttu-id="f6a57-138">В таблице получателей</span><span class="sxs-lookup"><span data-stu-id="f6a57-138">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f6a57-139">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f6a57-139">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f6a57-140">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f6a57-140">Protocol specifications</span></span>

<span data-ttu-id="f6a57-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6a57-141">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6a57-142">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f6a57-142">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f6a57-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6a57-143">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6a57-144">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="f6a57-144">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="f6a57-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6a57-145">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6a57-146">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="f6a57-146">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="f6a57-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6a57-147">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6a57-148">Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f6a57-148">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
<span data-ttu-id="f6a57-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f6a57-149">[[MS-OXTNEF]](http://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f6a57-150">Кодирует и декодирует объекты сообщения и вложения в представление эффективным потока.</span><span class="sxs-lookup"><span data-stu-id="f6a57-150">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f6a57-151">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="f6a57-151">Header files</span></span>

<span data-ttu-id="f6a57-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f6a57-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="f6a57-153">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f6a57-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="f6a57-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f6a57-154">Mapitags.h</span></span>
  
> <span data-ttu-id="f6a57-155">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f6a57-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f6a57-156">См. также</span><span class="sxs-lookup"><span data-stu-id="f6a57-156">See also</span></span>



[<span data-ttu-id="f6a57-157">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f6a57-157">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f6a57-158">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f6a57-158">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f6a57-159">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f6a57-159">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f6a57-160">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="f6a57-160">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

