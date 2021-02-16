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
# <a name="iablogonpreparerecips"></a><span data-ttu-id="cc958-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="cc958-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="cc958-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc958-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc958-105">Подготавливает список получателей к дальнейшему использованию системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="cc958-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="cc958-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc958-106">Parameters</span></span>

<span data-ttu-id="cc958-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cc958-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cc958-108">[in] Битоваяmas флагов, которая управляет типом текста в возвращаемой строке.</span><span class="sxs-lookup"><span data-stu-id="cc958-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="cc958-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="cc958-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="cc958-110">MAPI_CACHE_ONLY: используйте только автономной адресной книги для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="cc958-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="cc958-111">Например, этот флаг можно использовать, чтобы разрешить клиентского приложения открывать глобальный список адресов (GAL) в режиме кэшации exchange и получать доступ к записи в этой адресной книге из кэша без создания трафика между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="cc958-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="cc958-112">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="cc958-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="cc958-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="cc958-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="cc958-114">[in] Указатель на структуру [SPropTagArray,](sproptagarray.md) которая содержит массив тегов свойств, которые указывают свойства, которые требуют обновления, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="cc958-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="cc958-115">Параметр  _lpPropTagArray может_ иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="cc958-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="cc958-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="cc958-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="cc958-117">[in] Указатель на структуру [ADRLIST,](adrlist.md) которая содержит список получателей.</span><span class="sxs-lookup"><span data-stu-id="cc958-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cc958-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc958-118">Return value</span></span>

<span data-ttu-id="cc958-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="cc958-119">S_OK</span></span> 
  
> <span data-ttu-id="cc958-120">Список получателей успешно подготовлен.</span><span class="sxs-lookup"><span data-stu-id="cc958-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="cc958-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cc958-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cc958-122">Один или несколько получателей в параметре  _lpRecipList_ не существуют.</span><span class="sxs-lookup"><span data-stu-id="cc958-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cc958-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc958-123">Return value</span></span>

<span data-ttu-id="cc958-124">Клиент вызывает метод MAPI [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) для изменения или переустановки набора свойств для одного или более получателей.</span><span class="sxs-lookup"><span data-stu-id="cc958-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="cc958-125">Получатели могут быть или не быть частью списка получателей исходяния сообщения.</span><span class="sxs-lookup"><span data-stu-id="cc958-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="cc958-126">MAPI передает этот вызов методу **IABLogon::P repareRecips** поставщика адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cc958-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="cc958-127">**IABLogon::P repareRecips** выполняет четыре основных задачи:</span><span class="sxs-lookup"><span data-stu-id="cc958-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="cc958-128">Гарантирует, что все получатели в списке адресов, на которые указывает параметр  _lpRecipList,_ имеют долгосрочный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="cc958-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="cc958-129">Гарантирует, что у всех получателей есть свойства, указанные в массиве значений свойств, на которые указывает параметр _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="cc958-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="cc958-130">Гарантирует, что свойства из массива значений свойств будут отображаться перед любыми другими свойствами, которые существовали перед вызовом.</span><span class="sxs-lookup"><span data-stu-id="cc958-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="cc958-131">Обеспечивает тот же порядок свойств в структуре [ADRENTRY](adrentry.md) каждого получателя в структуре **ADRLIST,** что и в массиве значений свойств.</span><span class="sxs-lookup"><span data-stu-id="cc958-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="cc958-132">Структура **ADRENTRY** в параметре  _lpRecipList_ содержит одну структуру **ADRENTRY** для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="cc958-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="cc958-133">Каждая **структура ADRENTRY** содержит массив [структур SPropValue](spropvalue.md) для описания свойств получателя.</span><span class="sxs-lookup"><span data-stu-id="cc958-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="cc958-134">Когда **возвращается IABLogon::P repareRecips,** массив структуры **SPropValue** для каждого получателя включает свойства  _из lpPropTagArray_ и другие свойства получателя.</span><span class="sxs-lookup"><span data-stu-id="cc958-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="cc958-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="cc958-135">Notes to implementers</span></span>

<span data-ttu-id="cc958-136">Реализация **IABLogon::P repareRecips** подразумевает размещение свойств в определенном порядке, и получения значений свойств и преобразование краткосрочных идентификаторов записей в долгосрочные идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="cc958-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="cc958-137">Свойства, запрашиваемые в параметре _lpPropTagArray,_ должны быть в начале массива значений свойств, связанного со структурой **ADRENTRY** каждого получателя в параметре _lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="cc958-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="cc958-138">Если значения этих свойств не существуют, откройте связанный с ним пользователь или список рассылки сообщений, используя идентификатор записи и извлекая отсутствующие значения свойств.</span><span class="sxs-lookup"><span data-stu-id="cc958-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="cc958-139">Распределите **каждую структуру SPropValue,** переданную  _в lpRecipList,_ отдельно, чтобы структуры можно было освободить по отдельности.</span><span class="sxs-lookup"><span data-stu-id="cc958-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="cc958-140">Если необходимо выделить дополнительное пространство для любой структуры **SPropValue,** например для хранения данных для строкового свойства, используйте функцию [MAPIAllocateBuffer,](mapiallocatebuffer.md) чтобы выделить дополнительное пространство для всего массива значений свойств.</span><span class="sxs-lookup"><span data-stu-id="cc958-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="cc958-141">Используйте [функцию MAPIFreeBuffer,](mapifreebuffer.md) чтобы освободить исходный массив значений свойств, а затем используйте функцию [MAPIAllocateMore,](mapiallocatemore.md) чтобы выделить дополнительную память, необходимую.</span><span class="sxs-lookup"><span data-stu-id="cc958-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="cc958-142">Чтобы реализовать **IABLogon::P repareRecips,** используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="cc958-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="cc958-143">Проверьте записи в параметре _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="cc958-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="cc958-144">Если массив значений свойств пуст, то не нужно ничего делать.</span><span class="sxs-lookup"><span data-stu-id="cc958-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="cc958-145">Возврат значения успешности.</span><span class="sxs-lookup"><span data-stu-id="cc958-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="cc958-146">Обработать каждого получателя в _параметре lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="cc958-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="cc958-147">Для каждого получателя в списке имеется один член структуры **ADRENTRY.**</span><span class="sxs-lookup"><span data-stu-id="cc958-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="cc958-148">Игнорируйте следующие типы получателей:</span><span class="sxs-lookup"><span data-stu-id="cc958-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="cc958-149">Получатели без идентификатора записи в члене **rgPropVals** их **структуры ADRENTRY** (то есть не разрешенные получатели).</span><span class="sxs-lookup"><span data-stu-id="cc958-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="cc958-150">Получатели с идентификатором записи, который не принадлежит поставщику.</span><span class="sxs-lookup"><span data-stu-id="cc958-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="cc958-151">Эти получатели будут переданы другому поставщику адресной книги.</span><span class="sxs-lookup"><span data-stu-id="cc958-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="cc958-152">Откройте получателя и извлекаете свойства, которые уже настроены для получателя.</span><span class="sxs-lookup"><span data-stu-id="cc958-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="cc958-153">Объединение массива значений свойств, указанного в _lpRecipList,_ с массивом свойств, возвращаемого **getProps.**</span><span class="sxs-lookup"><span data-stu-id="cc958-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="cc958-154">Если одно и то же свойство происходит в обоих массивах свойств, используйте значение _из lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="cc958-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="cc958-155">Если массив  _значений свойств lpRecipList_ достаточно велик для размещения всех необходимых свойств, просто замените его объединенным массивом.</span><span class="sxs-lookup"><span data-stu-id="cc958-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="cc958-156">Если массив  _значений свойств lpRecipList_ недостаточно велик, замените его новым выделенным массивом.</span><span class="sxs-lookup"><span data-stu-id="cc958-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="cc958-157">Убедитесь, что новый массив имеет обновленное значение в каждом из его **членов cValues.**</span><span class="sxs-lookup"><span data-stu-id="cc958-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="cc958-158">Если одно или несколько свойств в параметре  _lpPropTagArray_ не распознаются, установите для типа свойства в структуре **получателя ADRENTRY** значение PT_ERROR и значение свойства MAPI_E_NOT_FOUND или другое значение, которое дает более конкретную причину недоступности свойства.</span><span class="sxs-lookup"><span data-stu-id="cc958-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="cc958-159">Сведения о PT_ERROR [см.](property-types.md)в</span><span class="sxs-lookup"><span data-stu-id="cc958-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="cc958-160">Никогда не перерасполнять структуру **ADRLIST,** которая передается в **IABLogon::P repareRecips,** или изменять количество записей.</span><span class="sxs-lookup"><span data-stu-id="cc958-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc958-161">См. также</span><span class="sxs-lookup"><span data-stu-id="cc958-161">See also</span></span>

- [<span data-ttu-id="cc958-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="cc958-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="cc958-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="cc958-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="cc958-164">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="cc958-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="cc958-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="cc958-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="cc958-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc958-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

