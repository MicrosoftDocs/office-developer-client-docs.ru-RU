---
title: имессажемодифиреЦипиентс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 07e1c2104068a6eb242e8ba81f91655edaa92cd8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426242"
---
# <a name="imessagemodifyrecipients"></a><span data-ttu-id="255ae-103">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="255ae-103">IMessage::ModifyRecipients</span></span>

  
  
<span data-ttu-id="255ae-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="255ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="255ae-105">����������, �������� ��� �������� ����������� ���������.</span><span class="sxs-lookup"><span data-stu-id="255ae-105">Adds, deletes, or modifies message recipients.</span></span>
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a><span data-ttu-id="255ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="255ae-106">Parameters</span></span>

 <span data-ttu-id="255ae-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="255ae-107">_ulFlags_</span></span>
  
> <span data-ttu-id="255ae-p101">[in] ������� ����� �����, ������� ��������� ����������� ���������. ���� ��� ���������  _ulFlags_ ���������� ����, **ModifyRecipients** �������� ��� ������������ ����������� ������ �����������, �� ������� ��������� ��������  _lpMods_. ��������� ����� ����� ������ ���  _ulFlags_:</span><span class="sxs-lookup"><span data-stu-id="255ae-p101">[in] Bitmask of flags that controls the recipient changes. If zero is passed for the  _ulFlags_ parameter, **ModifyRecipients** replaces all existing recipients with the recipient list pointed to by the  _lpMods_ parameter. The following flags can be set for  _ulFlags_:</span></span>
    
<span data-ttu-id="255ae-111">MODRECIP_ADD</span><span class="sxs-lookup"><span data-stu-id="255ae-111">MODRECIP_ADD</span></span> 
  
> <span data-ttu-id="255ae-112">����������, �� ������� ��������� ��������  _lpMods_ ������� �������� � ������ �����������.</span><span class="sxs-lookup"><span data-stu-id="255ae-112">The recipients pointed to by the  _lpMods_ parameter should be added to the recipient list.</span></span> 
    
<span data-ttu-id="255ae-113">MODRECIP_MODIFY</span><span class="sxs-lookup"><span data-stu-id="255ae-113">MODRECIP_MODIFY</span></span> 
  
> <span data-ttu-id="255ae-p102">����������, �� ������� ��������� ��������  _lpMods_ ���������� �������� ������������ �����������. ��� ������������ �������� ���������� �������� �������� ��������������� ��������� [ADRENTRY](adrentry.md) .</span><span class="sxs-lookup"><span data-stu-id="255ae-p102">The recipients pointed to by the  _lpMods_ parameter should replace existing recipients. All of the existing properties are replaced by those in the corresponding [ADRENTRY](adrentry.md) structure.</span></span> 
    
<span data-ttu-id="255ae-116">MODRECIP_REMOVE</span><span class="sxs-lookup"><span data-stu-id="255ae-116">MODRECIP_REMOVE</span></span> 
  
> <span data-ttu-id="255ae-117">Существующие получатели следует удалить из списка получателей, используя в качестве индекса свойство **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)), включенное в массив значений свойств каждой записи получателя в параметре _лпмодс_ .</span><span class="sxs-lookup"><span data-stu-id="255ae-117">Existing recipients should be removed from the recipient list using as an index the **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md)) property included in the property value array of each recipient entry in the  _lpMods_ parameter.</span></span> 
    
 <span data-ttu-id="255ae-118">_лпмодс_</span><span class="sxs-lookup"><span data-stu-id="255ae-118">_lpMods_</span></span>
  
> <span data-ttu-id="255ae-119">[in] ��������� �� ��������� [ADRLIST](adrlist.md) , ������� �������� ������ �����������, ����� ���� ���������, ������� ��� �������� � ���������.</span><span class="sxs-lookup"><span data-stu-id="255ae-119">[in] Pointer to an [ADRLIST](adrlist.md) structure that contains a list of recipients to be added, deleted, or modified in the message.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="255ae-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="255ae-120">Return value</span></span>

<span data-ttu-id="255ae-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="255ae-121">S_OK</span></span> 
  
> <span data-ttu-id="255ae-122">��������� ������ ����������� ��������� �������.</span><span class="sxs-lookup"><span data-stu-id="255ae-122">The recipient list was successfully modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="255ae-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="255ae-123">Remarks</span></span>

<span data-ttu-id="255ae-p103">����� **IMessage::ModifyRecipients** �������� ������ ����������� ���������. ��� �� ����� ������, ������� ���������� � ��������� [ADRLIST](adrlist.md) , ��� ����������� ����������.</span><span class="sxs-lookup"><span data-stu-id="255ae-p103">The **IMessage::ModifyRecipients** method changes the message's recipient list. It is from this list, held in an [ADRLIST](adrlist.md) structure, that the recipient table is built.</span></span> 
  
<span data-ttu-id="255ae-126">��������� **ADRLIST** �������� ���� ��������� [ADRENTRY](adrentry.md) ��� ������� ����������, � ������ **ADRENTRY** ��������� �������� ������ �������� �������, ����������� ���������� ����������.</span><span class="sxs-lookup"><span data-stu-id="255ae-126">The **ADRLIST** structure contains one [ADRENTRY](adrentry.md) structure for each recipient and each **ADRENTRY** structure contains an array of property values describing the recipient properties.</span></span> 
  
<span data-ttu-id="255ae-127">������ ����������� � ��������� **ADRLIST** ����� ��������� ��� ���������.</span><span class="sxs-lookup"><span data-stu-id="255ae-127">Recipients in the **ADRLIST** structure can be resolved or unresolved.</span></span> <span data-ttu-id="255ae-128">������� ����������� � ����� � ���� ��������, ������� ��������.</span><span class="sxs-lookup"><span data-stu-id="255ae-128">The difference is in the number and type of properties that are included.</span></span> <span data-ttu-id="255ae-129">Нераспознанный получатель содержит только **свойства PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) **и PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)), в то время как разрешенный получатель содержит эти два свойства плюс **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) и **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="255ae-129">An unresolved recipient contains only the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) properties while a resolved recipient contains those two properties plus **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) and **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).</span></span> <span data-ttu-id="255ae-130">Если доступен **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), он также может быть включен.</span><span class="sxs-lookup"><span data-stu-id="255ae-130">If **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) is available, it can be included also.</span></span>
  
<span data-ttu-id="255ae-p105">����� �������� ��������� ��� ���������� �������� ������ ����������� ���������� ����������� � ��� ������ �����������. ���������� ����������� ������� ����� � ���������� ��� ������ � ��������� ��������� ����������� ���������. �������������� �������� � �������� ���������� ���� � ����� ������ ������� [������������� ����](resolving-a-recipient-name.md)��. ��� ��������� �������������� �������� � ����� ������ ������� � �������� ����� ������ [���������� ���������� ����](implementing-name-resolution.md).</span><span class="sxs-lookup"><span data-stu-id="255ae-p105">By the time a message is submitted, it must include only resolved recipients in its recipient list. Unresolved recipients cause nondelivery reports to be created and sent to the original sender of the message. For more information about the name resolution process from the client perspective, see [Resolving a Name](resolving-a-recipient-name.md). For more information from the perspective of the address book provider, see [Implementing Name Resolution](implementing-name-resolution.md).</span></span>
  
<span data-ttu-id="255ae-p106">� ���������� � ����������� ���������� � ���������� ����������� ���������� ����� ���� NULL. ���� **cValues** ��������� **ADRENTRY** ��� ���������� ������������� ������� �������� � ���� **rgPropVals** ����� �������� NULL.</span><span class="sxs-lookup"><span data-stu-id="255ae-p106">In addition to resolved and unresolved recipients, a recipient can be NULL. The **cValues** member of the **ADRENTRY** structure for the recipient is set to zero and the **rgPropVals** member is set to NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="255ae-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="255ae-137">Notes to callers</span></span>

<span data-ttu-id="255ae-p107">����� ������� ������ �����������, ������ [IAddrBook::Address](imapisupport-address.md) ��� ����������� ����������� ���������� ����� � ���������� ������������ ������� ��������. ������ �������, ��������� ��������  _lppAdrList_ ��� **Address** ����� ���� ������� **ModifyRecipients** ��� ��������  _lpMods_.</span><span class="sxs-lookup"><span data-stu-id="255ae-p107">You can create a recipient list by calling [IAddrBook::Address](imapisupport-address.md) to display the common dialog box and prompt the user to select entries. The address list pointed to by the  _lppAdrList_ parameter to **Address** can be passed to **ModifyRecipients** as the  _lpMods_ parameter.</span></span> 
  
<span data-ttu-id="255ae-p108">��� �������� �������� ��� ���������� � ��������� [ADRLIST](adrlist.md) �������� ��� �������� ����������, �� ������ �� ��� ����� ��� ����������. ��� ��������� ����������, ��������� ��� ��������, �� ���������� � ��������� **ADRLIST**. ��� ��������� �������� ������ ������� ��� ���� ����������� ���������, �������� [GetRecipientTable](imessage-getrecipienttable.md) � �������� ��� ������. ��������� � ��������� ��������� **ADRLIST** **SRowSet**, �� ����� ������������ �����������.</span><span class="sxs-lookup"><span data-stu-id="255ae-p108">When you specify properties for a recipient in the [ADRLIST](adrlist.md) structure, include all of the recipient's properties, not only the new or changed ones. When a recipient is modified, any properties not included in the **ADRLIST** structure are deleted. To retrieve the current set of properties for all of a message's recipients, call [GetRecipientTable](imessage-getrecipienttable.md) and retrieve all of the rows. Because an **SRowSet** is identical in structure to an **ADRLIST**, you can use them interchangeably.</span></span>
  
 <span data-ttu-id="255ae-144">**ModifyRecipients** �������� ��� ������ � ������� ������ ����������� ��������, �� ������� ���������  _lpMods_ ���� �� ���� �� ������ �������� � ������� ���������  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="255ae-144">**ModifyRecipients** replaces all of the entries in the current recipient list with the information pointed to by  _lpMods_ when none of the flags are set in the  _ulFlags_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="255ae-145">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="255ae-145">Notes to callers</span></span>

<span data-ttu-id="255ae-p109">��� ��������� ����� MODRECIP_MODIFY **ModifyRecipients** �������� ������� ���������� ������ ����� � ��������� [ADRLIST](adrlist.md) ���������� �  _lpMods_. ������� �� ��� ������� ��� ��������, ������� ������ ����� ���������� ���������� �� ����, �������� �� ��� ���� �������� ��� �������������� ���������� ��������.</span><span class="sxs-lookup"><span data-stu-id="255ae-p109">When you set the MODRECIP_MODIFY flag, **ModifyRecipients** replaces each entire recipient row with the associated row in the [ADRLIST](adrlist.md) structure passed in  _lpMods_. Be careful to specify all of the properties that a recipient should have regardless of whether they have changed to prevent them from being unintentionally deleted.</span></span>
  
<span data-ttu-id="255ae-148">���� ����������� ��������� ������� ��� ��������� ������� ����������� � ��������� **ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="255ae-148">Following are some rules for setting the properties of the recipients in the **ADRLIST** structure:</span></span> 
  
- <span data-ttu-id="255ae-p110">�� ����������� PT_NULL � �������� ���� ��������. **ModifyRecipients** ���������� ������ ��� ����������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="255ae-p110">Do not use PT_NULL as a property type. **ModifyRecipients** returns an error when encountering this value.</span></span> 
    
- <span data-ttu-id="255ae-p111">�� ����������� PT_ERROR � �������� ���� ��������. **ModifyRecipients** ���������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="255ae-p111">Do not use PT_ERROR as a property type. **ModifyRecipients** ignores this value.</span></span> 
    
- <span data-ttu-id="255ae-153">�������� �������� **PR_ROWID** ��� ���� �����������, ��������� ����� MODRECIP_REMOVE ��� MODRECIP_MODIFY �  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="255ae-153">Include the **PR_ROWID** property for all recipients when you set either the MODRECIP_REMOVE or MODRECIP_MODIFY flag in  _ulFlags_.</span></span> 
    
- <span data-ttu-id="255ae-154">�� ��������� �������� **PR_ROWID** ��� �����-���� �� ����������� �� ����� ���� MODRECIP_ADD �  _ulFlags_ ��� ��� �������� ���� �  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="255ae-154">Do not include the **PR_ROWID** property for any of the recipients when you set the MODRECIP_ADD flag in  _ulFlags_ or when you pass zero in  _ulFlags_.</span></span>
    
<span data-ttu-id="255ae-p112">���� �������� �������� **PR_ADDRTYPE** ��� �������� **PR_EMAIL_ADDRESS** ��� ����������, � ������ ��� ��� ��� ��������, �� ������������� ��� ������ � ����� ����������, ��� ���������� � **PR_ENTRYID**, ���������� �� ����������. �� ���� ���������� ��� ��������, � ����������� �� ���������� �����.</span><span class="sxs-lookup"><span data-stu-id="255ae-p112">If you include either the **PR_ADDRTYPE** property or **PR_EMAIL_ADDRESS** property for a recipient and one or both of these properties are inconsistent with the address type and address of the recipient as identified by **PR_ENTRYID**, the results are undefined. That is, there are three possibilities, depending on the service provider:</span></span>
  
- <span data-ttu-id="255ae-157">��������� ������������ �� �����, ������������ �������� **PR_ADDRTYPE** � **PR_EMAIL_ADDRESS**.</span><span class="sxs-lookup"><span data-stu-id="255ae-157">The message will be delivered to the address described by the **PR_ADDRTYPE** and **PR_EMAIL_ADDRESS** properties.</span></span> 
    
- <span data-ttu-id="255ae-158">��������� ����� ���������� ����������, ������������ ��������� **PR_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="255ae-158">The message will be delivered to the recipient identified by **PR_ENTRYID**.</span></span>
    
- <span data-ttu-id="255ae-159">��������� ����� ��������� �������������� ��-�� ���������������� �������� �� ������.</span><span class="sxs-lookup"><span data-stu-id="255ae-159">The message will be declared undeliverable due to the ambiguity of the address information.</span></span>
    
<span data-ttu-id="255ae-p113">������������� ������� �������������, ��������� � [������ ADRLIST � SRowSet ��������](managing-memory-for-adrlist-and-srowset-structures.md) ��� ��������� ������ ��� ������ �����������. **ModifyRecipients** �� ����������� ��������� **ADRLIST** �� ����� -���� �� �� ��������� ���������. ��������� **ADRLIST** � ������� [SPropValue](spropvalue.md) ��������� ���������� �������� �������� � ������� ������� [MAPIAllocateBuffer](mapiallocatebuffer.md) ����� �������, ����� ���������� ������� �� �����������. ���� ����� ������� ��������������� ����� �� ����� ��� ������ **SPropValue** ���������, ��� ����� �������� ��������� **SPropValue** ��� ����� ���������� ����� ������� ������ � ������� [MAPIFreeBuffer](mapifreebuffer.md). �������� ��������� **SPropValue** ����� ����� ���������� � ������� **MAPIFreeBuffer**.</span><span class="sxs-lookup"><span data-stu-id="255ae-p113">Use the allocation rules outlined in [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md) to allocate memory for the recipient list. **ModifyRecipients** does not free the **ADRLIST** structure nor any of its substructures. The **ADRLIST** structure and each [SPropValue](spropvalue.md) structure must be separately allocated by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function such that each can be freed individually. If the method requires additional space for any **SPropValue** structure, it can replace the **SPropValue** structure with a new one that can later be freed using [MAPIFreeBuffer](mapifreebuffer.md). The original **SPropValue** structure should also be freed using **MAPIFreeBuffer**.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="255ae-165">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="255ae-165">MFCMAPI reference</span></span>

<span data-ttu-id="255ae-166">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="255ae-166">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="255ae-167">**Файл**</span><span class="sxs-lookup"><span data-stu-id="255ae-167">**File**</span></span>|<span data-ttu-id="255ae-168">**Функция**</span><span class="sxs-lookup"><span data-stu-id="255ae-168">**Function**</span></span>|<span data-ttu-id="255ae-169">**�����������**</span><span class="sxs-lookup"><span data-stu-id="255ae-169">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="255ae-170">Мапиабфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="255ae-170">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="255ae-171">аддреЦипиент</span><span class="sxs-lookup"><span data-stu-id="255ae-171">AddRecipient</span></span>  <br/> |<span data-ttu-id="255ae-172">Mfcmapi (en) ����� **IMessage::ModifyRecipients** ������������ ��� ���������� ����� ����������� �� ���������.</span><span class="sxs-lookup"><span data-stu-id="255ae-172">MFCMAPI uses the **IMessage::ModifyRecipients** method to add a new recipient to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="255ae-173">См. также</span><span class="sxs-lookup"><span data-stu-id="255ae-173">See also</span></span>



[<span data-ttu-id="255ae-174">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="255ae-174">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="255ae-175">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="255ae-175">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="255ae-176">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="255ae-176">IAddrBook::Address</span></span>](iaddrbook-address.md)
  
[<span data-ttu-id="255ae-177">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="255ae-177">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="255ae-178">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="255ae-178">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="255ae-179">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="255ae-179">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="255ae-180">SPropValue</span><span class="sxs-lookup"><span data-stu-id="255ae-180">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="255ae-181">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="255ae-181">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)


[<span data-ttu-id="255ae-182">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="255ae-182">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

