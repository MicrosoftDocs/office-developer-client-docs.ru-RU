---
title: Каноническое свойство PidTagValidFolderMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427796"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="6b8fd-103">Каноническое свойство PidTagValidFolderMask</span><span class="sxs-lookup"><span data-stu-id="6b8fd-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="6b8fd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b8fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b8fd-105">Содержит битмаску флагов, которые указывают на действительность идентификаторов записей папок в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6b8fd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6b8fd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b8fd-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="6b8fd-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="6b8fd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6b8fd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6b8fd-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="6b8fd-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="6b8fd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6b8fd-110">Data type:</span></span>  <br/> |<span data-ttu-id="6b8fd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="6b8fd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="6b8fd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6b8fd-112">Area:</span></span>  <br/> |<span data-ttu-id="6b8fd-113">Хранилище сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="6b8fd-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b8fd-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6b8fd-114">Remarks</span></span>

<span data-ttu-id="6b8fd-115">Идентификатор записи папки может стать недействительным, если пользователь удаляет папку или если хранилище сообщений повреждено.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="6b8fd-116">Для bitmask можно установить один или несколько следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="6b8fd-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="6b8fd-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="6b8fd-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="6b8fd-118">Общая папка представлений имеет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="6b8fd-119">См. **PR_COMMON_VIEWS_ENTRYID** [(PidTagCommonViewsEntryId).](pidtagcommonviewsentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6b8fd-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="6b8fd-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="6b8fd-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="6b8fd-121">Папка поиска имеет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="6b8fd-122">См. **PR_FINDER_ENTRYID** [(PidTagFinderEntryId).](pidtagfinderentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6b8fd-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="6b8fd-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="6b8fd-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="6b8fd-124">Папка получения межличностного сообщения (IPM) имеет допустимый идентификатор входа.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="6b8fd-125">См. [в книге IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="6b8fd-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="6b8fd-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="6b8fd-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="6b8fd-127">Папка outbox IPM имеет допустимый идентификатор входа.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="6b8fd-128">См. **PR_IPM_OUTBOX_ENTRYID** [(PidTagIpmOutboxEntryId).](pidtagipmoutboxentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6b8fd-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="6b8fd-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="6b8fd-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="6b8fd-130">Папка отправленных элементов IPM имеет допустимый идентификатор входа.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="6b8fd-131">См. **PR_IPM_SENTMAIL_ENTRYID** [(PidTagIpmSentMailEntryId).](pidtagipmsentmailentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6b8fd-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="6b8fd-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="6b8fd-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="6b8fd-133">Подтрий папки IPM имеет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="6b8fd-134">См. **PR_IPM_SUBTREE_ENTRYID** [(PidTagIpmSubtreeEntryId).](pidtagipmsubtreeentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6b8fd-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="6b8fd-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="6b8fd-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="6b8fd-136">Папка удаленных элементов IPM имеет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="6b8fd-137">См. **PR_IPM_WASTEBASKET_ENTRYID** [(PidTagIpmWastebasketEntryId).](pidtagipmwastebasketentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6b8fd-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="6b8fd-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="6b8fd-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="6b8fd-139">Папка представлений имеет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="6b8fd-140">См. **PR_VIEWS_ENTRYID** [(PidTagViewsEntryId).](pidtagviewsentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="6b8fd-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="6b8fd-141">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6b8fd-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6b8fd-142">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="6b8fd-142">Header files</span></span>

<span data-ttu-id="6b8fd-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b8fd-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b8fd-144">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="6b8fd-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6b8fd-145">Mapitags.h</span></span>
  
> <span data-ttu-id="6b8fd-146">Содержит определения свойств, перечисленных в качестве альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="6b8fd-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b8fd-147">См. также</span><span class="sxs-lookup"><span data-stu-id="6b8fd-147">See also</span></span>



[<span data-ttu-id="6b8fd-148">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6b8fd-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b8fd-149">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6b8fd-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b8fd-150">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6b8fd-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b8fd-151">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="6b8fd-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

