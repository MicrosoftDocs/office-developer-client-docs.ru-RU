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
# <a name="pidtagcontainercontents-canonical-property"></a><span data-ttu-id="39409-103">Каноническое свойство PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="39409-103">PidTagContainerContents Canonical Property</span></span>

  
  
<span data-ttu-id="39409-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39409-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39409-105">Содержит внедренный объект таблицы содержимого, предоставляющий сведения о контейнере.</span><span class="sxs-lookup"><span data-stu-id="39409-105">Contains an embedded contents table object that provides information about a container.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39409-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="39409-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39409-107">ПР_КОНТАИНЕР_КОНТЕНТС</span><span class="sxs-lookup"><span data-stu-id="39409-107">PR_CONTAINER_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="39409-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="39409-108">Identifier:</span></span>  <br/> |<span data-ttu-id="39409-109">0x360F</span><span class="sxs-lookup"><span data-stu-id="39409-109">0x360F</span></span>  <br/> |
|<span data-ttu-id="39409-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="39409-110">Data type:</span></span>  <br/> |<span data-ttu-id="39409-111">ПТ_ОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="39409-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="39409-112">Область:</span><span class="sxs-lookup"><span data-stu-id="39409-112">Area:</span></span>  <br/> |<span data-ttu-id="39409-113">Container</span><span class="sxs-lookup"><span data-stu-id="39409-113">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39409-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="39409-114">Remarks</span></span>

<span data-ttu-id="39409-115">Это свойство можно исключить в [IMAPIProp:: операции CopyTo](imapiprop-copyto.md) или включено в [IMAPIProp:: копипропс](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="39409-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="39409-116">Как свойство типа ПТ_ОБЖЕКТ, оно не может быть успешно получено методом [IMAPIProp::](imapiprop-getprops.md) ; к его содержимому должен получать доступ метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , запрашивающий идентификатор интерфейса иид_имапитабле.</span><span class="sxs-lookup"><span data-stu-id="39409-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the IID_IMAPITable interface identifier.</span></span> <span data-ttu-id="39409-117">Поставщики услуг должны сообщить об этом в метод [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , если он задан, но при необходимости можно сообщить ему, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="39409-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="39409-118">Чтобы получить содержимое таблицы, клиентское приложение должно вызвать метод [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="39409-118">To retrieve table contents, a client application should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="39409-119">For more information, see [���������� �������](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="39409-119">For more information, see [Contents Tables](contents-tables.md).</span></span> 
  
<span data-ttu-id="39409-120">Это свойство, **пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) и **пр_фолдер_ассоЦиатед_контентс** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) аналогично в использовании.</span><span class="sxs-lookup"><span data-stu-id="39409-120">This property, **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) , and **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) are similar in usage.</span></span> <span data-ttu-id="39409-121">Несколько свойств MAPI предоставляют доступ к таблицам:</span><span class="sxs-lookup"><span data-stu-id="39409-121">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="39409-122">**Property**</span><span class="sxs-lookup"><span data-stu-id="39409-122">**Property**</span></span>|<span data-ttu-id="39409-123">**Table**</span><span class="sxs-lookup"><span data-stu-id="39409-123">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="39409-124">PidTagContainerContents</span><span class="sxs-lookup"><span data-stu-id="39409-124">PidTagContainerContents</span></span>  <br/> |<span data-ttu-id="39409-125">Таблица содержимого</span><span class="sxs-lookup"><span data-stu-id="39409-125">Contents table</span></span>  <br/> |
|<span data-ttu-id="39409-126">**Пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39409-126">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39409-127">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="39409-127">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="39409-128">**Пр_фолдер_ассоЦиатед_контентс** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39409-128">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39409-129">Связанная таблица содержимого</span><span class="sxs-lookup"><span data-stu-id="39409-129">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="39409-130">**Пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39409-130">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39409-131">Таблица вложений</span><span class="sxs-lookup"><span data-stu-id="39409-131">Attachment table</span></span>  <br/> |
|<span data-ttu-id="39409-132">**Пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="39409-132">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="39409-133">Таблица получателей</span><span class="sxs-lookup"><span data-stu-id="39409-133">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="39409-134">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="39409-134">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39409-135">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="39409-135">Protocol specifications</span></span>

<span data-ttu-id="39409-136">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39409-136">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39409-137">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="39409-137">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="39409-138">[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39409-138">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39409-139">Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39409-139">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39409-140">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="39409-140">Header files</span></span>

<span data-ttu-id="39409-141">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="39409-141">Mapidefs.h</span></span>
  
> <span data-ttu-id="39409-142">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="39409-142">Provides data type definitions.</span></span>
    
<span data-ttu-id="39409-143">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="39409-143">Mapitags.h</span></span>
  
> <span data-ttu-id="39409-144">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="39409-144">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39409-145">См. также</span><span class="sxs-lookup"><span data-stu-id="39409-145">See also</span></span>



[<span data-ttu-id="39409-146">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="39409-146">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39409-147">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="39409-147">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39409-148">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="39409-148">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39409-149">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="39409-149">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

