---
title: Каноническое свойство PidTagContainerHierarchy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2c9598b583ba62adc42d6fb2b904dfe4981286ff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578110"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="53e78-103">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="53e78-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="53e78-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53e78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53e78-105">Содержит объект таблицы внедренных иерархии, предоставляющий информацию о дочерних контейнеров.</span><span class="sxs-lookup"><span data-stu-id="53e78-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53e78-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="53e78-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53e78-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="53e78-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="53e78-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="53e78-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53e78-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="53e78-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="53e78-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="53e78-110">Data type:</span></span>  <br/> |<span data-ttu-id="53e78-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="53e78-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="53e78-112">Область:</span><span class="sxs-lookup"><span data-stu-id="53e78-112">Area:</span></span>  <br/> |<span data-ttu-id="53e78-113">Контейнер</span><span class="sxs-lookup"><span data-stu-id="53e78-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53e78-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="53e78-114">Remarks</span></span>

<span data-ttu-id="53e78-115">Это свойство можно в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) для включения или исключения в [IMAPIProp::CopyProps](imapiprop-copyprops.md) операции.</span><span class="sxs-lookup"><span data-stu-id="53e78-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="53e78-116">Как свойство типа **PT_OBJECT**не может быть отменен успешно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) ; его содержимое должен осуществляться с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , запрашивающего идентификатор интерфейса IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="53e78-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="53e78-117">Поставщиков услуг должен сообщить о его в метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) если он имеет значение, но при необходимости можно сообщить или не в том случае, если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="53e78-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="53e78-118">Чтобы извлечь содержимое таблицы, клиентское приложение следует вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) .</span><span class="sxs-lookup"><span data-stu-id="53e78-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="53e78-119">Для получения дополнительных сведений см [Таблиц иерархии](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="53e78-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="53e78-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), а это свойство похожи в использовании.</span><span class="sxs-lookup"><span data-stu-id="53e78-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="53e78-121">Несколько свойств MAPI предоставляют доступ к таблицы:</span><span class="sxs-lookup"><span data-stu-id="53e78-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="53e78-122">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="53e78-122">**Property**</span></span>|<span data-ttu-id="53e78-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="53e78-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="53e78-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53e78-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53e78-125">Содержимое таблицы</span><span class="sxs-lookup"><span data-stu-id="53e78-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="53e78-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="53e78-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="53e78-127">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="53e78-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="53e78-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53e78-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53e78-129">Связанное содержимое таблицы</span><span class="sxs-lookup"><span data-stu-id="53e78-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="53e78-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53e78-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53e78-131">В таблице вложений</span><span class="sxs-lookup"><span data-stu-id="53e78-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="53e78-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="53e78-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="53e78-133">В таблице получателей</span><span class="sxs-lookup"><span data-stu-id="53e78-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="53e78-134">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="53e78-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53e78-135">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="53e78-135">Protocol specifications</span></span>

<span data-ttu-id="53e78-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53e78-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53e78-137">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="53e78-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53e78-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53e78-138">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53e78-139">Обрабатывает порядок и поток для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="53e78-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="53e78-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53e78-140">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53e78-141">Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.</span><span class="sxs-lookup"><span data-stu-id="53e78-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53e78-142">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="53e78-142">Header files</span></span>

<span data-ttu-id="53e78-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53e78-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="53e78-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="53e78-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="53e78-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="53e78-145">Mapitags.h</span></span>
  
> <span data-ttu-id="53e78-146">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="53e78-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53e78-147">См. также</span><span class="sxs-lookup"><span data-stu-id="53e78-147">See also</span></span>



[<span data-ttu-id="53e78-148">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="53e78-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="53e78-149">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="53e78-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="53e78-150">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="53e78-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="53e78-151">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="53e78-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

