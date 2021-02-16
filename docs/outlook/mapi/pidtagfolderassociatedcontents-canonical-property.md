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
# <a name="pidtagfolderassociatedcontents-canonical-property"></a><span data-ttu-id="69e60-103">Каноническое свойство PidTagFolderAssociatedContents</span><span class="sxs-lookup"><span data-stu-id="69e60-103">PidTagFolderAssociatedContents Canonical Property</span></span>

  
  
<span data-ttu-id="69e60-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69e60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69e60-105">Содержит встроенный объект таблицы содержимого, который предоставляет сведения о связанной таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="69e60-105">Contains an embedded contents table object that provides information about the associated contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="69e60-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="69e60-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="69e60-107">PR_FOLDER_ASSOCIATED_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="69e60-107">PR_FOLDER_ASSOCIATED_CONTENTS</span></span>  <br/> |
|<span data-ttu-id="69e60-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="69e60-108">Identifier:</span></span>  <br/> |<span data-ttu-id="69e60-109">0x3610</span><span class="sxs-lookup"><span data-stu-id="69e60-109">0x3610</span></span>  <br/> |
|<span data-ttu-id="69e60-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="69e60-110">Data type:</span></span>  <br/> |<span data-ttu-id="69e60-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="69e60-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="69e60-112">Область:</span><span class="sxs-lookup"><span data-stu-id="69e60-112">Area:</span></span>  <br/> |<span data-ttu-id="69e60-113">Контейнер MAPI</span><span class="sxs-lookup"><span data-stu-id="69e60-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69e60-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="69e60-114">Remarks</span></span>

<span data-ttu-id="69e60-115">Связанная таблица содержимого представляет в подчиненную, которая не появляется в стандартной таблице содержимого.</span><span class="sxs-lookup"><span data-stu-id="69e60-115">The associated contents table represents a subfolder that does not appear in the standard contents table.</span></span> <span data-ttu-id="69e60-116">Он содержит связанные или скрытые сообщения папки.</span><span class="sxs-lookup"><span data-stu-id="69e60-116">It contains the folder's associated, or hidden, messages.</span></span> 
  
<span data-ttu-id="69e60-117">Это свойство можно исключить в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в операции [IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="69e60-117">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="69e60-118">В качестве свойства типа **PT_OBJECT** его невозможно получить с помощью метода [IMAPIProp::GetProps;](imapiprop-getprops.md) Доступ к его содержимому должен получить метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивающий идентификатор IID_IMAPITable интерфейса. </span><span class="sxs-lookup"><span data-stu-id="69e60-118">As a property of type **PT_OBJECT**, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="69e60-119">Поставщики служб должны сообщить о нем методу [IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он установлен, но при желании может сообщить о нем или нет, если он не за установлен.</span><span class="sxs-lookup"><span data-stu-id="69e60-119">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="69e60-120">Чтобы получить содержимое таблицы, клиентские приложения должны вызывать метод [IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md)</span><span class="sxs-lookup"><span data-stu-id="69e60-120">To retrieve table contents, client applications should call the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method.</span></span> <span data-ttu-id="69e60-121">Дополнительные сведения о таблицах содержимого папок см. в таблицах "Содержимое" и "Отображение [](contents-tables.md) [таблицы содержимого папки".](displaying-a-folder-contents-table.md)</span><span class="sxs-lookup"><span data-stu-id="69e60-121">For more information on folder contents tables, see [Contents Tables](contents-tables.md) and [Displaying a Folder Contents Table](displaying-a-folder-contents-table.md).</span></span> 
  
<span data-ttu-id="69e60-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy),](pidtagcontainerhierarchy-canonical-property.md)and this property are similar in usage.</span><span class="sxs-lookup"><span data-stu-id="69e60-122">The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)), and this property are similar in usage.</span></span> <span data-ttu-id="69e60-123">Доступ к таблицам предоставляется несколькими свойствами MAPI:</span><span class="sxs-lookup"><span data-stu-id="69e60-123">Several MAPI properties provide access to tables:</span></span> 
  
|<span data-ttu-id="69e60-124">**Property**</span><span class="sxs-lookup"><span data-stu-id="69e60-124">**Property**</span></span>|<span data-ttu-id="69e60-125">**Table**</span><span class="sxs-lookup"><span data-stu-id="69e60-125">**Table**</span></span>|
|:-----|:-----|
|<span data-ttu-id="69e60-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="69e60-126">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69e60-127">Таблица Contents</span><span class="sxs-lookup"><span data-stu-id="69e60-127">Contents table</span></span>  <br/> |
|<span data-ttu-id="69e60-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="69e60-128">**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69e60-129">Таблица Hierarchy</span><span class="sxs-lookup"><span data-stu-id="69e60-129">Hierarchy table</span></span>  <br/> |
|<span data-ttu-id="69e60-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span><span class="sxs-lookup"><span data-stu-id="69e60-130">**PR_FOLDER_ASSOCIATED_CONTENTS**</span></span> <br/> |<span data-ttu-id="69e60-131">Связанная таблица содержимого</span><span class="sxs-lookup"><span data-stu-id="69e60-131">Associated contents table</span></span>  <br/> |
|<span data-ttu-id="69e60-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="69e60-132">**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69e60-133">Таблица Attachment</span><span class="sxs-lookup"><span data-stu-id="69e60-133">Attachment table</span></span>  <br/> |
|<span data-ttu-id="69e60-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="69e60-134">**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="69e60-135">Таблица Recipient</span><span class="sxs-lookup"><span data-stu-id="69e60-135">Recipient table</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="69e60-136">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="69e60-136">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="69e60-137">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="69e60-137">Protocol specifications</span></span>

<span data-ttu-id="69e60-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69e60-138">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69e60-139">Содержит ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="69e60-139">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="69e60-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69e60-140">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69e60-141">Обрабатывает порядок и поток передачи данных между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="69e60-141">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="69e60-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="69e60-142">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="69e60-143">Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также элементами встреч и собраний.</span><span class="sxs-lookup"><span data-stu-id="69e60-143">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting items.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="69e60-144">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="69e60-144">Header files</span></span>

<span data-ttu-id="69e60-145">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="69e60-145">Mapidefs.h</span></span>
  
> <span data-ttu-id="69e60-146">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="69e60-146">Provides data type definitions.</span></span>
    
<span data-ttu-id="69e60-147">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="69e60-147">Mapitags.h</span></span>
  
> <span data-ttu-id="69e60-148">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="69e60-148">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69e60-149">См. также</span><span class="sxs-lookup"><span data-stu-id="69e60-149">See also</span></span>



[<span data-ttu-id="69e60-150">Каноническое свойство PidTagAssociatedContentCount</span><span class="sxs-lookup"><span data-stu-id="69e60-150">PidTagAssociatedContentCount Canonical Property</span></span>](pidtagassociatedcontentcount-canonical-property.md)


[<span data-ttu-id="69e60-151">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69e60-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="69e60-152">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="69e60-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="69e60-153">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="69e60-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="69e60-154">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="69e60-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

