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
# <a name="pidtagcontainerhierarchy-canonical-property"></a><span data-ttu-id="ef240-103">Каноническое свойство PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="ef240-103">PidTagContainerHierarchy Canonical Property</span></span>

  
  
<span data-ttu-id="ef240-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef240-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef240-105">Содержит внедренный объект таблицы иерархий, предоставляющий сведения о дочерних контейнерах.</span><span class="sxs-lookup"><span data-stu-id="ef240-105">Contains an embedded hierarchy table object that provides information about the child containers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ef240-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ef240-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ef240-107">PR_CONTAINER_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="ef240-107">PR_CONTAINER_HIERARCHY</span></span>  <br/> |
|<span data-ttu-id="ef240-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="ef240-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ef240-109">0x360E</span><span class="sxs-lookup"><span data-stu-id="ef240-109">0x360E</span></span>  <br/> |
|<span data-ttu-id="ef240-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ef240-110">Data type:</span></span>  <br/> |<span data-ttu-id="ef240-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="ef240-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="ef240-112">Область:</span><span class="sxs-lookup"><span data-stu-id="ef240-112">Area:</span></span>  <br/> |<span data-ttu-id="ef240-113">Container</span><span class="sxs-lookup"><span data-stu-id="ef240-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ef240-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="ef240-114">Remarks</span></span>

<span data-ttu-id="ef240-115">Это свойство можно исключить в [IMAPIProp:: операции CopyTo](imapiprop-copyto.md) или включено в [IMAPIProp:: копипропс](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="ef240-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="ef240-116">Как свойство типа **PT_OBJECT**, оно не может быть успешно получено методом [IMAPIProp::](imapiprop-getprops.md) GetProperty. к его содержимому должен получать доступ метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , запрашивающий идентификатор интерфейса IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="ef240-116">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="ef240-117">Поставщики услуг должны сообщить об этом в метод [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , если он задан, но при необходимости можно сообщить ему, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="ef240-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="ef240-118">Чтобы получить содержимое таблицы, клиентское приложение должно вызвать метод [IMAPIContainer:: жесиерарчитабле](imapicontainer-gethierarchytable.md) .</span><span class="sxs-lookup"><span data-stu-id="ef240-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) method.</span></span> <span data-ttu-id="ef240-119">Более подробную информацию можно узнать в статье [Иерархия Tables](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ef240-119">For more information, see [Hierarchy Tables](hierarchy-tables.md).</span></span> 
  
 <span data-ttu-id="ef240-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), и это свойство аналогично в использовании.</span><span class="sxs-lookup"><span data-stu-id="ef240-120">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="ef240-121">Несколько свойств MAPI предоставляют доступ к таблицам:</span><span class="sxs-lookup"><span data-stu-id="ef240-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="ef240-122">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="ef240-122">**Property**</span></span>|<span data-ttu-id="ef240-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="ef240-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef240-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef240-124">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef240-125">Таблица содержимого</span><span class="sxs-lookup"><span data-stu-id="ef240-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="ef240-126">**PR_CONTAINER_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="ef240-126">**PR_CONTAINER_HIERARCHY**</span></span> <br/> |<span data-ttu-id="ef240-127">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="ef240-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="ef240-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef240-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef240-129">Связанная таблица содержимого</span><span class="sxs-lookup"><span data-stu-id="ef240-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="ef240-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef240-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef240-131">Таблица вложений</span><span class="sxs-lookup"><span data-stu-id="ef240-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="ef240-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ef240-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ef240-133">Таблица получателей</span><span class="sxs-lookup"><span data-stu-id="ef240-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ef240-134">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ef240-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ef240-135">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ef240-135">Protocol specifications</span></span>

<span data-ttu-id="ef240-136">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef240-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef240-137">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ef240-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ef240-138">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef240-138">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef240-139">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="ef240-139">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="ef240-140">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef240-140">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ef240-141">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="ef240-141">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ef240-142">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ef240-142">Header files</span></span>

<span data-ttu-id="ef240-143">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="ef240-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="ef240-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ef240-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="ef240-145">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="ef240-145">Mapitags.h</span></span>
  
> <span data-ttu-id="ef240-146">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="ef240-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef240-147">См. также</span><span class="sxs-lookup"><span data-stu-id="ef240-147">See also</span></span>



[<span data-ttu-id="ef240-148">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ef240-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ef240-149">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="ef240-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ef240-150">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ef240-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ef240-151">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ef240-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

