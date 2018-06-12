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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: ae09723c78fe4e333fb5c46e8c79da4b77c0b331
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812043"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a><span data-ttu-id="da6dc-103">Каноническое свойство PidTagValidFolderMask</span><span class="sxs-lookup"><span data-stu-id="da6dc-103">PidTagValidFolderMask Canonical Property</span></span>

  
  
<span data-ttu-id="da6dc-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="da6dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="da6dc-105">Содержит битовую маску флагов, указывающие на правильность идентификаторы записей папок в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="da6dc-105">Contains a bitmask of flags that indicate the validity of the entry identifiers of the folders in a message store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="da6dc-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="da6dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da6dc-107">PR_VALID_FOLDER_MASK</span><span class="sxs-lookup"><span data-stu-id="da6dc-107">PR_VALID_FOLDER_MASK</span></span>  <br/> |
|<span data-ttu-id="da6dc-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="da6dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="da6dc-109">0x35DF</span><span class="sxs-lookup"><span data-stu-id="da6dc-109">0x35DF</span></span>  <br/> |
|<span data-ttu-id="da6dc-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="da6dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="da6dc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="da6dc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="da6dc-112">Области:</span><span class="sxs-lookup"><span data-stu-id="da6dc-112">Area:</span></span>  <br/> |<span data-ttu-id="da6dc-113">Хранение сообщений MAPI</span><span class="sxs-lookup"><span data-stu-id="da6dc-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da6dc-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="da6dc-114">Remarks</span></span>

<span data-ttu-id="da6dc-115">Идентификатор записи папки могут стать недопустимыми, если пользователь удаляет папку или повреждения хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="da6dc-115">A folder's entry identifier can become invalid if a user deletes the folder or if the message store becomes corrupted.</span></span>
  
<span data-ttu-id="da6dc-116">Для Битовая маска, которая может быть установлено одно или несколько из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="da6dc-116">One or more of the following flags can be set for the bitmask:</span></span> 
  
<span data-ttu-id="da6dc-117">FOLDER_COMMON_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="da6dc-117">FOLDER_COMMON_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="da6dc-118">Общие папки "представления" имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="da6dc-118">The common views folder has a valid entry identifier.</span></span> <span data-ttu-id="da6dc-119">В разделе **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da6dc-119">See **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="da6dc-120">FOLDER_FINDER_VALID</span><span class="sxs-lookup"><span data-stu-id="da6dc-120">FOLDER_FINDER_VALID</span></span> 
  
> <span data-ttu-id="da6dc-121">Папки поиска с идентификатором записей.</span><span class="sxs-lookup"><span data-stu-id="da6dc-121">The finder folder has a valid entry identifier.</span></span> <span data-ttu-id="da6dc-122">В разделе **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da6dc-122">See **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="da6dc-123">FOLDER_IPM_INBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="da6dc-123">FOLDER_IPM_INBOX_VALID</span></span> 
  
> <span data-ttu-id="da6dc-124">Получать сообщения электронной почты — это (IPM) папки с идентификатором записей.</span><span class="sxs-lookup"><span data-stu-id="da6dc-124">The interpersonal message (IPM) receive folder has a valid entry identifier.</span></span> <span data-ttu-id="da6dc-125">В разделе [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span><span class="sxs-lookup"><span data-stu-id="da6dc-125">See [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md).</span></span> 
    
<span data-ttu-id="da6dc-126">FOLDER_IPM_OUTBOX_VALID</span><span class="sxs-lookup"><span data-stu-id="da6dc-126">FOLDER_IPM_OUTBOX_VALID</span></span> 
  
> <span data-ttu-id="da6dc-127">Папка исходящих IPM имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="da6dc-127">The IPM Outbox folder has a valid entry identifier.</span></span> <span data-ttu-id="da6dc-128">В разделе **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da6dc-128">See **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)).</span></span> 
    
<span data-ttu-id="da6dc-129">FOLDER_IPM_SENTMAIL_VALID</span><span class="sxs-lookup"><span data-stu-id="da6dc-129">FOLDER_IPM_SENTMAIL_VALID</span></span> 
  
> <span data-ttu-id="da6dc-130">Папка Отправленные IPM имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="da6dc-130">The IPM Sent Items folder has a valid entry identifier.</span></span> <span data-ttu-id="da6dc-131">В разделе **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da6dc-131">See **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="da6dc-132">FOLDER_IPM_SUBTREE_VALID</span><span class="sxs-lookup"><span data-stu-id="da6dc-132">FOLDER_IPM_SUBTREE_VALID</span></span> 
  
> <span data-ttu-id="da6dc-133">Папка поддерева IPM имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="da6dc-133">The IPM folder subtree has a valid entry identifier.</span></span> <span data-ttu-id="da6dc-134">В разделе **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da6dc-134">See **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="da6dc-135">FOLDER_IPM_WASTEBASKET_VALID</span><span class="sxs-lookup"><span data-stu-id="da6dc-135">FOLDER_IPM_WASTEBASKET_VALID</span></span> 
  
> <span data-ttu-id="da6dc-136">Папки "Удаленные IPM" имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="da6dc-136">The IPM Deleted Items folder has a valid entry identifier.</span></span> <span data-ttu-id="da6dc-137">В разделе **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da6dc-137">See **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).</span></span>
    
<span data-ttu-id="da6dc-138">FOLDER_VIEWS_VALID</span><span class="sxs-lookup"><span data-stu-id="da6dc-138">FOLDER_VIEWS_VALID</span></span> 
  
> <span data-ttu-id="da6dc-139">Папки "представления" имеет идентификатор записей.</span><span class="sxs-lookup"><span data-stu-id="da6dc-139">The views folder has a valid entry identifier.</span></span> <span data-ttu-id="da6dc-140">В разделе **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da6dc-140">See **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="da6dc-141">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="da6dc-141">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="da6dc-142">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="da6dc-142">Header files</span></span>

<span data-ttu-id="da6dc-143">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da6dc-143">Mapidefs.h</span></span>
  
> <span data-ttu-id="da6dc-144">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="da6dc-144">Provides data type definitions.</span></span>
    
<span data-ttu-id="da6dc-145">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="da6dc-145">Mapitags.h</span></span>
  
> <span data-ttu-id="da6dc-146">Содержит определения свойства в списке альтернативных имен.</span><span class="sxs-lookup"><span data-stu-id="da6dc-146">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da6dc-147">См. также</span><span class="sxs-lookup"><span data-stu-id="da6dc-147">See also</span></span>



[<span data-ttu-id="da6dc-148">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="da6dc-148">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da6dc-149">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="da6dc-149">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da6dc-150">Каноническое свойство имена сопоставляемых именам MAPI</span><span class="sxs-lookup"><span data-stu-id="da6dc-150">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da6dc-151">Сопоставление имен MAPI имена каноническое свойств</span><span class="sxs-lookup"><span data-stu-id="da6dc-151">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

