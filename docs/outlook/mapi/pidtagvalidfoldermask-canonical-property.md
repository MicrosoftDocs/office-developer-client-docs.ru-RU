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
ms.openlocfilehash: ae09723c78fe4e333fb5c46e8c79da4b77c0b331
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812043"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="b17d7-103">Каноническое свойство PidTagValidFolderMask</span><span class="sxs-lookup"><span data-stu-id="b17d7-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="b17d7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b17d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b17d7-105">Содержит битовую маску флагов, указывающие на правильность идентификаторы записей папок в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="b17d7-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b17d7-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="b17d7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b17d7-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="b17d7-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="b17d7-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="b17d7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b17d7-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="b17d7-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="b17d7-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="b17d7-110">Data type:</span></span>  <br/> |<span data-ttu-id="b17d7-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="b17d7-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="b17d7-112">Область:</span><span class="sxs-lookup"><span data-stu-id="b17d7-112">Area:</span></span>  <br/> |<span data-ttu-id="b17d7-113">Хранение сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="b17d7-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b17d7-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="b17d7-114">Remarks</span></span>

<span data-ttu-id="b17d7-115">Идентификатор записи папки могут стать недопустимыми, если пользователь удаляет папку или повреждения хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="b17d7-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="b17d7-116">Для Битовая маска, которая может быть установлено одно или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="b17d7-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="b17d7-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="b17d7-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="b17d7-118">Общие папки "представления" имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="b17d7-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="b17d7-119">В разделе **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b17d7-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="b17d7-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="b17d7-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="b17d7-121">Папки поиска с идентификатором записей.</span><span class="sxs-lookup"><span data-stu-id="b17d7-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="b17d7-122">В разделе **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b17d7-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="b17d7-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="b17d7-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="b17d7-124">Получать сообщения электронной почты — это (IPM) папки с идентификатором записей.</span><span class="sxs-lookup"><span data-stu-id="b17d7-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="b17d7-125">В разделе [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="b17d7-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="b17d7-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="b17d7-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="b17d7-127">Папка исходящих IPM имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="b17d7-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="b17d7-128">В разделе **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b17d7-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="b17d7-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="b17d7-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="b17d7-130">Папка Отправленные IPM имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="b17d7-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="b17d7-131">В разделе **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b17d7-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="b17d7-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="b17d7-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="b17d7-133">Папка поддерева IPM имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="b17d7-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="b17d7-134">В разделе **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b17d7-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="b17d7-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="b17d7-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="b17d7-136">Папки "Удаленные IPM" имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="b17d7-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="b17d7-137">В разделе **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b17d7-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="b17d7-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="b17d7-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="b17d7-139">Папки "представления" имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="b17d7-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="b17d7-140">В разделе **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b17d7-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="b17d7-141">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="b17d7-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b17d7-142">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="b17d7-142">Header files</span></span>

<span data-ttu-id="b17d7-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b17d7-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="b17d7-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="b17d7-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="b17d7-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b17d7-145">Mapitags.h</span></span>
  
> <span data-ttu-id="b17d7-146">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="b17d7-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b17d7-147">См. также</span><span class="sxs-lookup"><span data-stu-id="b17d7-147">See also</span></span>



[<span data-ttu-id="b17d7-148">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b17d7-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b17d7-149">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="b17d7-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b17d7-150">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="b17d7-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b17d7-151">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="b17d7-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

