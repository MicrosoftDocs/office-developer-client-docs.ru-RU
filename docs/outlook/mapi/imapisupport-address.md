---
title: имаписуппортаддресс
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
# <a name="imapisupportaddress"></a><span data-ttu-id="3e2e6-103">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="3e2e6-103">IMAPISupport::Address</span></span>

  
  
<span data-ttu-id="3e2e6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e2e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e2e6-105">Отображает диалоговое окно "общий адрес".</span><span class="sxs-lookup"><span data-stu-id="3e2e6-105">Displays the common address dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="3e2e6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e2e6-106">Parameters</span></span>

 <span data-ttu-id="3e2e6-107">_лпулуипарам_</span><span class="sxs-lookup"><span data-stu-id="3e2e6-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="3e2e6-108">[вход, выход] Указатель на дескриптор родительского окна диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-108">[in, out] A pointer to the handle of the parent window of the dialog box.</span></span> <span data-ttu-id="3e2e6-109">Во входных данных дескриптор окна всегда должен быть передан.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="3e2e6-110">В выходных данных, если флаг DIALOG_SDI задается в структуре [адрпарм](adrparm.md) , на которую указывает параметр _лпадрпармс_ , возвращается дескриптор окна немодального диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-110">On output, if the DIALOG_SDI flag is set in the [ADRPARM](adrparm.md) structure pointed to by the  _lpAdrParms_ parameter, the window handle of the modeless dialog box is returned.</span></span> 
    
 <span data-ttu-id="3e2e6-111">_лпадрпармс_</span><span class="sxs-lookup"><span data-stu-id="3e2e6-111">_lpAdrParms_</span></span>
  
> <span data-ttu-id="3e2e6-112">[вход, выход] Указатель на структуру **адрпарм** , которая управляет представлением и поведением диалогового окна "адрес".</span><span class="sxs-lookup"><span data-stu-id="3e2e6-112">[in, out] A pointer to an **ADRPARM** structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="3e2e6-113">_лппадрлист_</span><span class="sxs-lookup"><span data-stu-id="3e2e6-113">_lppAdrList_</span></span>
  
> <span data-ttu-id="3e2e6-114">[вход, выход] Указатель на указатель на список адресов.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-114">[in, out] A pointer to a pointer to an address list.</span></span> <span data-ttu-id="3e2e6-115">При вводе этот список является либо текущим списком получателей в сообщении, либо значением NULL, если такого списка не существует.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-115">On input, this list is either the current list of recipients in a message or NULL, if no such list exists.</span></span> <span data-ttu-id="3e2e6-116">В выходных данных _лппадрлист_ указывает на обновленный список получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-116">On output,  _lppAdrList_ points to an updated list of message recipients.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3e2e6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e2e6-117">Return value</span></span>

<span data-ttu-id="3e2e6-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e2e6-118">S_OK</span></span> 
  
> <span data-ttu-id="3e2e6-119">Диалоговое окно "адрес" успешно отображено.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-119">The address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3e2e6-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e2e6-120">Remarks</span></span>

<span data-ttu-id="3e2e6-121">Метод **имаписуппорт:: Address** реализован для объектов поддержки поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-121">The **IMAPISupport::Address** method is implemented for address book provider support objects.</span></span> <span data-ttu-id="3e2e6-122">Поставщик адресных книг **адрес** вызова для создания или обновления списка получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-122">Address book providers call **Address** to create or update a list of message recipients.</span></span> 
  
<span data-ttu-id="3e2e6-123">Каждый получатель описан в структуре [адрентри](adrentry.md) , которая включается в структуру [ADRLIST](adrlist.md) , на которую указывает параметр _лппадрлист_ .</span><span class="sxs-lookup"><span data-stu-id="3e2e6-123">Each recipient is described in an [ADRENTRY](adrentry.md) structure that is included in the [ADRLIST](adrlist.md) structure pointed to by the  _lppAdrList_ parameter.</span></span> <span data-ttu-id="3e2e6-124">Структура **адрентри** содержит массив значений свойств Recipient, один из которых является типом получателя или свойство **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3e2e6-124">The **ADRENTRY** structure contains an array of recipient property values, one of which is the recipient's type, or **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property.</span></span> <span data-ttu-id="3e2e6-125">Эту структуру **ADRLIST** можно передать клиенту, чтобы использовать в качестве параметра _лпмодс_ в вызове [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md).</span><span class="sxs-lookup"><span data-stu-id="3e2e6-125">This **ADRLIST** structure can be passed to a client to use as the  _lpMods_ parameter in a call to [IMessage::ModifyRecipients](imessage-modifyrecipients.md).</span></span>
  
<span data-ttu-id="3e2e6-126">Каждый получатель в структуре **ADRLIST** может быть разрешаемым, что указывает на то, что одно из значений свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) или не определено, что указывает на отсутствие свойства **PR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="3e2e6-126">Each recipient in the **ADRLIST** structure can be either resolved, which indicates that one of its property values is its **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="3e2e6-127">Кроме **PR_ENTRYID**, разрешенные получатели включают следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="3e2e6-127">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="3e2e6-128">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="3e2e6-128">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="3e2e6-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e2e6-129">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="3e2e6-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e2e6-130">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="3e2e6-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3e2e6-131">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="3e2e6-132">Как правило, нераспознанным получателям относятся только **PR_DISPLAY_NAME** и **PR_RECIPIENT_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-132">Unresolved recipients typically include only **PR_DISPLAY_NAME** and **PR_RECIPIENT_TYPE**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3e2e6-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="3e2e6-133">Notes to callers</span></span>

<span data-ttu-id="3e2e6-134">Структура **ADRLIST** , которую передает вызывающий абонент, может иметь другой размер из структуры, которую возвращает MAPI.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="3e2e6-135">При выделении памяти для структуры **ADRLIST** выделяет память для каждой структуры [спропвалуе](spropvalue.md) отдельно.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-135">When you allocate memory for the **ADRLIST** structure, allocate the memory for each [SPropValue](spropvalue.md) structure separately.</span></span> 
  
<span data-ttu-id="3e2e6-136">Используйте указатели на функции выделения памяти MAPI, передаваемые функции [абпровидеринит](abproviderinit.md) для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-136">Use the pointers to the MAPI memory allocation functions passed in to your [ABProviderInit](abproviderinit.md) function to allocate memory.</span></span> <span data-ttu-id="3e2e6-137">Выделение памяти с помощью функции [мапиаллокатебуффер](mapiallocatebuffer.md) для **ADRLIST** и каждой структуры значений свойств в структурах **адрентри** в **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-137">Allocate memory with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function for **ADRLIST** and each property value structure in the **ADRENTRY** structures in **ADRLIST**.</span></span> 
  
<span data-ttu-id="3e2e6-138">Если **Address** должен возвращать более крупную структуру **ADRLIST** , или если для _лппадрлист_было передано значение null, то **Address** освобождает исходную структуру и выделяет новую.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-138">If **Address** must return a larger **ADRLIST** structure, or if you have passed NULL for  _lppAdrList_, **Address** frees the original structure and allocates a new one.</span></span> <span data-ttu-id="3e2e6-139">**Address** также выделяет дополнительные структуры значений свойств в структуре **ADRLIST** и освобождает старые, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="3e2e6-139">**Address** also allocates additional property value structures in the **ADRLIST** structure and frees old ones as appropriate.</span></span> <span data-ttu-id="3e2e6-140">Дополнительные сведения об управлении памятью для структур **ADRLIST** приведены в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="3e2e6-140">For more information about how memory is managed for **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span>
  
 <span data-ttu-id="3e2e6-141">**Адрес** немедленно возвращается, если установлен флаг DIALOG_SDI в структуре **адрпарм** в параметре _лпадрпармс_ .</span><span class="sxs-lookup"><span data-stu-id="3e2e6-141">**Address** returns immediately if the DIALOG_SDI flag was set in the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e2e6-142">См. также</span><span class="sxs-lookup"><span data-stu-id="3e2e6-142">See also</span></span>



[<span data-ttu-id="3e2e6-143">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="3e2e6-143">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="3e2e6-144">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="3e2e6-144">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="3e2e6-145">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="3e2e6-145">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="3e2e6-146">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="3e2e6-146">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="3e2e6-147">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="3e2e6-147">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="3e2e6-148">FreeProws</span><span class="sxs-lookup"><span data-stu-id="3e2e6-148">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="3e2e6-149">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="3e2e6-149">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)
  
[<span data-ttu-id="3e2e6-150">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="3e2e6-150">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="3e2e6-151">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="3e2e6-151">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="3e2e6-152">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3e2e6-152">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3e2e6-153">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="3e2e6-153">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="3e2e6-154">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3e2e6-154">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3e2e6-155">Каноническое свойство PidTagAddressType</span><span class="sxs-lookup"><span data-stu-id="3e2e6-155">PidTagAddressType Canonical Property</span></span>](pidtagaddresstype-canonical-property.md)
  
[<span data-ttu-id="3e2e6-156">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="3e2e6-156">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="3e2e6-157">Каноническое свойство PidTagDisplayType</span><span class="sxs-lookup"><span data-stu-id="3e2e6-157">PidTagDisplayType Canonical Property</span></span>](pidtagdisplaytype-canonical-property.md)
  
[<span data-ttu-id="3e2e6-158">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="3e2e6-158">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
  
[<span data-ttu-id="3e2e6-159">Каноническое свойство PidTagRecipientType</span><span class="sxs-lookup"><span data-stu-id="3e2e6-159">PidTagRecipientType Canonical Property</span></span>](pidtagrecipienttype-canonical-property.md)
  
[<span data-ttu-id="3e2e6-160">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3e2e6-160">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="3e2e6-161">SRowSet</span><span class="sxs-lookup"><span data-stu-id="3e2e6-161">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="3e2e6-162">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e2e6-162">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="3e2e6-163">Управление памятью для структур ADRLIST и SRowSet</span><span class="sxs-lookup"><span data-stu-id="3e2e6-163">Managing Memory for ADRLIST and SRowSet Structures</span></span>](managing-memory-for-adrlist-and-srowset-structures.md)

