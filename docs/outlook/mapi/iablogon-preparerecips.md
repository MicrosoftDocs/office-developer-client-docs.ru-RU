---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423862"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="36269-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="36269-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="36269-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36269-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36269-105">Подготавливает список получателей для более позднего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="36269-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="36269-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="36269-106">Parameters</span></span>

<span data-ttu-id="36269-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="36269-107">_ulFlags_</span></span>
  
> <span data-ttu-id="36269-108">[in] Немного флагов, которые контролируют тип текста в возвращенных строках.</span><span class="sxs-lookup"><span data-stu-id="36269-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="36269-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="36269-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="36269-110">MAPI_CACHE_ONLY. Для выполнения разрешения имен используйте только офлайн-адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="36269-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="36269-111">Например, этот флаг можно использовать, чтобы разрешить клиентской приложению открывать глобальный список адресов (GAL) в кэшном режиме обмена и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="36269-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="36269-112">Этот флаг поддерживается только поставщиком Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="36269-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="36269-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="36269-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="36269-114">[in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, которые указывают свойства, которые требуют обновления, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="36269-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="36269-115">Параметр  _lpPropTagArray может_ быть NULL.</span><span class="sxs-lookup"><span data-stu-id="36269-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="36269-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="36269-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="36269-117">[in] Указатель на структуру [ADRLIST,](adrlist.md) которая содержит список получателей.</span><span class="sxs-lookup"><span data-stu-id="36269-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36269-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36269-118">Return value</span></span>

<span data-ttu-id="36269-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="36269-119">S_OK</span></span> 
  
> <span data-ttu-id="36269-120">Список получателей был успешно подготовлен.</span><span class="sxs-lookup"><span data-stu-id="36269-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="36269-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="36269-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="36269-122">Один или несколько получателей в параметре  _lpRecipList_ не существуют.</span><span class="sxs-lookup"><span data-stu-id="36269-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="36269-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36269-123">Return value</span></span>

<span data-ttu-id="36269-124">Клиент вызывает метод MAPI [IAddrBook::P repareRecips,](iaddrbook-preparerecips.md) чтобы изменить или изменить набор свойств для одного или более получателей.</span><span class="sxs-lookup"><span data-stu-id="36269-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="36269-125">Получатели могут быть или не быть частью списка получателей исходя из сообщения.</span><span class="sxs-lookup"><span data-stu-id="36269-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="36269-126">MAPI передает этот вызов **методу IABLogon::P repareRecips.**</span><span class="sxs-lookup"><span data-stu-id="36269-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="36269-127">**IABLogon::P repareRecips** выполняет четыре основные задачи:</span><span class="sxs-lookup"><span data-stu-id="36269-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="36269-128">Гарантирует, что все получатели в списке адресов, на которые указывает параметр  _lpRecipList,_ имеют долгосрочный идентификатор входа.</span><span class="sxs-lookup"><span data-stu-id="36269-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="36269-129">Гарантирует, что все получатели имеют свойства, указанные в массиве значений свойств, указанных _параметром lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="36269-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="36269-130">Гарантирует, что свойства из массива значений свойств отображаются перед любыми другими свойствами, существовать до вызова.</span><span class="sxs-lookup"><span data-stu-id="36269-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="36269-131">Гарантирует, что порядок свойств в структуре [ADRENTRY](adrentry.md) каждого получателя в **структуре ADRLIST** будет таким же, как в массиве значений свойств.</span><span class="sxs-lookup"><span data-stu-id="36269-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="36269-132">Структура **ADRENTRY** в параметре  _lpRecipList_ содержит одну **структуру ADRENTRY** для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="36269-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="36269-133">Каждая **структура ADRENTRY** содержит массив [структур SPropValue](spropvalue.md) для описания свойств получателя.</span><span class="sxs-lookup"><span data-stu-id="36269-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="36269-134">Когда **возвращается IABLogon::P repareRecips,** массив **структуры SPropValue** для каждого получателя включает свойства  _из lpPropTagArray,_ а затем другие свойства для получателя.</span><span class="sxs-lookup"><span data-stu-id="36269-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="36269-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="36269-135">Notes to implementers</span></span>

<span data-ttu-id="36269-136">Реализация **IABLogon::P repareRecips** предполагает ввод свойств в определенный порядок, ирисовку значений свойств и преобразование краткосрочных идентификаторов записей в долгосрочные идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="36269-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="36269-137">Свойства, запрашиваемые в параметре _lpPropTagArray,_ должны быть в начале массива значений свойств, связанного со структурой **ADRENTRY** каждого получателя в параметре _lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="36269-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="36269-138">Если значений для этих свойств не существует, откройте связанного пользователя обмена сообщениями или список рассылки с помощью его идентификатора записи и извлекайте недостающие значения свойств.</span><span class="sxs-lookup"><span data-stu-id="36269-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="36269-139">Распределите каждую структуру **SPropValue,** переданную в  _lpRecipList_ отдельно, чтобы эти структуры могли быть освобождены по отдельности.</span><span class="sxs-lookup"><span data-stu-id="36269-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="36269-140">Если необходимо выделить дополнительное пространство для любой структуры **SPropValue,** например для хранения данных для свойства строки, используйте функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) для выделения дополнительного пространства для полного массива значений свойства.</span><span class="sxs-lookup"><span data-stu-id="36269-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="36269-141">Используйте [функцию MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить исходный массив значений свойств, а затем использовать функцию [MAPIAllocateMore,](mapiallocatemore.md) чтобы выделить любую необходимую дополнительную память.</span><span class="sxs-lookup"><span data-stu-id="36269-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="36269-142">Чтобы реализовать **IABLogon::P repareRecips,** используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="36269-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="36269-143">Проверьте записи в _параметре lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="36269-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="36269-144">Если массив значений свойств пуст, не нужно делать никаких работ.</span><span class="sxs-lookup"><span data-stu-id="36269-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="36269-145">Возврат значения успешности.</span><span class="sxs-lookup"><span data-stu-id="36269-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="36269-146">Обработать каждого получателя в _параметре lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="36269-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="36269-147">Для каждого получателя в списке имеется один член структуры **ADRENTRY.**</span><span class="sxs-lookup"><span data-stu-id="36269-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="36269-148">Игнорируйте следующие типы получателей:</span><span class="sxs-lookup"><span data-stu-id="36269-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="36269-149">Получатели без идентификатора записи в **члене rgPropVals** их **структуры ADRENTRY** (то есть неурегулированных получателей).</span><span class="sxs-lookup"><span data-stu-id="36269-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="36269-150">Получатели с идентификатором записи, который не принадлежит поставщику.</span><span class="sxs-lookup"><span data-stu-id="36269-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="36269-151">Эти получатели будут переданы другому поставщику адресной книги.</span><span class="sxs-lookup"><span data-stu-id="36269-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="36269-152">Откройте получателя и извлекай свойства, которые уже настроены для получателя.</span><span class="sxs-lookup"><span data-stu-id="36269-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="36269-153">Объединение массива значений свойств, указанного в _lpRecipList,_ с массивом свойств, возвращаемых **из GetProps.**</span><span class="sxs-lookup"><span data-stu-id="36269-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="36269-154">Если одно и то же свойство встречается в обоих массивах свойств, используйте значение _из lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="36269-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="36269-155">Если массив  _свойств lpRecipList_ достаточно велик, чтобы вместить все необходимые свойства, просто замените его объединенным массивом.</span><span class="sxs-lookup"><span data-stu-id="36269-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="36269-156">Если массив  _свойств lpRecipList_ недостаточно велик, замените его новым выделенным массивом.</span><span class="sxs-lookup"><span data-stu-id="36269-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="36269-157">Убедитесь, что новый массив имеет обновленное значение в каждом из членов **cValues.**</span><span class="sxs-lookup"><span data-stu-id="36269-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="36269-158">Если вы не распознаёте одно или несколько свойств в параметре  _lpPropTagArray,_ установите тип свойства в структуре **ADRENTRY** получателя PT_ERROR и значение свойства MAPI_E_NOT_FOUND или другое значение, которое дает более конкретную причину недоступности свойства.</span><span class="sxs-lookup"><span data-stu-id="36269-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="36269-159">Сведения о PT_ERROR см. в этой PT_ERROR [типах свойств.](property-types.md)</span><span class="sxs-lookup"><span data-stu-id="36269-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="36269-160">Никогда не перерасполнять структуру **ADRLIST,** которая передается в **IABLogon::P repareRecips,** или изменять ее количество записей.</span><span class="sxs-lookup"><span data-stu-id="36269-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36269-161">См. также</span><span class="sxs-lookup"><span data-stu-id="36269-161">See also</span></span>

- [<span data-ttu-id="36269-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="36269-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="36269-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="36269-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="36269-164">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="36269-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="36269-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="36269-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="36269-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36269-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

