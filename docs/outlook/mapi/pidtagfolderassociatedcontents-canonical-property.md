---
title: Каноническое свойство PidTagFolderAssociatedContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ae09488b99cd55e5cfca23f504d81ac5919633d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574155"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="1f946-103">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="1f946-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="1f946-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f946-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f946-105">Содержит объект внедренного содержимого таблицы, предоставляющий информацию о таблице связанного содержимого.</span><span class="sxs-lookup"><span data-stu-id="1f946-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f946-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="1f946-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f946-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="1f946-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="1f946-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="1f946-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f946-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="1f946-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="1f946-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="1f946-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f946-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="1f946-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="1f946-112">Область:</span><span class="sxs-lookup"><span data-stu-id="1f946-112">Area:</span></span>  <br/> |<span data-ttu-id="1f946-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="1f946-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f946-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1f946-114">Remarks</span></span>

<span data-ttu-id="1f946-115">Связанное содержимое таблицы представляет вложенной папке, которая не отображается в таблице стандартных содержимое.</span><span class="sxs-lookup"><span data-stu-id="1f946-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="1f946-116">Она содержит папку связанного или скрытым, сообщения.</span><span class="sxs-lookup"><span data-stu-id="1f946-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="1f946-117">Это свойство можно в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) для включения или исключения в [IMAPIProp::CopyProps](imapiprop-copyprops.md) операции.</span><span class="sxs-lookup"><span data-stu-id="1f946-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="1f946-118">Как свойство типа **PT_OBJECT**не может быть отменен успешно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) ; его содержимое должен осуществляться с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , запрашивающего идентификатор интерфейса **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="1f946-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="1f946-119">Поставщиков услуг должен сообщить о его в метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) если оно установлено, но может сообщать о его или не в том случае, если не указано.</span><span class="sxs-lookup"><span data-stu-id="1f946-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="1f946-120">Для получения содержимого таблицы, клиентские приложения необходимо вызвать метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="1f946-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="1f946-121">Дополнительные сведения о таблицах содержимое папки просмотрите [Содержимое таблицы](contents-tables.md) и [Отображение Содержание папки](displaying-a-folder-contents-table.md).</span><span class="sxs-lookup"><span data-stu-id="1f946-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="1f946-122">При использовании похожи **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) и это свойство.</span><span class="sxs-lookup"><span data-stu-id="1f946-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="1f946-123">Несколько свойств MAPI предоставляют доступ к таблицы:</span><span class="sxs-lookup"><span data-stu-id="1f946-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="1f946-124">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="1f946-124">**Property**</span></span>|<span data-ttu-id="1f946-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="1f946-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f946-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f946-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f946-127">Содержимое таблицы</span><span class="sxs-lookup"><span data-stu-id="1f946-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="1f946-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f946-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f946-129">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="1f946-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="1f946-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="1f946-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="1f946-131">Связанное содержимое таблицы</span><span class="sxs-lookup"><span data-stu-id="1f946-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="1f946-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f946-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f946-133">В таблице вложений</span><span class="sxs-lookup"><span data-stu-id="1f946-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="1f946-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="1f946-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="1f946-135">В таблице получателей</span><span class="sxs-lookup"><span data-stu-id="1f946-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1f946-136">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1f946-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1f946-137">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="1f946-137">Protocol specifications</span></span>

<span data-ttu-id="1f946-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f946-138">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f946-139">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1f946-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f946-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f946-140">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f946-141">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="1f946-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="1f946-142">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f946-142">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f946-143">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания элементов.</span><span class="sxs-lookup"><span data-stu-id="1f946-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f946-144">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="1f946-144">Header files</span></span>

<span data-ttu-id="1f946-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f946-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f946-146">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="1f946-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f946-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f946-147">Mapitags.h</span></span>
  
> <span data-ttu-id="1f946-148">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="1f946-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f946-149">См. также</span><span class="sxs-lookup"><span data-stu-id="1f946-149">See also</span></span>



[<span data-ttu-id="1f946-150">Каноническое свойство PidTagAssociatedContentCount</span><span class="sxs-lookup"><span data-stu-id="1f946-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="1f946-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1f946-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f946-152">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="1f946-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f946-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="1f946-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f946-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="1f946-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

