---
title: Иаддрбукаддресс
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
# <a name="iaddrbookaddress"></a><span data-ttu-id="ff15e-103">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="ff15e-103">IAddrBook::Address</span></span>

  
  
<span data-ttu-id="ff15e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff15e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff15e-105">Отображает диалоговое окно "Адресная книга Outlook".</span><span class="sxs-lookup"><span data-stu-id="ff15e-105">Displays the Outlook address book dialog box.</span></span> 
  
```cpp
HRESULT Address(
  ULONG_PTR FAR * lpulUIParam,
  LPADRPARM lpAdrParms,
  LPADRLIST FAR * lppAdrList
);
```

## <a name="parameters"></a><span data-ttu-id="ff15e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff15e-106">Parameters</span></span>

 <span data-ttu-id="ff15e-107">_Лпулуипарам_</span><span class="sxs-lookup"><span data-stu-id="ff15e-107">_lpulUIParam_</span></span>
  
> <span data-ttu-id="ff15e-108">[вход, выход] Указатель на дескриптор родительского окна диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ff15e-108">[in, out] A pointer to a handle of the parent window of the dialog box.</span></span> <span data-ttu-id="ff15e-109">Во входных данных дескриптор окна всегда должен быть передан.</span><span class="sxs-lookup"><span data-stu-id="ff15e-109">On input, a window handle must always be passed.</span></span> <span data-ttu-id="ff15e-110">В выходных данных, если для члена **ulFlags** параметра _лпадрпармс_ задано значение диалог_сди, возвращается дескриптор окна немодального диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ff15e-110">On output, if the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI, the window handle of the modeless dialog box is returned.</span></span> <span data-ttu-id="ff15e-111">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="ff15e-111">See Remarks.</span></span> 
    
 <span data-ttu-id="ff15e-112">_Лпадрпармс_</span><span class="sxs-lookup"><span data-stu-id="ff15e-112">_lpAdrParms_</span></span>
  
> <span data-ttu-id="ff15e-113">[вход, выход] Указатель на структуру [адрпарм](adrparm.md) , которая управляет представлением и поведением диалогового окна "адрес".</span><span class="sxs-lookup"><span data-stu-id="ff15e-113">[in, out] A pointer to an [ADRPARM](adrparm.md) structure that controls the presentation and behavior of the address dialog box.</span></span> 
    
 <span data-ttu-id="ff15e-114">_Лппадрлист_</span><span class="sxs-lookup"><span data-stu-id="ff15e-114">_lppAdrList_</span></span>
  
> <span data-ttu-id="ff15e-115">[вход, выход] Указатель на указатель на структуру [ADRLIST](adrlist.md) , содержащую сведения о получателе.</span><span class="sxs-lookup"><span data-stu-id="ff15e-115">[in, out] A pointer to a pointer to an [ADRLIST](adrlist.md) structure that contains recipient information.</span></span> <span data-ttu-id="ff15e-116">В параметре input этот параметр может иметь значение NULL или указывать на допустимый указатель.</span><span class="sxs-lookup"><span data-stu-id="ff15e-116">On input, this parameter can be NULL or point to a valid pointer.</span></span> <span data-ttu-id="ff15e-117">В выходных данных этот параметр указывает на указатель на допустимые сведения о получателе.</span><span class="sxs-lookup"><span data-stu-id="ff15e-117">On output, this parameter points to a pointer to valid recipient information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ff15e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff15e-118">Return value</span></span>

<span data-ttu-id="ff15e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff15e-119">S_OK</span></span> 
  
> <span data-ttu-id="ff15e-120">Успешно отображено диалоговое окно Common Address.</span><span class="sxs-lookup"><span data-stu-id="ff15e-120">The common address dialog box was successfully displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff15e-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff15e-121">Remarks</span></span>

<span data-ttu-id="ff15e-122">Если для члена **ulFlags** параметра _лпадрпармс_ задано значение диалог_сди, которое предполагает возврат дескриптора окна немодального диалогового окна на выходе, оно игнорируется в Outlook; модальная версия диалогового окна всегда отображается в клиентах, не относящихся к Outlook.</span><span class="sxs-lookup"><span data-stu-id="ff15e-122">If the **ulFlags** member of the  _lpAdrParms_ parameter is set to DIALOG_SDI anticipating the return of the window handle of the modeless dialog box on output, it is ignored in Outlook; the modal version of the dialog is always shown in non-Outlook clients.</span></span> 
  
<span data-ttu-id="ff15e-123">Структура **ADRLIST** , передаваемая через MAPI абоненту с помощью параметра _лппадрлист_ , содержит массив структур [адрентри](adrentry.md) , по одной структуре для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="ff15e-123">The **ADRLIST** structure passed back by MAPI to the caller through the  _lppAdrList_ parameter contains an array of [ADRENTRY](adrentry.md) structures, one structure for each recipient.</span></span> <span data-ttu-id="ff15e-124">При передаче в метод [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) исходящего сообщения в параметре _лпмодс_ структура **ADRLIST** может использоваться для обновления списка получателей.</span><span class="sxs-lookup"><span data-stu-id="ff15e-124">When passed to an outgoing message's [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method in the  _lpMods_ parameter, the **ADRLIST** structure can be used to update its recipient list.</span></span> 
  
<span data-ttu-id="ff15e-125">Каждая структура **адрентри** в структуре **ADRLIST** содержит ноль или более структур [спропвалуе](spropvalue.md) , одна структура для каждого набора свойств получателя.</span><span class="sxs-lookup"><span data-stu-id="ff15e-125">Each **ADRENTRY** structure in the **ADRLIST** structure contains zero or more [SPropValue](spropvalue.md) structures, one structure for every property set for the recipient.</span></span> <span data-ttu-id="ff15e-126">Если для удаления получателя используется диалоговое окно, представленное методом **Address** , может иметь нулевые структуры **спропвалуе** .</span><span class="sxs-lookup"><span data-stu-id="ff15e-126">There can be zero **SPropValue** structures when the dialog box presented by the **Address** method is used to remove a recipient.</span></span> <span data-ttu-id="ff15e-127">При наличии одной или нескольких структур **спропвалуе** для добавления или обновления получателя используется соответствующая структура **адрентри** .</span><span class="sxs-lookup"><span data-stu-id="ff15e-127">When there are one or more **SPropValue** structures, the corresponding **ADRENTRY** structure is used to add or update a recipient.</span></span> <span data-ttu-id="ff15e-128">Получатель может быть разрешен, что указывает на то, что одна из структур **спропвалуе** описывает свойство **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) получателя или является неразрешенным, что указывает на то, что свойство **пр_ентрид** хватает.</span><span class="sxs-lookup"><span data-stu-id="ff15e-128">The recipient can be resolved, which indicates that one of the **SPropValue** structures describes the recipient's **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property, or unresolved, which indicates that the **PR_ENTRYID** property is missing.</span></span> 
  
<span data-ttu-id="ff15e-129">Кроме **пр_ентрид**, разрешенные получатели включают следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="ff15e-129">In addition to **PR_ENTRYID**, resolved recipients include the following properties:</span></span>
  
- <span data-ttu-id="ff15e-130">**Пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ff15e-130">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="ff15e-131">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ff15e-131">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="ff15e-132">**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ff15e-132">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="ff15e-133">**Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ff15e-133">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
<span data-ttu-id="ff15e-134">Структура **ADRLIST** , которую передает вызывающий абонент, может иметь другой размер из структуры, которую возвращает MAPI.</span><span class="sxs-lookup"><span data-stu-id="ff15e-134">The **ADRLIST** structure that the caller passes in might be a different size from the structure that MAPI returns.</span></span> <span data-ttu-id="ff15e-135">Если MAPI должен вернуть более крупную структуру **ADRLIST** , он освобождает исходную структуру и выделяет новую.</span><span class="sxs-lookup"><span data-stu-id="ff15e-135">If MAPI must return a larger **ADRLIST** structure, it frees the original structure and allocates a new one.</span></span> <span data-ttu-id="ff15e-136">При выделении памяти для структуры **ADRLIST** выделяет память для каждой структуры **спропвалуе** отдельно.</span><span class="sxs-lookup"><span data-stu-id="ff15e-136">When you allocate memory for the **ADRLIST** structure, allocate the memory for each **SPropValue** structure separately.</span></span> <span data-ttu-id="ff15e-137">Дополнительные сведения о том, как распределять и освобождать структуры **ADRLIST** , приведены в статье [Управление памятью для структур ADRLIST и SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)</span><span class="sxs-lookup"><span data-stu-id="ff15e-137">For more information about how to allocate and free **ADRLIST** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md)</span></span>
  
 <span data-ttu-id="ff15e-138">**Адрес** немедленно возвращается, если установлен флаг диалог_сди в элементе **ulFlags** структуры **адрпарм** в параметре _лпадрпармс_ .</span><span class="sxs-lookup"><span data-stu-id="ff15e-138">**Address** returns immediately if the DIALOG_SDI flag is set in the **ulFlags** member of the **ADRPARM** structure in the  _lpAdrParms_ parameter.</span></span> <span data-ttu-id="ff15e-139">Флаг ДИАЛОГ_СДИ игнорируется для клиентов, не относящихся к Outlook.</span><span class="sxs-lookup"><span data-stu-id="ff15e-139">The DIALOG_SDI flag is ignored for non-Outlook clients.</span></span> <span data-ttu-id="ff15e-140">Если ДИАЛОГ_СДИ игнорируется, отображается модальная версия диалогового окна, а указатель на дескриптор не должен ожидаться в _лпулуипарам_.</span><span class="sxs-lookup"><span data-stu-id="ff15e-140">If DIALOG_SDI is ignored, the modal version of the dialog will be displayed and a pointer to a handle should not be expected in  _lpulUIParam_.</span></span>
  
 <span data-ttu-id="ff15e-141">**Address** поддерживает строки символов Юникода в структуре **АДРПАРМ** , если аб_уникодеуи был указан в элементе **UlFlags** **адрпарм** в параметре _лпадрпармс_ , и он поддерживает строки символов Юникода в \*\* ADRLIST\*\*.</span><span class="sxs-lookup"><span data-stu-id="ff15e-141">**Address** supports Unicode character strings in the **ADRPARM** structure if AB_UNICODEUI was specified in the **ulFlags** member of **ADRPARM** in the  _lpAdrParms_ parameter, and it supports Unicode character strings in **ADRLIST**.</span></span> <span data-ttu-id="ff15e-142">Строки Юникод преобразуются в формат многобайтовых символов (MBCS), прежде чем они будут отображаться в диалоговом окне Адресная книга Outlook.</span><span class="sxs-lookup"><span data-stu-id="ff15e-142">The Unicode strings are converted to the multibyte character string (MBCS) format before they are displayed in the Outlook address book dialog box.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff15e-143">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ff15e-143">MFCMAPI reference</span></span>

<span data-ttu-id="ff15e-144">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ff15e-144">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff15e-145">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ff15e-145">**File**</span></span>|<span data-ttu-id="ff15e-146">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ff15e-146">**Function**</span></span>|<span data-ttu-id="ff15e-147">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ff15e-147">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff15e-148">Маписторефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="ff15e-148">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="ff15e-149">Опеносерусерсмаилбоксфромгал</span><span class="sxs-lookup"><span data-stu-id="ff15e-149">OpenOtherUsersMailboxFromGal</span></span>  <br/> |<span data-ttu-id="ff15e-150">MFCMAPI использует метод **Address** , позволяющий пользователю выбрать почтовый ящик, который нужно открыть.</span><span class="sxs-lookup"><span data-stu-id="ff15e-150">MFCMAPI uses the **Address** method to allow the user to select which mailbox to open.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff15e-151">См. также</span><span class="sxs-lookup"><span data-stu-id="ff15e-151">See also</span></span>



[<span data-ttu-id="ff15e-152">ADRENTRY</span><span class="sxs-lookup"><span data-stu-id="ff15e-152">ADRENTRY</span></span>](adrentry.md)
  
[<span data-ttu-id="ff15e-153">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="ff15e-153">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="ff15e-154">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="ff15e-154">ADRPARM</span></span>](adrparm.md)
  
[<span data-ttu-id="ff15e-155">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="ff15e-155">FreePadrlist</span></span>](freepadrlist.md)
  
[<span data-ttu-id="ff15e-156">FreeProws</span><span class="sxs-lookup"><span data-stu-id="ff15e-156">FreeProws</span></span>](freeprows.md)
  
[<span data-ttu-id="ff15e-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="ff15e-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="ff15e-158">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="ff15e-158">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="ff15e-159">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ff15e-159">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ff15e-160">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="ff15e-160">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="ff15e-161">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ff15e-161">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ff15e-162">SPropValue</span><span class="sxs-lookup"><span data-stu-id="ff15e-162">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="ff15e-163">SRowSet</span><span class="sxs-lookup"><span data-stu-id="ff15e-163">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="ff15e-164">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ff15e-164">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)


[<span data-ttu-id="ff15e-165">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="ff15e-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="ff15e-166">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ff15e-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

