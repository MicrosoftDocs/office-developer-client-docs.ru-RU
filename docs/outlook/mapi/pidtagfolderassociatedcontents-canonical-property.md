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
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316305"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="dbe92-103">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="dbe92-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="dbe92-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbe92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbe92-105">Содержит внедренный объект таблицы содержимого, предоставляющий сведения о связанной таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="dbe92-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbe92-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="dbe92-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dbe92-107">ПР_ФОЛДЕР_АССОЦИАТЕД_КОНТЕНТС</span><span class="sxs-lookup"><span data-stu-id="dbe92-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="dbe92-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dbe92-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dbe92-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="dbe92-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="dbe92-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="dbe92-110">Data type:</span></span>  <br/> |<span data-ttu-id="dbe92-111">ПТ_ОБЖЕКТ</span><span class="sxs-lookup"><span data-stu-id="dbe92-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="dbe92-112">Область:</span><span class="sxs-lookup"><span data-stu-id="dbe92-112">Area:</span></span>  <br/> |<span data-ttu-id="dbe92-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="dbe92-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbe92-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="dbe92-114">Remarks</span></span>

<span data-ttu-id="dbe92-115">Связанная таблица содержимого представляет вложенную папку, которая не отображается в стандартной таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="dbe92-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="dbe92-116">Он содержит связанные или скрытые сообщения для папки.</span><span class="sxs-lookup"><span data-stu-id="dbe92-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="dbe92-117">Это свойство можно исключить в [IMAPIProp:: операции CopyTo](imapiprop-copyto.md) или включено в [IMAPIProp:: копипропс](imapiprop-copyprops.md) Operations.</span><span class="sxs-lookup"><span data-stu-id="dbe92-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="dbe92-118">Как свойство типа **пт_обжект**, оно не может быть успешно получено методом [IMAPIProp::](imapiprop-getprops.md) ; к его содержимому должен получать доступ метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , запрашивающий идентификатор интерфейса **иид_имапитабле** .</span><span class="sxs-lookup"><span data-stu-id="dbe92-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="dbe92-119">Поставщики услуг должны сообщить о ней методу [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , если он задан, но при необходимости можно сообщить ему, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="dbe92-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="dbe92-120">Чтобы получить содержимое таблицы, клиентские приложения должны вызвать метод [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md) .</span><span class="sxs-lookup"><span data-stu-id="dbe92-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="dbe92-121">Для получения дополнительных сведений о таблицах содержимого папок [](contents-tables.md) ознакомьтесь с таблицами оглавления и [отображением таблицы содержимое папки](displaying-a-folder-contents-table.md).</span><span class="sxs-lookup"><span data-stu-id="dbe92-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="dbe92-122">**Пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) и это свойство аналогичны в использовании.</span><span class="sxs-lookup"><span data-stu-id="dbe92-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="dbe92-123">Несколько свойств MAPI предоставляют доступ к таблицам:</span><span class="sxs-lookup"><span data-stu-id="dbe92-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="dbe92-124">**Property**</span><span class="sxs-lookup"><span data-stu-id="dbe92-124">**Property**</span></span>|<span data-ttu-id="dbe92-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="dbe92-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dbe92-126">**Пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dbe92-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dbe92-127">Таблица содержимого</span><span class="sxs-lookup"><span data-stu-id="dbe92-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="dbe92-128">**Пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dbe92-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dbe92-129">Таблица иерархии</span><span class="sxs-lookup"><span data-stu-id="dbe92-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="dbe92-130">**ПР_ФОЛДЕР_АССОЦИАТЕД_КОНТЕНТС**</span><span class="sxs-lookup"><span data-stu-id="dbe92-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="dbe92-131">Связанная таблица содержимого</span><span class="sxs-lookup"><span data-stu-id="dbe92-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="dbe92-132">**Пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dbe92-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dbe92-133">Таблица вложений</span><span class="sxs-lookup"><span data-stu-id="dbe92-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="dbe92-134">**Пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="dbe92-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="dbe92-135">Таблица получателей</span><span class="sxs-lookup"><span data-stu-id="dbe92-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="dbe92-136">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="dbe92-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dbe92-137">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="dbe92-137">Protocol specifications</span></span>

<span data-ttu-id="dbe92-138">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dbe92-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dbe92-139">Содержит ссылки на соответствующие спецификации протоколов Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dbe92-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dbe92-140">[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dbe92-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dbe92-141">Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="dbe92-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="dbe92-142">[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dbe92-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dbe92-143">Преобразование между IETF RFC2445, RFC2446 и RFC2447, а элементы встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="dbe92-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dbe92-144">Файлы заГоловков</span><span class="sxs-lookup"><span data-stu-id="dbe92-144">Header files</span></span>

<span data-ttu-id="dbe92-145">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="dbe92-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="dbe92-146">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="dbe92-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="dbe92-147">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="dbe92-147">Mapitags.h</span></span>
  
> <span data-ttu-id="dbe92-148">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="dbe92-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dbe92-149">См. также</span><span class="sxs-lookup"><span data-stu-id="dbe92-149">See also</span></span>



[<span data-ttu-id="dbe92-150">Каноническое свойство PidTagAssociatedContentCount</span><span class="sxs-lookup"><span data-stu-id="dbe92-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="dbe92-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="dbe92-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dbe92-152">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="dbe92-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dbe92-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="dbe92-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dbe92-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="dbe92-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

