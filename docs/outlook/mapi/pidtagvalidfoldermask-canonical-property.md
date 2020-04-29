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
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="d74cd-103">Каноническое свойство PidTagValidFolderMask</span><span class="sxs-lookup"><span data-stu-id="d74cd-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="d74cd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d74cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d74cd-105">Содержит битовую маску флагов, указывающих допустимость идентификаторов записей папок в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="d74cd-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d74cd-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="d74cd-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d74cd-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="d74cd-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="d74cd-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="d74cd-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d74cd-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="d74cd-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="d74cd-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="d74cd-110">Data type:</span></span>  <br/> |<span data-ttu-id="d74cd-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d74cd-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d74cd-112">Область:</span><span class="sxs-lookup"><span data-stu-id="d74cd-112">Area:</span></span>  <br/> |<span data-ttu-id="d74cd-113">Хранилище сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="d74cd-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d74cd-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="d74cd-114">Remarks</span></span>

<span data-ttu-id="d74cd-115">Идентификатор записи папки может стать недопустимым, если пользователь удаляет папку или повреждено хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="d74cd-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="d74cd-116">Для битовой маски можно задать один или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="d74cd-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="d74cd-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="d74cd-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="d74cd-118">Папка "Общие представления" имеет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d74cd-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="d74cd-119">Просмотрите **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d74cd-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="d74cd-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="d74cd-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="d74cd-121">Папка Finder имеет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d74cd-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="d74cd-122">Просмотрите **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d74cd-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="d74cd-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="d74cd-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="d74cd-124">Папка приема сообщений (IPM) имеет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d74cd-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="d74cd-125">См. [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="d74cd-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="d74cd-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="d74cd-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="d74cd-127">В папке "Исходящие" IPM есть допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d74cd-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="d74cd-128">Просмотрите **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d74cd-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="d74cd-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="d74cd-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="d74cd-130">У папки IPM Sent Items допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d74cd-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="d74cd-131">Просмотрите **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d74cd-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="d74cd-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="d74cd-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="d74cd-133">Поддерево папки IPM имеет допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d74cd-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="d74cd-134">Просмотрите **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d74cd-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="d74cd-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="d74cd-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="d74cd-136">Папка "Удаленные" IPM содержит допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d74cd-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="d74cd-137">Просмотрите **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d74cd-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="d74cd-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="d74cd-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="d74cd-139">У папки Views допустимый идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="d74cd-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="d74cd-140">Просмотрите **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d74cd-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="d74cd-141">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="d74cd-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d74cd-142">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="d74cd-142">Header files</span></span>

<span data-ttu-id="d74cd-143">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="d74cd-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="d74cd-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="d74cd-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="d74cd-145">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="d74cd-145">Mapitags.h</span></span>
  
> <span data-ttu-id="d74cd-146">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="d74cd-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d74cd-147">См. также</span><span class="sxs-lookup"><span data-stu-id="d74cd-147">See also</span></span>



[<span data-ttu-id="d74cd-148">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="d74cd-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d74cd-149">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="d74cd-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d74cd-150">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="d74cd-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d74cd-151">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="d74cd-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

