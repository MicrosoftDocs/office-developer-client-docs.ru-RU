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
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332860"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="db9ce-103">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="db9ce-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="db9ce-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db9ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db9ce-105">Содержит встроенный объект таблицы иерархии, который предоставляет сведения о child containers.</span><span class="sxs-lookup"><span data-stu-id="db9ce-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db9ce-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="db9ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="db9ce-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="db9ce-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="db9ce-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="db9ce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="db9ce-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="db9ce-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="db9ce-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="db9ce-110">Data type:</span></span>  <br/> |<span data-ttu-id="db9ce-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="db9ce-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="db9ce-112">Область:</span><span class="sxs-lookup"><span data-stu-id="db9ce-112">Area:</span></span>  <br/> |<span data-ttu-id="db9ce-113">Container</span><span class="sxs-lookup"><span data-stu-id="db9ce-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db9ce-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="db9ce-114">Remarks</span></span>

<span data-ttu-id="db9ce-115">Это свойство можно исключить в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в операции [IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="db9ce-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="db9ce-116">В качестве свойства типа **PT_OBJECT** его не удается получить с помощью метода [IMAPIProp::GetProps;](imapiprop-getprops.md) Доступ к его содержимому должен получить метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивающий идентификатор IID_IMAPITable интерфейса.</span><span class="sxs-lookup"><span data-stu-id="db9ce-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="db9ce-117">Поставщики служб должны сообщить об этом методу [IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он установлен, но при желании может сообщить о нем или нет, если он не установлен.</span><span class="sxs-lookup"><span data-stu-id="db9ce-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="db9ce-118">Чтобы получить содержимое таблицы, клиентские приложения должны вызвать [метод IMAPIContainer::GetHierarchyTable.](imapicontainer-gethierarchytable.md)</span><span class="sxs-lookup"><span data-stu-id="db9ce-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="db9ce-119">Дополнительные сведения см. [в таблицах иерархии.](hierarchy-tables.md)</span><span class="sxs-lookup"><span data-stu-id="db9ce-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="db9ce-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents),](pidtagcontainercontents-canonical-property.md) **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents),](pidtagfolderassociatedcontents-canonical-property.md)и это свойство похожи в использовании.</span><span class="sxs-lookup"><span data-stu-id="db9ce-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="db9ce-121">Доступ к таблицам предоставляется несколькими свойствами MAPI:</span><span class="sxs-lookup"><span data-stu-id="db9ce-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="db9ce-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="db9ce-122">**Property**</span></span>|<span data-ttu-id="db9ce-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="db9ce-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="db9ce-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db9ce-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="db9ce-125">Таблица Contents</span><span class="sxs-lookup"><span data-stu-id="db9ce-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="db9ce-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="db9ce-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="db9ce-127">Таблица Hierarchy</span><span class="sxs-lookup"><span data-stu-id="db9ce-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="db9ce-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db9ce-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="db9ce-129">Связанная таблица содержимого</span><span class="sxs-lookup"><span data-stu-id="db9ce-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="db9ce-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db9ce-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="db9ce-131">Таблица Attachment</span><span class="sxs-lookup"><span data-stu-id="db9ce-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="db9ce-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db9ce-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="db9ce-133">Таблица Recipient</span><span class="sxs-lookup"><span data-stu-id="db9ce-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="db9ce-134">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="db9ce-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="db9ce-135">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="db9ce-135">Protocol specifications</span></span>

<span data-ttu-id="db9ce-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db9ce-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db9ce-137">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="db9ce-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="db9ce-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db9ce-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db9ce-139">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="db9ce-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="db9ce-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="db9ce-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="db9ce-141">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="db9ce-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="db9ce-142">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="db9ce-142">Header files</span></span>

<span data-ttu-id="db9ce-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="db9ce-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="db9ce-144">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="db9ce-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="db9ce-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="db9ce-145">Mapitags.h</span></span>
  
> <span data-ttu-id="db9ce-146">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="db9ce-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db9ce-147">См. также</span><span class="sxs-lookup"><span data-stu-id="db9ce-147">See also</span></span>



[<span data-ttu-id="db9ce-148">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="db9ce-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="db9ce-149">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="db9ce-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="db9ce-150">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="db9ce-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="db9ce-151">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="db9ce-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

