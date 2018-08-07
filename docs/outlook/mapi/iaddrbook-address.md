---
title: IAddrBookAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Address
api_type:
- COM
ms.assetid: ef2112c7-35cd-4106-ad18-a45e1dbe07d6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 10f8f2cf44bf1a8e00f8c2b1a76826db5fc07161
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808741"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="79b36-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="79b36-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="79b36-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79b36-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79b36-105">Отображает диалоговое окно Outlook адресной книги.</span><span class="sxs-lookup"><span data-stu-id="79b36-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="79b36-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="79b36-106">Parameters</span></span>

 <span data-ttu-id="79b36-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="79b36-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="79b36-108">[in, out] Указатель на маркер родительского окна диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="79b36-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="79b36-109">На входе дескриптор окна всегда должен быть передан.</span><span class="sxs-lookup"><span data-stu-id="79b36-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="79b36-110">На выходных данных Если член **ulFlags** для параметра _lpAdrParms_ установлено значение DIALOG_SDI, возвращаемый дескриптор окна безрежимным диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="79b36-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="79b36-111">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="79b36-111">See Remarks.</span></span> 
    
 <span data-ttu-id="79b36-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="79b36-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="79b36-113">[in, out] Указатель на структуру [ADRPARM](adrparm.md) , определяющее представление и поведение диалоговое окно "адрес".</span><span class="sxs-lookup"><span data-stu-id="79b36-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="79b36-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="79b36-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="79b36-115">[in, out] Указатель на указатель на структуру [ADRLIST](adrlist.md) , содержащий сведения о получателях.</span><span class="sxs-lookup"><span data-stu-id="79b36-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="79b36-116">На входные данные этот параметр может быть NULL или укажите допустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="79b36-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="79b36-117">В выходных данных этот параметр указывает указатель на допустимый адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="79b36-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="79b36-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="79b36-119">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="79b36-119">S_OK</span></span> 
  
> <span data-ttu-id="79b36-120">Стандартным диалоговым окном адрес успешно отображается.</span><span class="sxs-lookup"><span data-stu-id="79b36-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79b36-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="79b36-121">Remarks</span></span>

<span data-ttu-id="79b36-122">Если элемент **ulFlags** параметр _lpAdrParms_ имеет значение DIALOG_SDI предупреждение return дескриптор окна безрежимным диалогового окна на выходных данных, он обрабатывается в Outlook; в отличные от Outlook всегда отображается версия модального диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="79b36-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="79b36-123">Структура **ADRLIST** , передается обратно по MAPI вызывающему через параметр _lppAdrList_ содержит массив структур [ADRENTRY](adrentry.md) одной структуры для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="79b36-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="79b36-124">При передаче методу [IMessage::ModifyRecipients](imessage-modifyrecipients.md) исходящих сообщений с помощью параметра _lpMods_ структура **ADRLIST** можно использовать для обновление получателей списка.</span><span class="sxs-lookup"><span data-stu-id="79b36-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="79b36-125">Структура каждого **ADRENTRY** в структуре **ADRLIST** содержит ноль или больше [SPropValue](spropvalue.md) структуры, структуры один для каждого свойства для получателя.</span><span class="sxs-lookup"><span data-stu-id="79b36-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="79b36-126">При окно доклад **адрес** метод используется для удаления получателя может быть ноль **SPropValue** структуры.</span><span class="sxs-lookup"><span data-stu-id="79b36-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="79b36-127">При наличии одного или нескольких структур **SPropValue** , соответствующий структура **ADRENTRY** используется для добавления или обновления получателя.</span><span class="sxs-lookup"><span data-stu-id="79b36-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="79b36-128">Получатель может быть разрешен, это означает, что один из структур **SPropValue** описывает свойства получателя **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) или разрешены, указывает, что свойство **PR_ENTRYID** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="79b36-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="79b36-129">В дополнение к **PR_ENTRYID**разрешить получателей относятся следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="79b36-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="79b36-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="79b36-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="79b36-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="79b36-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="79b36-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="79b36-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="79b36-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="79b36-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="79b36-134">Структура **ADRLIST** , вызывающий объект передает в может быть другой размер структуры, которые возвращает MAPI.</span><span class="sxs-lookup"><span data-stu-id="79b36-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="79b36-135">Если MAPI должен возвращать увеличенное структура **ADRLIST** , он освобождает исходной структуры и выделяет новый.</span><span class="sxs-lookup"><span data-stu-id="79b36-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="79b36-136">После выделения памяти для структуры **ADRLIST** выделите память для каждой структуры **SPropValue** отдельно.</span><span class="sxs-lookup"><span data-stu-id="79b36-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="79b36-137">Дополнительные сведения о том, как выделять и освобождать структуры **ADRLIST** можно [Памяти ADRLIST и SRowSet структур](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="79b36-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="79b36-138">**Адрес** возвращает немедленно, если флаг DIALOG_SDI установлен в член **ulFlags** структуры **ADRPARM** с помощью параметра _lpAdrParms_ .</span><span class="sxs-lookup"><span data-stu-id="79b36-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="79b36-139">Флаг DIALOG_SDI игнорируется для клиентов, не являющиеся Outlook.</span><span class="sxs-lookup"><span data-stu-id="79b36-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="79b36-140">Если DIALOG_SDI игнорируется, будет отображаться версия модального диалогового окна и указатель на маркер не следует ожидать в _lpulUIParam_.</span><span class="sxs-lookup"><span data-stu-id="79b36-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="79b36-141">**Адрес** поддерживает строк символов Юникод в структуре **ADRPARM** , если в **ulFlags** членом **ADRPARM** с помощью параметра _lpAdrParms_ указано значение AB_UNICODEUI и поддерживает Юникод строк символов в ** ADRLIST**.</span><span class="sxs-lookup"><span data-stu-id="79b36-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="79b36-142">Строки Юникод преобразуются в формат многобайтовой строки (MBCS), прежде чем они будут отображаться в диалоговом окне Outlook адресной книги.</span><span class="sxs-lookup"><span data-stu-id="79b36-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="79b36-143">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="79b36-143">MFCMAPI reference</span></span>

<span data-ttu-id="79b36-144">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="79b36-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="79b36-145">**����**</span><span class="sxs-lookup"><span data-stu-id="79b36-145">**File**</span></span>|<span data-ttu-id="79b36-146">**�������**</span><span class="sxs-lookup"><span data-stu-id="79b36-146">**Function**</span></span>|<span data-ttu-id="79b36-147">**�����������**</span><span class="sxs-lookup"><span data-stu-id="79b36-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="79b36-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="79b36-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="79b36-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="79b36-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="79b36-150">Mfcmapi (en) использует метод **адрес** разрешить пользователю выберите почтовый ящик, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="79b36-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79b36-151">См. также</span><span class="sxs-lookup"><span data-stu-id="79b36-151">See also</span></span>



[<span data-ttu-id="79b36-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="79b36-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="79b36-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="79b36-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="79b36-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="79b36-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="79b36-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="79b36-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="79b36-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="79b36-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="79b36-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="79b36-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="79b36-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="79b36-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="79b36-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="79b36-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="79b36-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="79b36-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="79b36-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="79b36-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="79b36-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="79b36-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="79b36-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="79b36-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="79b36-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="79b36-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="79b36-165">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="79b36-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="79b36-166">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="79b36-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

