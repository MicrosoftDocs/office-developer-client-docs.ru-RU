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
ms.openlocfilehash: c2546fc990169526361f2c452c50212123d8284d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407909"
---
# <a name="iaddrbookaddress"></a><span data-ttu-id="de787-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="de787-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="de787-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de787-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de787-105">Отображает диалоговое окно адресной книги Outlook.</span><span class="sxs-lookup"><span data-stu-id="de787-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="de787-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="de787-106">Parameters</span></span>

 <span data-ttu-id="de787-107">_lpulUIParam_</span><span class="sxs-lookup"><span data-stu-id="de787-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="de787-108">[in, out] Указатель на окне родительского окна диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="de787-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="de787-109">При вводе всегда должен передаваться окне окне.</span><span class="sxs-lookup"><span data-stu-id="de787-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="de787-110">При выходе, если для члена **ulFlags**  _параметра lpAdrParms_ установлено DIALOG_SDI, возвращается окне окне диалоговых окон без режима.</span><span class="sxs-lookup"><span data-stu-id="de787-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="de787-111">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="de787-111">See Remarks.</span></span> 
    
 <span data-ttu-id="de787-112">_lpAdrParms_</span><span class="sxs-lookup"><span data-stu-id="de787-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="de787-113">[in, out] Указатель на [структуру ADRPARM,](adrparm.md) которая управляет представлением и поведением диалоговых окна адресов.</span><span class="sxs-lookup"><span data-stu-id="de787-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="de787-114">_lppAdrList_</span><span class="sxs-lookup"><span data-stu-id="de787-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="de787-115">[in, out] Указатель на указатель на структуру [ADRLIST,](adrlist.md) которая содержит сведения о получателе.</span><span class="sxs-lookup"><span data-stu-id="de787-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="de787-116">При вводе этот параметр может иметь NULL или указать допустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="de787-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="de787-117">В выходных данных этот параметр указывает на указатель на допустимые сведения о получателе.</span><span class="sxs-lookup"><span data-stu-id="de787-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="de787-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de787-118">Return value</span></span>

<span data-ttu-id="de787-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="de787-119">S_OK</span></span> 
  
> <span data-ttu-id="de787-120">Диалоговое окно общего адреса успешно отобразилось.</span><span class="sxs-lookup"><span data-stu-id="de787-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de787-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="de787-121">Remarks</span></span>

<span data-ttu-id="de787-122">Если для члена **ulFlags**  _параметра lpAdrParms_ задано DIALOG_SDI ожидание возврата окне окне в диалоговом окне без режима при выходе, он игнорируется в Outlook; Модальная версия диалогового окно всегда отображается в клиентах, не в том числе Outlook.</span><span class="sxs-lookup"><span data-stu-id="de787-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="de787-123">Структура **ADRLIST,** переданная mapI вызываемой стороне с помощью параметра  _lppAdrList,_ содержит массив структур [ADRENTRY,](adrentry.md) по одной структуре для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="de787-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="de787-124">При передании методу [IMessage::ModifyRecipients](imessage-modifyrecipients.md) исходяния сообщения в  _параметре lpMods_ структуру **ADRLIST** можно использовать для обновления списка получателей.</span><span class="sxs-lookup"><span data-stu-id="de787-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="de787-125">Каждая **структура ADRENTRY** в структуре **ADRLIST** содержит ноль или несколько [структур SPropValue,](spropvalue.md) по одной структуре для каждого набора свойств получателя.</span><span class="sxs-lookup"><span data-stu-id="de787-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="de787-126">Структуры **SPropValue** могут быть нулевой, если диалоговое окно, представляемые методом **Address,** используется для удаления получателя.</span><span class="sxs-lookup"><span data-stu-id="de787-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="de787-127">Если имеется одна или несколько **структур SPropValue,** соответствующая **структура ADRENTRY** используется для добавления или обновления получателя.</span><span class="sxs-lookup"><span data-stu-id="de787-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="de787-128">Получатель может быть разрешен, что означает, что одна из структур **SPropValue** описывает свойство **PR_ENTRYID** получателя [(PidTagEntryId)](pidtagentryid-canonical-property.md)или не разрешено, что указывает на то, что свойство **PR_ENTRYID** отсутствует.</span><span class="sxs-lookup"><span data-stu-id="de787-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="de787-129">Помимо **PR_ENTRYID,** разрешенные получатели включают следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="de787-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="de787-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="de787-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="de787-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="de787-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="de787-132">**PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="de787-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="de787-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="de787-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="de787-134">Структура **ADRLIST,** в которую передается звоняя, может быть отличается от структуры, возвращаемой MAPI.</span><span class="sxs-lookup"><span data-stu-id="de787-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="de787-135">Если MAPI должен вернуть более крупную структуру **ADRLIST,** она освободит исходную структуру и выделит новую.</span><span class="sxs-lookup"><span data-stu-id="de787-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="de787-136">При выделении памяти для **структуры ADRLIST** выделяете память для каждой **структуры SPropValue** отдельно.</span><span class="sxs-lookup"><span data-stu-id="de787-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="de787-137">Дополнительные сведения о выделении и бесплатном выделении структур **ADRLIST** см. в под управлением памятью [для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="de787-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="de787-138">**Адрес** немедленно возвращается, DIALOG_SDI флага в члене **ulFlags** структуры **ADRPARM** в параметре _lpAdrParms._</span><span class="sxs-lookup"><span data-stu-id="de787-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="de787-139">Флаг DIALOG_SDI игнорируется для клиентов, не вехахав от Outlook.</span><span class="sxs-lookup"><span data-stu-id="de787-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="de787-140">Если DIALOG_SDI игнорируется, отображается модальная версия диалоговое окно, и указатель на handle не следует ожидать в _lpulUIParam._</span><span class="sxs-lookup"><span data-stu-id="de787-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="de787-141"> Адрес поддерживает строки символов Юникода в структуре **ADRPARM,** если AB_UNICODEUI был указан в члене **ulFlags** **ADRPARM** в параметре _lpAdrParms_ и поддерживает строки символов Юникода в **ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="de787-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="de787-142">Строки Юникода преобразуются в формат многобайтовых строк (MBCS) перед их отображением в диалоговом окне адресной книги Outlook.</span><span class="sxs-lookup"><span data-stu-id="de787-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="de787-143">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="de787-143">MFCMAPI reference</span></span>

<span data-ttu-id="de787-144">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="de787-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="de787-145">**Файл**</span><span class="sxs-lookup"><span data-stu-id="de787-145">**File**</span></span>|<span data-ttu-id="de787-146">**Функция**</span><span class="sxs-lookup"><span data-stu-id="de787-146">**Function**</span></span>|<span data-ttu-id="de787-147">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="de787-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="de787-148">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="de787-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="de787-149">OpenOtherUsersMailboxFromGal</span><span class="sxs-lookup"><span data-stu-id="de787-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="de787-150">MFCMAPI использует метод **Address,** чтобы позволить пользователю выбрать, какой почтовый ящик нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="de787-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de787-151">См. также</span><span class="sxs-lookup"><span data-stu-id="de787-151">See also</span></span>



[<span data-ttu-id="de787-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="de787-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="de787-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="de787-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="de787-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="de787-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="de787-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="de787-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="de787-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="de787-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="de787-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="de787-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="de787-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="de787-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="de787-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="de787-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="de787-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="de787-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="de787-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="de787-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="de787-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="de787-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="de787-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="de787-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="de787-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="de787-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="de787-165">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="de787-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="de787-166">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="de787-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

