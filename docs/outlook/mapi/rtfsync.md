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
# <a name="rtfsync"></a><span data-ttu-id="7f40b-103">RTFSync</span><span class="sxs-lookup"><span data-stu-id="7f40b-103">RTFSync</span></span>

<span data-ttu-id="7f40b-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f40b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f40b-105">Убедитесь, что текст сообщения в формате RTF соответствует версии обычного текста.</span><span class="sxs-lookup"><span data-stu-id="7f40b-105">Makes sure that the Rich Text Format (RTF) message text matches the plain text version.</span></span> <span data-ttu-id="7f40b-106">Перед считыванием версии RTF и изменением версии RTF необходимо вызвать эту функцию.</span><span class="sxs-lookup"><span data-stu-id="7f40b-106">It is necessary to call this function before reading the RTF version and after modifying the RTF version.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f40b-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="7f40b-107">Header file:</span></span>  <br/> |<span data-ttu-id="7f40b-108">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="7f40b-108">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7f40b-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="7f40b-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="7f40b-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="7f40b-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="7f40b-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="7f40b-111">Called by:</span></span>  <br/> |<span data-ttu-id="7f40b-112">Клиентские приложения и поставщики хранилищ сообщений с поддержкой RTF</span><span class="sxs-lookup"><span data-stu-id="7f40b-112">RTF-aware client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT RTFSync(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  BOOL FAR * lpfMessageUpdated
);
```

## <a name="parameters"></a><span data-ttu-id="7f40b-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f40b-113">Parameters</span></span>

<span data-ttu-id="7f40b-114">_Лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="7f40b-114">_lpMessage_</span></span>
  
> <span data-ttu-id="7f40b-115">возврата Указатель на сообщение, которое требуется обновить.</span><span class="sxs-lookup"><span data-stu-id="7f40b-115">[in] Pointer to the message to be updated.</span></span>
    
<span data-ttu-id="7f40b-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7f40b-116">_ulFlags_</span></span>
  
> <span data-ttu-id="7f40b-117">возврата Битовая маска флагов, используемых для обозначения измененной версии сообщения в формате RTF или обычного текста.</span><span class="sxs-lookup"><span data-stu-id="7f40b-117">[in] Bitmask of flags used to indicate the RTF or plain text version of the message has changed.</span></span> <span data-ttu-id="7f40b-118">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="7f40b-118">The following flags can be set:</span></span>
    
  - <span data-ttu-id="7f40b-119">РТФ_СИНК_БОДИ_ЧАНЖЕД: версия сообщения с обычным текстом изменилась.</span><span class="sxs-lookup"><span data-stu-id="7f40b-119">RTF_SYNC_BODY_CHANGED: The plain text version of the message has changed.</span></span>
      
  - <span data-ttu-id="7f40b-120">РТФ_СИНК_РТФ_ЧАНЖЕД: изменена версия RTF сообщения.</span><span class="sxs-lookup"><span data-stu-id="7f40b-120">RTF_SYNC_RTF_CHANGED: The RTF version of the message has changed.</span></span>
    
  <span data-ttu-id="7f40b-121">Все остальные биты в параметре _ulFlags_ зарезервированы для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="7f40b-121">All other bits in the  _ulFlags_ parameter are reserved for future use.</span></span> 
    
<span data-ttu-id="7f40b-122">_Лпфмессажеупдатед_</span><span class="sxs-lookup"><span data-stu-id="7f40b-122">_lpfMessageUpdated_</span></span>
  
> <span data-ttu-id="7f40b-123">вышли Указатель на переменную, указывающую наличие обновленного сообщения.</span><span class="sxs-lookup"><span data-stu-id="7f40b-123">[out] Pointer to a variable indicating whether there is an updated message.</span></span> <span data-ttu-id="7f40b-124">ЗНАЧЕНИЕ TRUE, если имеется обновленное сообщение, в противном случае — FALSE.</span><span class="sxs-lookup"><span data-stu-id="7f40b-124">TRUE if there is an updated message, FALSE otherwise.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7f40b-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f40b-125">Return value</span></span>

<span data-ttu-id="7f40b-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f40b-126">S_OK</span></span> 
  
> <span data-ttu-id="7f40b-127">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7f40b-127">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f40b-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="7f40b-128">Remarks</span></span>

<span data-ttu-id="7f40b-129">Если свойство **пр_ртф_ин_синк** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) отсутствует или имеет значение false, перед чтением свойства **пр_ртф_компрессед** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) необходимо вызвать функцию **ртфсинк** с помощью параметра ртф_синк_боди_ ИЗМЕНЕНный набор флагов.</span><span class="sxs-lookup"><span data-stu-id="7f40b-129">If the **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) property is missing or is FALSE, before reading the **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property the **RTFSync** function should be called with the RTF_SYNC_BODY_CHANGED flag set.</span></span> 
  
<span data-ttu-id="7f40b-130">Если флаг СТОРЕ_РТФ_ОК не задан в свойстве **пр_сторе_суппорт_маск** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), эта функция должна вызыватьСЯ с флагом ртф_синк_ртф_чанжед, установленным после изменения \*\*пр_ртф_компрессед\*\*.</span><span class="sxs-lookup"><span data-stu-id="7f40b-130">If the STORE_RTF_OK flag is not set in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property, this function should be called with the RTF_SYNC_RTF_CHANGED flag set after modifying **PR_RTF_COMPRESSED**.</span></span> 
  
<span data-ttu-id="7f40b-131">Если были изменены оба **пр_боди** ([PidTagBody](pidtagbody-canonical-property.md)) и **пр_ртф_компрессед** , функция **ртфсинк** должна вызываться с установленными обоими флагами.</span><span class="sxs-lookup"><span data-stu-id="7f40b-131">If both **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) and **PR_RTF_COMPRESSED** have been changed, the **RTFSync** function should be called with both flags set.</span></span> 
  
<span data-ttu-id="7f40b-132">Если для параметра _лпфмессажеупдатед_ задано значение true, то для сообщения должен вызываться метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="7f40b-132">If the value of the  _lpfMessageUpdated_ parameter is set to TRUE, then the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method should be called for the message.</span></span> <span data-ttu-id="7f40b-133">Если параметр **SaveChanges** не вызывается, изменения не будут сохранены в сообщении.</span><span class="sxs-lookup"><span data-stu-id="7f40b-133">If **SaveChanges** is not called, the modifications will not be saved in the message.</span></span> 
  
<span data-ttu-id="7f40b-134">Поставщики хранилищ сообщений могут использовать **ртфсинк** для синхронизации свойств **пр_боди** и **пр_ртф_компрессед** .</span><span class="sxs-lookup"><span data-stu-id="7f40b-134">Message store providers can use **RTFSync** to keep the **PR_BODY** and **PR_RTF_COMPRESSED** properties synchronized.</span></span> 
  
<span data-ttu-id="7f40b-135">Дополнительную информацию можно узнать в статье [поддержка текста в формате RTF для поставщиков хранилищ сообщений](supporting-rtf-text-for-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="7f40b-135">For more information, see [Supporting RTF Text for Message Store Providers](supporting-rtf-text-for-message-store-providers.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f40b-136">См. также</span><span class="sxs-lookup"><span data-stu-id="7f40b-136">See also</span></span>

- [<span data-ttu-id="7f40b-137">WrapCompressedRTFStream</span><span class="sxs-lookup"><span data-stu-id="7f40b-137">WrapCompressedRTFStream</span></span>](wrapcompressedrtfstream.md)

