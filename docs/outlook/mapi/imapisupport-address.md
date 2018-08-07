---
title: IMAPISupportAddress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Address
api_type:
- COM
ms.assetid: 8c22547e-ddf5-47f7-aed3-76e3854688df
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cb683178a8e258f571cbc3d05a3b030481905433
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809099"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="234bf-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="234bf-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="234bf-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="234bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="234bf-105">Отображает диалоговое окно Общие адреса.</span><span class="sxs-lookup"><span data-stu-id="234bf-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="234bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="234bf-106">Parameters</span></span>

 <span data-ttu-id="234bf-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="234bf-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="234bf-108">[in, out] Указатель на дескриптор окна родительского диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="234bf-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="234bf-109">На входе дескриптор окна всегда должен быть передан.</span><span class="sxs-lookup"><span data-stu-id="234bf-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="234bf-110">В выходных данных Если в структуре [ADRPARM](adrparm.md) , на который указывает параметр _lpAdrParms_ установлен флаг DIALOG_SDI возвращается дескриптор окна безрежимным диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="234bf-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="234bf-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="234bf-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="234bf-112">[in, out] Указатель на структуру **ADRPARM** , определяющее представление и поведение диалоговое окно "адрес".</span><span class="sxs-lookup"><span data-stu-id="234bf-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="234bf-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="234bf-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="234bf-114">[in, out] Указатель на указатель на список адресов.</span><span class="sxs-lookup"><span data-stu-id="234bf-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="234bf-115">Для ввода данных этот список является либо текущий список получателей в сообщении или значение NULL, если список не существует.</span><span class="sxs-lookup"><span data-stu-id="234bf-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="234bf-116">На выходе _lppAdrList_ указывает на обновленный список получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="234bf-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="234bf-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7">Return value</span></span>

<span data-ttu-id="234bf-118">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="234bf-118">S_OK</span></span> 
  
> <span data-ttu-id="234bf-119">Диалоговое окно "адрес" успешно отображается.</span><span class="sxs-lookup"><span data-stu-id="234bf-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="234bf-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="234bf-120">Remarks</span></span>

<span data-ttu-id="234bf-121">Метод **IMAPISupport::Address** реализуется для объектов поддержки поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="234bf-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="234bf-122">Поставщиками адресной книги вызовите **адрес** , который необходимо создать или обновить список получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="234bf-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="234bf-123">Каждого получателя, описанного в структуре [ADRENTRY](adrentry.md) , включенную в структуре [ADRLIST](adrlist.md) указывает параметр _lppAdrList_ .</span><span class="sxs-lookup"><span data-stu-id="234bf-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="234bf-124">Структура **ADRENTRY** содержит массив значений свойства получателей, один из которых является тип получателя или свойство **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="234bf-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="234bf-125">Эта структура **ADRLIST** может быть передан клиента для использования в качестве параметра _lpMods_ в вызове [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span><span class="sxs-lookup"><span data-stu-id="234bf-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="234bf-126">Каждого получателя в структуре **ADRLIST** может быть либо разрешен, это означает, что одно из значений его свойств, его свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), или разрешены, указывает, что свойство **PR_ENTRYID** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="234bf-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="234bf-127">В дополнение к **PR_ENTRYID**разрешить получателей относятся следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="234bf-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="234bf-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="234bf-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="234bf-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="234bf-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="234bf-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="234bf-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="234bf-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="234bf-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="234bf-132">Нерешенные получателей относятся только **PR_DISPLAY_NAME** и **PR_RECIPIENT_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="234bf-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="234bf-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="234bf-133">Notes to callers</span></span>

<span data-ttu-id="234bf-134">Структура **ADRLIST** , вызывающий объект передает в может быть другой размер структуры, которые возвращает MAPI.</span><span class="sxs-lookup"><span data-stu-id="234bf-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="234bf-135">После выделения памяти для структуры **ADRLIST** выделите память для каждой структуры [SPropValue](spropvalue.md) отдельно.</span><span class="sxs-lookup"><span data-stu-id="234bf-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="234bf-136">Используйте указатели на функции выделения памяти MAPI, переданных в функции [ABProviderInit](abproviderinit.md) для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="234bf-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="234bf-137">Выделите память с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) для **ADRLIST** и структуры значение каждого свойства в структур **ADRENTRY** в **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="234bf-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="234bf-138">Если **адрес** должен вернуть увеличенное структуру **ADRLIST** или переданное значение NULL для _lppAdrList_, **адрес** освобождает исходной структуры и выделяет новый.</span><span class="sxs-lookup"><span data-stu-id="234bf-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="234bf-139">**Адрес** также выделяет структур значение дополнительные свойства в структуре **ADRLIST** и освобождает старых соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="234bf-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="234bf-140">Дополнительные сведения об управлении памяти **ADRLIST** структуры можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="234bf-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="234bf-141">**Адрес** возвращает немедленно, если был установлен флажок DIALOG_SDI в структуре **ADRPARM** в параметре _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="234bf-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="234bf-142">См. также</span><span class="sxs-lookup"><span data-stu-id="234bf-142">See also</span></span>



[<span data-ttu-id="234bf-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="234bf-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="234bf-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="234bf-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="234bf-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="234bf-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="234bf-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="234bf-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="234bf-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="234bf-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="234bf-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="234bf-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="234bf-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="234bf-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="234bf-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="234bf-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="234bf-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="234bf-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="234bf-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="234bf-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="234bf-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="234bf-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="234bf-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="234bf-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="234bf-155">Каноническое свойство PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="234bf-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="234bf-156">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="234bf-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="234bf-157">Каноническое свойство PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="234bf-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="234bf-158">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="234bf-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="234bf-159">Каноническое свойство PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="234bf-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="234bf-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="234bf-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="234bf-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="234bf-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="234bf-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="234bf-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="234bf-163">Управление памятью для структур ADRLIST и SRowSet</span><span class="sxs-lookup"><span data-stu-id="234bf-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

