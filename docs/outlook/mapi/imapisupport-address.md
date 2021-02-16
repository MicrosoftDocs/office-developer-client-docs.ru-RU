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
ms.openlocfilehash: 7300c11d5835640fe308430c9bb08d40b397e47b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407321"
---
# <a name="imapisupportaddress"></a><span data-ttu-id="3656e-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="3656e-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="3656e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3656e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3656e-105">Отображает диалоговое окно общего адреса.</span><span class="sxs-lookup"><span data-stu-id="3656e-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="3656e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3656e-106">Parameters</span></span>

 <span data-ttu-id="3656e-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3656e-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="3656e-108">[in, out] Указатель на ладку родительского окна диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="3656e-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="3656e-109">При вводе всегда должен передаваться окне окне.</span><span class="sxs-lookup"><span data-stu-id="3656e-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="3656e-110">Если флаг DIALOG_SDI установлен в структуре [ADRPARM,](adrparm.md) на который указывает параметр  _lpAdrParms,_ возвращается окне окне в диалоговом окне без режима.</span><span class="sxs-lookup"><span data-stu-id="3656e-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="3656e-111">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="3656e-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="3656e-112">[in, out] Указатель на **структуру ADRPARM,** которая управляет представлением и поведением диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="3656e-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="3656e-113">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="3656e-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="3656e-114">[in, out] Указатель на указатель на список адресов.</span><span class="sxs-lookup"><span data-stu-id="3656e-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="3656e-115">При вводе этот список является текущим списком получателей в сообщении или NULL, если такого списка нет.</span><span class="sxs-lookup"><span data-stu-id="3656e-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="3656e-116">При выходе  _lppAdrList_ указывает на обновленный список получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="3656e-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3656e-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3656e-117">Return value</span></span>

<span data-ttu-id="3656e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3656e-118">S_OK</span></span> 
  
> <span data-ttu-id="3656e-119">Диалоговое окно адреса успешно отобразилось.</span><span class="sxs-lookup"><span data-stu-id="3656e-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3656e-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="3656e-120">Remarks</span></span>

<span data-ttu-id="3656e-121">Метод **IMAPISupport::Address** реализован для объектов поддержки поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3656e-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="3656e-122">Поставщики адресных книг **звонят** по адресу, чтобы создать или обновить список получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="3656e-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="3656e-123">Каждый получатель описывается в структуре [ADRENTRY,](adrentry.md) включенной в структуру [ADRLIST,](adrlist.md) на которую указывает параметр _lppAdrList._</span><span class="sxs-lookup"><span data-stu-id="3656e-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="3656e-124">Структура **ADRENTRY** содержит массив значений свойств получателя, одно из которых является типом получателя или **свойством PR_RECIPIENT_TYPE** ([PidTagRecipientType).](pidtagrecipienttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3656e-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="3656e-125">Эта **структура ADRLIST** может быть передана клиенту для использования в качестве параметра  _lpMods_ в вызове [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span><span class="sxs-lookup"><span data-stu-id="3656e-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="3656e-126">Каждый получатель в структуре **ADRLIST** может быть разрешен, что означает, что одно из его значений свойства — это его **свойство PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)или не разрешено, что указывает на то, что свойство **PR_ENTRYID** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="3656e-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="3656e-127">Помимо **PR_ENTRYID,** разрешенные получатели включают следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="3656e-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="3656e-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="3656e-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="3656e-129">**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3656e-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="3656e-130">**PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3656e-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="3656e-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="3656e-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="3656e-132">Как правило, не разрешенные получатели включают **только** PR_DISPLAY_NAME и **PR_RECIPIENT_TYPE.**</span><span class="sxs-lookup"><span data-stu-id="3656e-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3656e-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3656e-133">Notes to callers</span></span>

<span data-ttu-id="3656e-134">Структура **ADRLIST,** в которую передается звоняя, может быть отличается от структуры, возвращаемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="3656e-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="3656e-135">При выделении памяти для **структуры ADRLIST** выделяете память для каждой [структуры SPropValue](spropvalue.md) отдельно.</span><span class="sxs-lookup"><span data-stu-id="3656e-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="3656e-136">Используйте указатели на функции выделения памяти MAPI, переданные функции [ABProviderInit](abproviderinit.md) для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="3656e-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="3656e-137">Выделите память с помощью функции [MAPIAllocateBuffer](mapiallocatebuffer.md) для **ADRLIST** и каждой структуры значений свойств в структурах **ADRENTRY** **в ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="3656e-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="3656e-138">Если **адрес** должен возвращать более крупную структуру **ADRLIST** или если вы передали NULL для _lppAdrList,_ address освободит исходную структуру и выделит новую. </span><span class="sxs-lookup"><span data-stu-id="3656e-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="3656e-139">**Адрес** также выделяет дополнительные структуры значений свойств в структуре **ADRLIST** и при необходимости освободит старые.</span><span class="sxs-lookup"><span data-stu-id="3656e-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="3656e-140">Дополнительные сведения об управлении памятью для структур **ADRLIST** см. в под управлением памятью [для ADRLIST и структур SRowSet.](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="3656e-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="3656e-141">**Адрес** немедленно возвращается, DIALOG_SDI флага, установленного в структуре **ADRPARM** в параметре _lpAdrParms._</span><span class="sxs-lookup"><span data-stu-id="3656e-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3656e-142">См. также</span><span class="sxs-lookup"><span data-stu-id="3656e-142">See also</span></span>



[<span data-ttu-id="3656e-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="3656e-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="3656e-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="3656e-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="3656e-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="3656e-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="3656e-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="3656e-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="3656e-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="3656e-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="3656e-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="3656e-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="3656e-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="3656e-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="3656e-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="3656e-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="3656e-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="3656e-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="3656e-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3656e-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3656e-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="3656e-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="3656e-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3656e-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3656e-155">Каноническое свойство PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="3656e-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="3656e-156">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="3656e-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="3656e-157">Каноническое свойство PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="3656e-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="3656e-158">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="3656e-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="3656e-159">Каноническое свойство PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="3656e-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="3656e-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3656e-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="3656e-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="3656e-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="3656e-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3656e-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="3656e-163">Управление памятью для структур ADRLIST и SRowSet</span><span class="sxs-lookup"><span data-stu-id="3656e-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

