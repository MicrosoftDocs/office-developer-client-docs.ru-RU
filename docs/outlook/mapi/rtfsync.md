---
title: RTFSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RTFSync
api_type:
- HeaderDef
ms.assetid: 627f95e9-39ac-4d43-8f02-687783b09785
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dfdf1068caaab3894b1b489d53ccc8debe1b3a29
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436211"
---
# <a name="rtfsync"></a><span data-ttu-id="45062-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="45062-103">RTFSync</span></span>

<span data-ttu-id="45062-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45062-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45062-105">Убедитесь, что текст сообщения Rich Text Format (RTF) совпадает с обычной текстовой версией.</span><span class="sxs-lookup"><span data-stu-id="45062-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="45062-106">Необходимо вызвать эту функцию перед чтением версии RTF и после изменения версии RTF.</span><span class="sxs-lookup"><span data-stu-id="45062-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45062-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="45062-107">Header file:</span></span>  <br/> |<span data-ttu-id="45062-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="45062-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="45062-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="45062-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="45062-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="45062-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="45062-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="45062-111">Called by:</span></span>  <br/> |<span data-ttu-id="45062-112">Клиентские приложения и поставщики магазинов сообщений, осведомленные о RTF</span><span class="sxs-lookup"><span data-stu-id="45062-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="45062-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="45062-113">Parameters</span></span>

<span data-ttu-id="45062-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="45062-114">_lpMessage_</span></span>
  
> <span data-ttu-id="45062-115">[in] Указатель на обновленное сообщение.</span><span class="sxs-lookup"><span data-stu-id="45062-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="45062-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="45062-116">_ulFlags_</span></span>
  
> <span data-ttu-id="45062-117">[in] Изменена битмаска флагов, используемых для указать RTF или обычную текстовую версию сообщения.</span><span class="sxs-lookup"><span data-stu-id="45062-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="45062-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="45062-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="45062-119">RTF_SYNC_BODY_CHANGED: обычная текстовая версия сообщения изменилась.</span><span class="sxs-lookup"><span data-stu-id="45062-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="45062-120">RTF_SYNC_RTF_CHANGED. Версия сообщения RTF изменилась.</span><span class="sxs-lookup"><span data-stu-id="45062-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="45062-121">Все остальные биты в параметре  _ulFlags_ зарезервированы для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="45062-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="45062-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="45062-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="45062-123">[вышел] Указатель на переменную, указывающее, есть ли обновленное сообщение.</span><span class="sxs-lookup"><span data-stu-id="45062-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="45062-124">TRUE, если есть обновленное сообщение, FALSE в противном случае.</span><span class="sxs-lookup"><span data-stu-id="45062-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="45062-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="45062-125">Return value</span></span>

<span data-ttu-id="45062-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="45062-126">S_OK</span></span> 
  
> <span data-ttu-id="45062-127">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="45062-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45062-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="45062-128">Remarks</span></span>

<span data-ttu-id="45062-129">Если **свойство PR_RTF_IN_SYNC** [(PidTagRtfInSync)](pidtagrtfinsync-canonical-property.md)отсутствует или является FALSE, перед чтением свойства **PR_RTF_COMPRESSED** [(PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)функция **RTFSync** должна быть вызвана с набором флага RTF_SYNC_BODY_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="45062-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="45062-130">Если флаг STORE_RTF_OK не установлен в **свойстве PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask),](pidtagstoresupportmask-canonical-property.md)эта функция должна быть вызвана с набором флага RTF_SYNC_RTF_CHANGED после изменения **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="45062-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="45062-131">Если **изменены PR_BODY** [(PidTagBody)](pidtagbody-canonical-property.md)и **PR_RTF_COMPRESSED,** функция **RTFSync** должна быть вызвана с набором флагов.</span><span class="sxs-lookup"><span data-stu-id="45062-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="45062-132">Если значение параметра _lpfMessageUpdated_ задано значение TRUE, для сообщения должен быть вызван метод [IMAPIProp::SaveChanges.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="45062-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="45062-133">Если **SaveChanges** не называется, изменения не будут сохранены в сообщении.</span><span class="sxs-lookup"><span data-stu-id="45062-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="45062-134">Поставщики магазинов сообщений могут использовать **RTFSync** для синхронизации свойств PR_BODY и **PR_RTF_COMPRESSED.** </span><span class="sxs-lookup"><span data-stu-id="45062-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="45062-135">Дополнительные сведения см. [в документе Поддержка текста RTF для поставщиков магазинов сообщений.](supporting-rtf-text-for-message-store-providers.md)</span><span class="sxs-lookup"><span data-stu-id="45062-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="45062-136">См. также</span><span class="sxs-lookup"><span data-stu-id="45062-136">See also</span></span>

- [<span data-ttu-id="45062-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="45062-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

