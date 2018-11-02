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
ms.openlocfilehash: c42077528a4f7227321d8f987cc5dd0ccd4c966c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589744"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="3ab01-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="3ab01-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="3ab01-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ab01-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ab01-105">Подготовка списка получателей для дальнейшего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3ab01-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="3ab01-106">���������</span><span class="sxs-lookup"><span data-stu-id="3ab01-106">Parameters</span></span>

<span data-ttu-id="3ab01-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ab01-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3ab01-108">[in] Битовая маска флаги, определяющее тип текста в возвращенных строк.</span><span class="sxs-lookup"><span data-stu-id="3ab01-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="3ab01-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="3ab01-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="3ab01-110">MAPI_CACHE_ONLY: Для выполнения разрешения имен используйте автономной адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3ab01-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="3ab01-111">Например можно использовать этот флаг позволяет открыть глобальный список адресов (GAL) в режиме кэширования данных exchange и получить доступ к записи в этот список адресов из кэша без создания трафика между клиентом и сервером клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="3ab01-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="3ab01-112">Этот флаг поддерживается только поставщик Exchange адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3ab01-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="3ab01-113">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="3ab01-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="3ab01-114">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив тегов свойств, которые указывают свойства, которым требуется обновление, при их наличии.</span><span class="sxs-lookup"><span data-stu-id="3ab01-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="3ab01-115">Параметр _lpPropTagArray_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="3ab01-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="3ab01-116">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="3ab01-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="3ab01-117">[in] Указатель на структуру [ADRLIST](adrlist.md) , в котором размещается список получателей.</span><span class="sxs-lookup"><span data-stu-id="3ab01-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3ab01-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ab01-118">Return value</span></span>

<span data-ttu-id="3ab01-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ab01-119">S_OK</span></span> 
  
> <span data-ttu-id="3ab01-120">Список получателей успешно подготовлен.</span><span class="sxs-lookup"><span data-stu-id="3ab01-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="3ab01-121">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="3ab01-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="3ab01-122">Один или несколько получателей с помощью параметра _lpRecipList_ не существует.</span><span class="sxs-lookup"><span data-stu-id="3ab01-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3ab01-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ab01-123">Return value</span></span>

<span data-ttu-id="3ab01-124">Клиент вызывает метод MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) , изменить или переместить набор свойств для одного или нескольких получателей.</span><span class="sxs-lookup"><span data-stu-id="3ab01-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="3ab01-125">Получатели могут или не может быть частью списка получателей исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="3ab01-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="3ab01-126">MAPI передает этот вызов метода **IABLogon::PrepareRecips** поставщика адресных книг.</span><span class="sxs-lookup"><span data-stu-id="3ab01-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="3ab01-127">**IABLogon::PrepareRecips** выполняет четырех основных задач:</span><span class="sxs-lookup"><span data-stu-id="3ab01-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="3ab01-128">Гарантирует, что всех получателей в списке адресов, на который указывает параметр _lpRecipList_ обеспечивает долгосрочного идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="3ab01-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="3ab01-129">Гарантирует, что всем получателям свойства, указанные в массиве значение свойства указывает параметр _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="3ab01-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="3ab01-130">Гарантирует, что прежде чем другие свойства, существовавшего до вызова отображаются свойства из массива значение свойства.</span><span class="sxs-lookup"><span data-stu-id="3ab01-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="3ab01-131">Гарантирует, что порядок свойств в структуре [ADRENTRY](adrentry.md) каждого получателя в структуре **ADRLIST** совпадает со значением массива значение свойства.</span><span class="sxs-lookup"><span data-stu-id="3ab01-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="3ab01-132">Структура **ADRENTRY** с помощью параметра _lpRecipList_ содержит одну структуру **ADRENTRY** для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="3ab01-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="3ab01-133">Структура каждого **ADRENTRY** содержит массив структур [SPropValue](spropvalue.md) для описания свойства получателя.</span><span class="sxs-lookup"><span data-stu-id="3ab01-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="3ab01-134">При возврате **IABLogon::PrepareRecips** массива **SPropValue** структуры для каждого получателя, включает в себя свойства из _lpPropTagArray_ , а затем другие свойства для получателя.</span><span class="sxs-lookup"><span data-stu-id="3ab01-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3ab01-135">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="3ab01-135">Notes to implementers</span></span>

<span data-ttu-id="3ab01-136">Реализация **IABLogon::PrepareRecips** включает в себя выравнивание свойства в определенном порядке, извлечение значения свойств и преобразование краткосрочных идентификаторы записей для долгосрочного идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="3ab01-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="3ab01-137">Свойства, которые запрашиваются с помощью параметра _lpPropTagArray_ должны быть в начале массива значение свойства, связанные со структурой **ADRENTRY** каждого получателя с помощью параметра _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="3ab01-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="3ab01-138">Если значения этих свойств не существует, откройте связанного обмена сообщениями пользователя или список рассылки с помощью его идентификатор записи и извлечение отсутствующие значения свойств.</span><span class="sxs-lookup"><span data-stu-id="3ab01-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="3ab01-139">Выделите каждый **SPropValue** структуры, переданного _lpRecipList_ отдельно, чтобы структур можно освободить по отдельности.</span><span class="sxs-lookup"><span data-stu-id="3ab01-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="3ab01-140">Если необходимо выделить дополнительного места на диске для любого **SPropValue** структуры, например, для хранения данных, для свойства строки, функция [MAPIAllocateBuffer](mapiallocatebuffer.md) для выделения дополнительного места на диске для массива значение полного свойства.</span><span class="sxs-lookup"><span data-stu-id="3ab01-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="3ab01-141">Используйте функцию [MAPIFreeBuffer](mapifreebuffer.md) , чтобы освободить место на исходный массив значение свойства и затем использовать функцию [MAPIAllocateMore](mapiallocatemore.md) распределения любой дополнительной памяти, который является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3ab01-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="3ab01-142">Чтобы реализовать **IABLogon::PrepareRecips**, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="3ab01-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="3ab01-143">Проверьте наличие записи с помощью параметра _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="3ab01-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="3ab01-144">Если пустое значение массива свойства нет заданий для выполнения.</span><span class="sxs-lookup"><span data-stu-id="3ab01-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="3ab01-145">Возвращает значения успеха.</span><span class="sxs-lookup"><span data-stu-id="3ab01-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="3ab01-146">Обработать каждого получателя, с помощью параметра _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="3ab01-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="3ab01-147">Существует один член **ADRENTRY** структуры для каждого получателя в списке.</span><span class="sxs-lookup"><span data-stu-id="3ab01-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="3ab01-148">Пропуск следующие типы получателей:</span><span class="sxs-lookup"><span data-stu-id="3ab01-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="3ab01-149">Получатели без идентификатора записи в элементе **rgPropVals** их **ADRENTRY** структуры (то есть, нерешенные получателей).</span><span class="sxs-lookup"><span data-stu-id="3ab01-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="3ab01-150">Получатели с идентификатором записи, которая не относится к поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="3ab01-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="3ab01-151">Эти получателей будет передан другой поставщик адресной книги.</span><span class="sxs-lookup"><span data-stu-id="3ab01-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="3ab01-152">Откройте получателя и извлечения свойств, которые уже задано для получателя.</span><span class="sxs-lookup"><span data-stu-id="3ab01-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="3ab01-153">Объединение массива значение свойства, указанного в _lpRecipList_ с массивом свойств, возвращенный из **GetProps**.</span><span class="sxs-lookup"><span data-stu-id="3ab01-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="3ab01-154">Если же свойство возникает в обоих массивах свойство, используйте значение из _lpRecipList_.</span><span class="sxs-lookup"><span data-stu-id="3ab01-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="3ab01-155">Если массива значение свойства _lpRecipList_ размер все необходимые свойства, просто замените его с объединенными массива.</span><span class="sxs-lookup"><span data-stu-id="3ab01-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="3ab01-156">Если массива значение свойства _lpRecipList_ не, замените его вновь выделенный массива.</span><span class="sxs-lookup"><span data-stu-id="3ab01-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="3ab01-157">Убедитесь, что новый массив имеет обновленное значение в каждой из его члены **cValues** .</span><span class="sxs-lookup"><span data-stu-id="3ab01-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="3ab01-158">Если вы не распознают одно или несколько свойств с помощью параметра _lpPropTagArray_ , необходимо задайте тип свойства в структуре **ADRENTRY** получателя PT_ERROR и значение свойства MAPI_E_NOT_FOUND или другое значение, которое обеспечивает более причины недоступности свойства.</span><span class="sxs-lookup"><span data-stu-id="3ab01-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="3ab01-159">Сведения о PT_ERROR содержатся [Типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="3ab01-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="3ab01-160">Никогда не перемещать структура **ADRLIST** , передаваемый в **IABLogon::PrepareRecips** или измените его число записей.</span><span class="sxs-lookup"><span data-stu-id="3ab01-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ab01-161">См. также</span><span class="sxs-lookup"><span data-stu-id="3ab01-161">See also</span></span>

- [<span data-ttu-id="3ab01-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="3ab01-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="3ab01-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="3ab01-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="3ab01-164">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="3ab01-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="3ab01-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="3ab01-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="3ab01-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ab01-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

