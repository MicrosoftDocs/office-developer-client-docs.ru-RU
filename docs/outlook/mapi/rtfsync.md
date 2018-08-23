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
ms.openlocfilehash: 706c628241e519642209a271dce62d21b16938e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565741"
---
# <a name="rtfsync"></a><span data-ttu-id="9681b-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="9681b-103">RTFSync</span></span>

<span data-ttu-id="9681b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9681b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9681b-105">Следит за тем, что текста сообщения форматированный текст (RTF) соответствует версии обычного текста.</span><span class="sxs-lookup"><span data-stu-id="9681b-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="9681b-106">Это необходимо для вызова этой функции перед чтением версии RTF и после изменения версии RTF.</span><span class="sxs-lookup"><span data-stu-id="9681b-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9681b-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9681b-107">Header file:</span></span>  <br/> |<span data-ttu-id="9681b-108">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9681b-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9681b-109">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="9681b-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="9681b-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="9681b-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="9681b-111">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="9681b-111">Called by:</span></span>  <br/> |<span data-ttu-id="9681b-112">Поставщики удаленного хранилища принять во внимание RTF клиентских приложений и сообщения</span><span class="sxs-lookup"><span data-stu-id="9681b-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="9681b-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="9681b-113">Parameters</span></span>

<span data-ttu-id="9681b-114">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="9681b-114">_lpMessage_</span></span>
  
> <span data-ttu-id="9681b-115">[in] Указатель на сообщение, который требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="9681b-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="9681b-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9681b-116">_ulFlags_</span></span>
  
> <span data-ttu-id="9681b-117">[in] Битовая маска флагов служит для указания RTF или текстовая версия сообщения, была изменена.</span><span class="sxs-lookup"><span data-stu-id="9681b-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="9681b-118">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="9681b-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="9681b-119">RTF_SYNC_BODY_CHANGED: Версия обычного текста сообщения, была изменена.</span><span class="sxs-lookup"><span data-stu-id="9681b-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="9681b-120">RTF_SYNC_RTF_CHANGED: Версия RTF сообщения, была изменена.</span><span class="sxs-lookup"><span data-stu-id="9681b-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="9681b-121">Все другие биты с помощью параметра _ulFlags_ зарезервированы для использования в будущем.</span><span class="sxs-lookup"><span data-stu-id="9681b-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="9681b-122">_lpfMessageUpdated_</span><span class="sxs-lookup"><span data-stu-id="9681b-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="9681b-123">[out] Указатель на переменную, указывающее, существует ли обновленные сообщения.</span><span class="sxs-lookup"><span data-stu-id="9681b-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="9681b-124">Значение TRUE, если сообщение обновленные значение FALSE в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9681b-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9681b-125">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="9681b-125">Return value</span></span>

<span data-ttu-id="9681b-126">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="9681b-126">S_OK</span></span> 
  
> <span data-ttu-id="9681b-127">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9681b-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9681b-128">���������</span><span class="sxs-lookup"><span data-stu-id="9681b-128">Remarks</span></span>

<span data-ttu-id="9681b-129">Если свойство **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) отсутствует или имеет значение FALSE, перед чтением свойства **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) функция **RTFSync** вызывается с RTF_SYNC_BODY_ ИЗМЕНЕН флаг.</span><span class="sxs-lookup"><span data-stu-id="9681b-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="9681b-130">Если флаг STORE_RTF_OK не установлен в свойстве **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), эта функция должна вызываться с флаг RTF_SYNC_RTF_CHANGED после изменения **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="9681b-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="9681b-131">При изменении **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) и **PR_RTF_COMPRESSED** **RTFSync** функция должна вызываться с оба набора флаги.</span><span class="sxs-lookup"><span data-stu-id="9681b-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="9681b-132">Если параметр _lpfMessageUpdated_ имеет значение TRUE, метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) должен быть вызван для сообщения.</span><span class="sxs-lookup"><span data-stu-id="9681b-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="9681b-133">Если **SaveChanges** не вызван, изменения не будут сохранены в сообщении.</span><span class="sxs-lookup"><span data-stu-id="9681b-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="9681b-134">Поставщики хранилища сообщений можно использовать **RTFSync** для хранения синхронизацию свойств **PR_BODY** и **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="9681b-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="9681b-135">Для получения дополнительных сведений см [Поддержка текст RTF для поставщиков хранилища сообщений](supporting-rtf-text-for-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="9681b-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9681b-136">См. также</span><span class="sxs-lookup"><span data-stu-id="9681b-136">See also</span></span>

- [<span data-ttu-id="9681b-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="9681b-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

