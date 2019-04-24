---
title: ИаблогонпрепаререЦипс
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348946"
---
# <a name="iablogonpreparerecips"></a><span data-ttu-id="75d3b-103">IABLogon::PrepareRecips</span><span class="sxs-lookup"><span data-stu-id="75d3b-103">IABLogon::PrepareRecips</span></span>

<span data-ttu-id="75d3b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75d3b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75d3b-105">ПодГотавливает список получателей для последующего использования системой обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="75d3b-105">Prepares a recipient list for later use by the messaging system.</span></span>
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="75d3b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="75d3b-106">Parameters</span></span>

<span data-ttu-id="75d3b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="75d3b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="75d3b-108">возврата Битовая маска флагов, определяющая тип текста в возвращаемых строках.</span><span class="sxs-lookup"><span data-stu-id="75d3b-108">[in] A bitmask of flags that controls the type of the text in the returned strings.</span></span> <span data-ttu-id="75d3b-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="75d3b-109">The following flag can be set:</span></span>
    
  - <span data-ttu-id="75d3b-110">МАПИ_КАЧЕ_ОНЛИ: Используйте только автономную адресную книгу для разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="75d3b-110">MAPI_CACHE_ONLY: Use only the offline address book to perform name resolution.</span></span> <span data-ttu-id="75d3b-111">Например, вы можете использовать этот флаг, чтобы разрешить клиентскому приложению открывать глобальный список адресов (GAL) в режиме кэширования Exchange и получать доступ к записи в этой адресной книге из кэша, не создавая трафик между клиентом и сервером.</span><span class="sxs-lookup"><span data-stu-id="75d3b-111">For example, you can use this flag to allow a client application to open the global address list (GAL) in cached exchange mode and access an entry in that address book from the cache without creating traffic between the client and the server.</span></span> <span data-ttu-id="75d3b-112">Этот флаг поддерживается только поставщиком адресной книги Exchange.</span><span class="sxs-lookup"><span data-stu-id="75d3b-112">This flag is supported only by the Exchange Address Book Provider.</span></span>
    
<span data-ttu-id="75d3b-113">_Лппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="75d3b-113">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="75d3b-114">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , которая содержит массив тегов свойств, указывающих свойства, которые требуют обновления, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="75d3b-114">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags that indicate the properties that require updating, if any.</span></span> <span data-ttu-id="75d3b-115">Параметр _лппроптагаррай_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="75d3b-115">The  _lpPropTagArray_ parameter can be NULL.</span></span> 
    
<span data-ttu-id="75d3b-116">_ЛпреЦиплист_</span><span class="sxs-lookup"><span data-stu-id="75d3b-116">_lpRecipList_</span></span>
  
> <span data-ttu-id="75d3b-117">возврата Указатель на структуру [ADRLIST](adrlist.md) , в которой хранится список получателей.</span><span class="sxs-lookup"><span data-stu-id="75d3b-117">[in] A pointer to an [ADRLIST](adrlist.md) structure that holds the recipient list.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="75d3b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75d3b-118">Return value</span></span>

<span data-ttu-id="75d3b-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="75d3b-119">S_OK</span></span> 
  
> <span data-ttu-id="75d3b-120">Список получателей был успешно подготовлен.</span><span class="sxs-lookup"><span data-stu-id="75d3b-120">The recipient list was successfully prepared.</span></span>
    
<span data-ttu-id="75d3b-121">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="75d3b-121">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="75d3b-122">Один или несколько получателей в параметре _лпреЦиплист_ не существуют.</span><span class="sxs-lookup"><span data-stu-id="75d3b-122">One or more of the recipients in the  _lpRecipList_ parameter do not exist.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="75d3b-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75d3b-123">Return value</span></span>

<span data-ttu-id="75d3b-124">Клиент вызывает метод MAPI [IAddrBook::P репаререЦипс](iaddrbook-preparerecips.md) , чтобы изменить или изменить набор свойств для одного или нескольких получателей.</span><span class="sxs-lookup"><span data-stu-id="75d3b-124">A client calls the MAPI [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) method to modify or rearrange a set of properties for one or more recipients.</span></span> <span data-ttu-id="75d3b-125">Получатели могут или не входить в список получателей исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="75d3b-125">The recipients may or may not be part of the recipient list of an outgoing message.</span></span> <span data-ttu-id="75d3b-126">MAPI передает этот вызов методу поставщика адресных книг **иаблогон::P репаререЦипс** .</span><span class="sxs-lookup"><span data-stu-id="75d3b-126">MAPI transfers this call to an address book provider's **IABLogon::PrepareRecips** method.</span></span> 
  
<span data-ttu-id="75d3b-127">**Иаблогон::P репаререЦипс** выполняет четыре основные задачи:</span><span class="sxs-lookup"><span data-stu-id="75d3b-127">**IABLogon::PrepareRecips** performs four main tasks:</span></span> 
  
- <span data-ttu-id="75d3b-128">Гарантирует, что все получатели в списке адресов, на которые указывает параметр _лпреЦиплист_ , содержат долгосрочный идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="75d3b-128">Ensures that all recipients in the address list pointed to by the  _lpRecipList_ parameter have a long-term entry identifier.</span></span> 
    
- <span data-ttu-id="75d3b-129">Гарантирует, что все получатели имеют свойства, указанные в массиве значений свойства, на который указывает параметр _лппроптагаррай_ .</span><span class="sxs-lookup"><span data-stu-id="75d3b-129">Ensures that all recipients have the properties specified in the property value array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
    
- <span data-ttu-id="75d3b-130">Гарантирует, что свойства из массива значений свойств появятся перед всеми другими свойствами, существовавшими перед вызовом.</span><span class="sxs-lookup"><span data-stu-id="75d3b-130">Ensures that the properties from the property value array appear before any other properties that existed before the call.</span></span>
    
- <span data-ttu-id="75d3b-131">Гарантирует, что порядок свойств в структуре [адрентри](adrentry.md) каждого получателя в структуре **ADRLIST** совпадает с порядком в массиве значений свойства.</span><span class="sxs-lookup"><span data-stu-id="75d3b-131">Ensures that the order of the properties in each recipient's [ADRENTRY](adrentry.md) structure in the **ADRLIST** structure is the same as in the property value array.</span></span> 
    
<span data-ttu-id="75d3b-132">Структура **адрентри** в параметре _лпреЦиплист_ содержит одну структуру **адрентри** для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="75d3b-132">The **ADRENTRY** structure in the  _lpRecipList_ parameter contains one **ADRENTRY** structure for each recipient.</span></span> <span data-ttu-id="75d3b-133">Каждая структура **адрентри** содержит массив структур [спропвалуе](spropvalue.md) , описывающих свойства получателя.</span><span class="sxs-lookup"><span data-stu-id="75d3b-133">Each **ADRENTRY** structure contains an array of [SPropValue](spropvalue.md) structures to describe the recipient's properties.</span></span> <span data-ttu-id="75d3b-134">Когда **иаблогон::P репаререЦипс** возвращает, массив структуры **спропвалуе** для каждого получателя содержит свойства _лппроптагаррай_ , за которыми следуют другие свойства получателя.</span><span class="sxs-lookup"><span data-stu-id="75d3b-134">When **IABLogon::PrepareRecips** returns, the **SPropValue** structure array for each recipient includes the properties from the  _lpPropTagArray_ followed by the other properties for the recipient.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="75d3b-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="75d3b-135">Notes to implementers</span></span>

<span data-ttu-id="75d3b-136">Реализация **иаблогон::P репаререЦипс** включает в себя размещение свойств в определенном порядке, извлечение значений свойств и преобразование коротких идентификаторов записей в долгосрочные идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="75d3b-136">Implementing **IABLogon::PrepareRecips** involves putting properties in a specific order, retrieving property values, and converting short-term entry identifiers to long-term entry identifiers.</span></span> <span data-ttu-id="75d3b-137">Свойства, запрашиваемые в параметре _лппроптагаррай_ , должны находиться в начале массива значений свойства, связанного с каждой структурой **адрентри** каждого получателя в параметре _лпреЦиплист_ .</span><span class="sxs-lookup"><span data-stu-id="75d3b-137">The properties that are requested in the  _lpPropTagArray_ parameter must be at the start of the property value array associated with each recipient's **ADRENTRY** structure in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="75d3b-138">Если значения для этих свойств не существуют, откройте связанный пользователь обмена сообщениями или список рассылки с помощью идентификатора записи и извлеките отсутствующие значения свойств.</span><span class="sxs-lookup"><span data-stu-id="75d3b-138">If values for these properties do not exist, open the associated messaging user or distribution list by using its entry identifier and retrieve the missing property values.</span></span> 
  
<span data-ttu-id="75d3b-139">РазДеляйте каждую структуру **спропвалуе** , переданную в _лпреЦиплист_ , по отдельности, чтобы можно было освободить отдельные структуры.</span><span class="sxs-lookup"><span data-stu-id="75d3b-139">Allocate each **SPropValue** structure passed in  _lpRecipList_ separately so that the structures can be freed individually.</span></span> <span data-ttu-id="75d3b-140">Если необходимо выделить дополнительное пространство для любой структуры **спропвалуе** , например для хранения данных для свойства String, используйте функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , чтобы выделить дополнительное пространство для полного массива значений свойства.</span><span class="sxs-lookup"><span data-stu-id="75d3b-140">If you must allocate additional space for any **SPropValue** structure, for example, to store the data for a string property, use the [MAPIAllocateBuffer](mapiallocatebuffer.md) function to allocate additional space for the full property value array.</span></span> <span data-ttu-id="75d3b-141">С помощью функции [мапифрибуффер](mapifreebuffer.md) Освободите исходный массив значений свойства, а затем используйте функцию [мапиаллокатеморе](mapiallocatemore.md) , чтобы выделить необходимую дополнительную память.</span><span class="sxs-lookup"><span data-stu-id="75d3b-141">Use the [MAPIFreeBuffer](mapifreebuffer.md) function to free the original property value array, and then use the [MAPIAllocateMore](mapiallocatemore.md) function to allocate any additional memory that is required.</span></span> 
  
<span data-ttu-id="75d3b-142">Чтобы реализовать **иаблогон::P репаререЦипс**, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="75d3b-142">To implement **IABLogon::PrepareRecips**, use the following procedure:</span></span>
  
1. <span data-ttu-id="75d3b-143">Проверьте наличие записей в параметре _лппроптагаррай_ .</span><span class="sxs-lookup"><span data-stu-id="75d3b-143">Check for entries in the  _lpPropTagArray_ parameter.</span></span> <span data-ttu-id="75d3b-144">Если массив значений свойства пуст, нет действий, которые можно выполнить.</span><span class="sxs-lookup"><span data-stu-id="75d3b-144">If the property value array is empty, there is no work to do.</span></span> <span data-ttu-id="75d3b-145">Возвращает значение Success.</span><span class="sxs-lookup"><span data-stu-id="75d3b-145">Return a success value.</span></span> 
    
2. <span data-ttu-id="75d3b-146">ОбРаботайте каждого получателя в параметре _лпреЦиплист_ .</span><span class="sxs-lookup"><span data-stu-id="75d3b-146">Process each recipient in the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="75d3b-147">Для каждого получателя в списке существует один элемент структуры **адрентри** .</span><span class="sxs-lookup"><span data-stu-id="75d3b-147">There is one **ADRENTRY** structure member for each recipient in the list.</span></span> <span data-ttu-id="75d3b-148">ПроПускать следующие типы получателей:</span><span class="sxs-lookup"><span data-stu-id="75d3b-148">Ignore the following types of recipients:</span></span> 
    
   - <span data-ttu-id="75d3b-149">Получатели без идентификатора записи в **ргпропвалс** -члене структуры **адрентри** (то есть неразрешенных получателей).</span><span class="sxs-lookup"><span data-stu-id="75d3b-149">Recipients without an entry identifier in the **rgPropVals** member of their **ADRENTRY** structure (that is, unresolved recipients).</span></span> 
    
   - <span data-ttu-id="75d3b-150">Получатели с идентификатором записи, который не принадлежит поставщику.</span><span class="sxs-lookup"><span data-stu-id="75d3b-150">Recipients with an entry identifier that does not belong to your provider.</span></span> <span data-ttu-id="75d3b-151">Эти получатели будут переданы другому поставщику адресных книг.</span><span class="sxs-lookup"><span data-stu-id="75d3b-151">These recipients will be passed to another address book provider.</span></span>
    
3. <span data-ttu-id="75d3b-152">Откройте получателя и извлеките свойства, которые уже заданы для получателя.</span><span class="sxs-lookup"><span data-stu-id="75d3b-152">Open the recipient and retrieve the properties that are already set for the recipient.</span></span>
    
4. <span data-ttu-id="75d3b-153">Слияние массива значений свойства, указанного в параметре _лпреЦиплист_ , с массивом свойств, возвращаемых методом **PROPS**.</span><span class="sxs-lookup"><span data-stu-id="75d3b-153">Merge the property value array specified in the  _lpRecipList_ with the array of properties returned from **GetProps**.</span></span> <span data-ttu-id="75d3b-154">Если одно и то же свойство присутствует в обоих массивах свойств, используйте значение из _лпреЦиплист_.</span><span class="sxs-lookup"><span data-stu-id="75d3b-154">If the same property occurs in both property arrays, use the value from  _lpRecipList_.</span></span>
    
5. <span data-ttu-id="75d3b-155">Если массив значений свойства _лпреЦиплист_ достаточно велик для хранения всех необходимых свойств, просто замените его на объединенный массив.</span><span class="sxs-lookup"><span data-stu-id="75d3b-155">If the  _lpRecipList_ property value array is big enough to hold all of the necessary properties, just replace it with the merged array.</span></span> <span data-ttu-id="75d3b-156">Если массив значений свойства _лпреЦиплист_ недостаточно велик, замените его новым выделенным массивом.</span><span class="sxs-lookup"><span data-stu-id="75d3b-156">If the  _lpRecipList_ property value array is not big enough, replace it with a newly allocated array.</span></span> <span data-ttu-id="75d3b-157">Убедитесь, что новый массив имеет обновленное значение в каждом из его элементов **квалуес** .</span><span class="sxs-lookup"><span data-stu-id="75d3b-157">Be sure the new array has an updated value in each of its **cValues** members.</span></span> 
    
6. <span data-ttu-id="75d3b-158">Если вы не распознаете одно или несколько свойств в параметре _лппроптагаррай_ , задайте для свойства тип свойства в структуре **АДРЕНТРИ** получателя значение пт_еррор, а для свойства — значение мапи_е_нот_фаунд или другое значение, которое предоставляет больше конкретная причина недоступности свойства.</span><span class="sxs-lookup"><span data-stu-id="75d3b-158">If you do not recognize one or more of the properties in the  _lpPropTagArray_ parameter, set the property type in the recipient's **ADRENTRY** structure to PT_ERROR and the property value either to MAPI_E_NOT_FOUND or to another value that gives a more specific reason for the unavailability of the property.</span></span> <span data-ttu-id="75d3b-159">Сведения о ПТ_ЕРРОР можно найти в статье [типы свойств](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="75d3b-159">For information about PT_ERROR, see [Property Types](property-types.md).</span></span>
    
> [!NOTE]
> <span data-ttu-id="75d3b-160">Никогда не Перераспределите структуру **ADRLIST** , переданную в **Иаблогон::P репаререЦипс** или измените количество записей.</span><span class="sxs-lookup"><span data-stu-id="75d3b-160">Never reallocate the **ADRLIST** structure that is passed into **IABLogon::PrepareRecips** or change its number of entries.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="75d3b-161">См. также</span><span class="sxs-lookup"><span data-stu-id="75d3b-161">See also</span></span>

- [<span data-ttu-id="75d3b-162">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="75d3b-162">ADRLIST</span></span>](adrlist.md)
- [<span data-ttu-id="75d3b-163">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="75d3b-163">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
- [<span data-ttu-id="75d3b-164">Каноническое свойство PidTagEntryId</span><span class="sxs-lookup"><span data-stu-id="75d3b-164">PidTagEntryId Canonical Property</span></span>](pidtagentryid-canonical-property.md)
- [<span data-ttu-id="75d3b-165">SPropValue</span><span class="sxs-lookup"><span data-stu-id="75d3b-165">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="75d3b-166">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="75d3b-166">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

