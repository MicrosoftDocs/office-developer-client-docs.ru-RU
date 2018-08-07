---
title: Каноническое свойство PidTagContainerContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c2979a0825ad6c62dbbb7931255501e90d8450a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810970"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="12ad6-103">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="12ad6-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="12ad6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="12ad6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="12ad6-105">Содержит объект внедренного содержимого таблицы, предоставляющий информацию о контейнером.</span><span class="sxs-lookup"><span data-stu-id="12ad6-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12ad6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="12ad6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12ad6-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="12ad6-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="12ad6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="12ad6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="12ad6-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="12ad6-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="12ad6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="12ad6-110">Data type:</span></span>  <br/> |<span data-ttu-id="12ad6-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="12ad6-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="12ad6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="12ad6-112">Area:</span></span>  <br/> |<span data-ttu-id="12ad6-113">Контейнер</span><span class="sxs-lookup"><span data-stu-id="12ad6-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12ad6-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="12ad6-114">Remarks</span></span>

<span data-ttu-id="12ad6-115">Это свойство можно в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) для включения или исключения в [IMAPIProp::CopyProps](imapiprop-copyprops.md) операции.</span><span class="sxs-lookup"><span data-stu-id="12ad6-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="12ad6-116">Как свойство типа PT_OBJECT не может быть отменен успешно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) ; его содержимое должен осуществляться с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , запрашивающего идентификатор интерфейса IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="12ad6-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="12ad6-117">Поставщиков услуг должен сообщить о его в метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) если он имеет значение, но при необходимости можно сообщить или не в том случае, если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="12ad6-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="12ad6-118">Чтобы извлечь содержимое таблицы, клиентское приложение следует вызовите метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="12ad6-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="12ad6-119">For more information, see [���������� �������](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="12ad6-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="12ad6-120">Это свойство **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) и **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) похожи в использовании.</span><span class="sxs-lookup"><span data-stu-id="12ad6-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="12ad6-121">Несколько свойств MAPI предоставляют доступ к таблицы:</span><span class="sxs-lookup"><span data-stu-id="12ad6-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="12ad6-122">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="12ad6-122">**Property**</span></span>|<span data-ttu-id="12ad6-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="12ad6-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12ad6-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="12ad6-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="12ad6-125">Содержимое таблицы</span><span class="sxs-lookup"><span data-stu-id="12ad6-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="12ad6-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12ad6-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="12ad6-127">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="12ad6-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="12ad6-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12ad6-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="12ad6-129">Связанное содержимое таблицы</span><span class="sxs-lookup"><span data-stu-id="12ad6-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="12ad6-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12ad6-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="12ad6-131">В таблице вложений</span><span class="sxs-lookup"><span data-stu-id="12ad6-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="12ad6-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="12ad6-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="12ad6-133">В таблице получателей</span><span class="sxs-lookup"><span data-stu-id="12ad6-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="12ad6-134">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="12ad6-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12ad6-135">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="12ad6-135">Protocol specifications</span></span>

<span data-ttu-id="12ad6-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12ad6-136">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12ad6-137">Содержит ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="12ad6-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12ad6-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12ad6-138">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12ad6-139">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12ad6-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12ad6-140">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="12ad6-140">Header files</span></span>

<span data-ttu-id="12ad6-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="12ad6-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="12ad6-142">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="12ad6-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="12ad6-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="12ad6-143">Mapitags.h</span></span>
  
> <span data-ttu-id="12ad6-144">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="12ad6-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12ad6-145">См. также</span><span class="sxs-lookup"><span data-stu-id="12ad6-145">See also</span></span>



[<span data-ttu-id="12ad6-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12ad6-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12ad6-147">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="12ad6-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12ad6-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="12ad6-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12ad6-149">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="12ad6-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

