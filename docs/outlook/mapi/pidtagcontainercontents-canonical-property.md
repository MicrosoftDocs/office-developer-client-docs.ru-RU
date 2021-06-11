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
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283130"
---
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="f13fe-103">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="f13fe-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="f13fe-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f13fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f13fe-105">Содержит встроенный объект таблицы содержимого, который предоставляет сведения о контейнере.</span><span class="sxs-lookup"><span data-stu-id="f13fe-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f13fe-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="f13fe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f13fe-107">PR_CONTAINER_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="f13fe-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="f13fe-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f13fe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f13fe-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="f13fe-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="f13fe-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="f13fe-110">Data type:</span></span>  <br/> |<span data-ttu-id="f13fe-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="f13fe-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="f13fe-112">Область:</span><span class="sxs-lookup"><span data-stu-id="f13fe-112">Area:</span></span>  <br/> |<span data-ttu-id="f13fe-113">Container</span><span class="sxs-lookup"><span data-stu-id="f13fe-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f13fe-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="f13fe-114">Remarks</span></span>

<span data-ttu-id="f13fe-115">Это свойство можно исключить в [операциях IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в [операции IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="f13fe-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="f13fe-116">Как свойство типа PT_OBJECT, его невозможно успешно получить [методом IMAPIProp::GetProps;](imapiprop-getprops.md) Его содержимое должно быть доступны [методом IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивая идентификатор IID_IMAPITable интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f13fe-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="f13fe-117">Поставщики услуг должны сообщить об этом [методу IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он за установлен, но может сообщить об этом или нет, если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="f13fe-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="f13fe-118">Чтобы получить содержимое таблицы, клиентская заявка должна вызвать [метод IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md)</span><span class="sxs-lookup"><span data-stu-id="f13fe-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="f13fe-119">For more information, see [���������� �������](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f13fe-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="f13fe-120">Это свойство **PR_CONTAINER_HIERARCHY** [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)и **PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)похожи по использованию.</span><span class="sxs-lookup"><span data-stu-id="f13fe-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="f13fe-121">Несколько свойств MAPI предоставляют доступ к таблицам:</span><span class="sxs-lookup"><span data-stu-id="f13fe-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="f13fe-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="f13fe-122">**Property**</span></span>|<span data-ttu-id="f13fe-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="f13fe-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f13fe-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="f13fe-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="f13fe-125">Таблица контента</span><span class="sxs-lookup"><span data-stu-id="f13fe-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="f13fe-126">**PR_CONTAINER_HIERARCHY** [(PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f13fe-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f13fe-127">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="f13fe-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="f13fe-128">**PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f13fe-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f13fe-129">Связанная таблица контента</span><span class="sxs-lookup"><span data-stu-id="f13fe-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="f13fe-130">**PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f13fe-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f13fe-131">Таблица вложений</span><span class="sxs-lookup"><span data-stu-id="f13fe-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="f13fe-132">**PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="f13fe-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="f13fe-133">Таблица получателей</span><span class="sxs-lookup"><span data-stu-id="f13fe-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f13fe-134">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f13fe-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f13fe-135">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="f13fe-135">Protocol specifications</span></span>

<span data-ttu-id="f13fe-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f13fe-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f13fe-137">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="f13fe-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f13fe-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f13fe-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f13fe-139">Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f13fe-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f13fe-140">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="f13fe-140">Header files</span></span>

<span data-ttu-id="f13fe-141">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f13fe-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="f13fe-142">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="f13fe-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="f13fe-143">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f13fe-143">Mapitags.h</span></span>
  
> <span data-ttu-id="f13fe-144">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="f13fe-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f13fe-145">См. также</span><span class="sxs-lookup"><span data-stu-id="f13fe-145">See also</span></span>



[<span data-ttu-id="f13fe-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f13fe-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f13fe-147">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="f13fe-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f13fe-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="f13fe-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f13fe-149">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="f13fe-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

