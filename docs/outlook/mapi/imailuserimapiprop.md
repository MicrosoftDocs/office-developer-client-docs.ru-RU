---
title: IMailUser IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMailUser
api_type:
- COM
ms.assetid: 74c25870-62d9-484a-9a99-4dc35c52479e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a0e109fe95120483e700bab5b82f6d7cb75e2e28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436596"
---
# <a name="imailuser--imapiprop"></a><span data-ttu-id="b0ab7-103">IMailUser : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b0ab7-103">IMailUser : IMAPIProp</span></span>

  
  
<span data-ttu-id="b0ab7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0ab7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0ab7-105">Предоставляет доступ к многим свойствам, связанным с пользователями обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b0ab7-105">Provides access to the many properties that are associated with messaging users.</span></span> <span data-ttu-id="b0ab7-106">Интерфейс **IMailUser** реализуется объектами пользователей обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b0ab7-106">The **IMailUser** interface is implemented by messaging user objects.</span></span> <span data-ttu-id="b0ab7-107">**IMailUser** наследует интерфейс [IMAPIProp : IUnknown](imapipropiunknown.md) и не имеет собственных уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="b0ab7-107">**IMailUser** inherits from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface and has no unique methods of its own.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0ab7-108">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b0ab7-108">Header file:</span></span>  <br/> |<span data-ttu-id="b0ab7-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b0ab7-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b0ab7-110">Подвергается:</span><span class="sxs-lookup"><span data-stu-id="b0ab7-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="b0ab7-111">Объекты пользователей обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="b0ab7-111">Messaging user objects</span></span>  <br/> |
|<span data-ttu-id="b0ab7-112">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="b0ab7-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="b0ab7-113">Поставщики адресных книг</span><span class="sxs-lookup"><span data-stu-id="b0ab7-113">Address book providers</span></span>  <br/> |
|<span data-ttu-id="b0ab7-114">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="b0ab7-114">Called by:</span></span>  <br/> |<span data-ttu-id="b0ab7-115">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="b0ab7-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="b0ab7-116">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="b0ab7-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b0ab7-117">IID_IMailUser</span><span class="sxs-lookup"><span data-stu-id="b0ab7-117">IID_IMailUser</span></span>  <br/> |
|<span data-ttu-id="b0ab7-118">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="b0ab7-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="b0ab7-119">LPMAILUSER</span><span class="sxs-lookup"><span data-stu-id="b0ab7-119">LPMAILUSER</span></span>  <br/> |
|<span data-ttu-id="b0ab7-120">Модель транзакции:</span><span class="sxs-lookup"><span data-stu-id="b0ab7-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="b0ab7-121">Transacted</span><span class="sxs-lookup"><span data-stu-id="b0ab7-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b0ab7-122">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="b0ab7-122">Vtable order</span></span>

<span data-ttu-id="b0ab7-123">Этот интерфейс не имеет уникальных методов.</span><span class="sxs-lookup"><span data-stu-id="b0ab7-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="b0ab7-124">**Обязательные свойства**</span><span class="sxs-lookup"><span data-stu-id="b0ab7-124">**Required properties**</span></span>|<span data-ttu-id="b0ab7-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="b0ab7-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b0ab7-126">**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-126">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0ab7-127">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b0ab7-127">Read/write</span></span>  <br/> |
|<span data-ttu-id="b0ab7-128">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-128">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0ab7-129">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b0ab7-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="b0ab7-130">**PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-130">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0ab7-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0ab7-131">Read-only</span></span>  <br/> |
|<span data-ttu-id="b0ab7-132">**PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-132">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0ab7-133">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="b0ab7-133">Read/write</span></span>  <br/> |
|<span data-ttu-id="b0ab7-134">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-134">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0ab7-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0ab7-135">Read-only</span></span>  <br/> |
|<span data-ttu-id="b0ab7-136">**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-136">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0ab7-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0ab7-137">Read-only</span></span>  <br/> |
|<span data-ttu-id="b0ab7-138">**PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b0ab7-138">**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0ab7-139">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0ab7-139">Read-only</span></span>  <br/> |
|<span data-ttu-id="b0ab7-140">**PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-140">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="b0ab7-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b0ab7-141">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0ab7-142">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0ab7-142">Remarks</span></span>

<span data-ttu-id="b0ab7-143">Пять из необходимых свойств известны как базовые свойства адресов для получателей:</span><span class="sxs-lookup"><span data-stu-id="b0ab7-143">Five of the required properties are known as the base address properties for recipients:</span></span>
  
- <span data-ttu-id="b0ab7-144">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="b0ab7-144">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="b0ab7-145">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="b0ab7-145">**PR_DISPLAY_NAME**</span></span>
    
- <span data-ttu-id="b0ab7-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="b0ab7-146">**PR_EMAIL_ADDRESS**</span></span>
    
- <span data-ttu-id="b0ab7-147">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="b0ab7-147">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="b0ab7-148">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="b0ab7-148">**PR_SEARCH_KEY**</span></span>
    
<span data-ttu-id="b0ab7-149">Эти свойства считаются особыми, так как многие другие группы аналогичных свойств построены на этой базовой группе.</span><span class="sxs-lookup"><span data-stu-id="b0ab7-149">These properties are considered special because many other groups of similar properties are built upon this base group.</span></span> <span data-ttu-id="b0ab7-150">Другие группы используются для описания получателя в различных ролях, таких как исходный или делегированная отправитель сообщения.</span><span class="sxs-lookup"><span data-stu-id="b0ab7-150">The other groups are used to describe a recipient in various roles, such as a message's original or delegate sender.</span></span> <span data-ttu-id="b0ab7-151">Дополнительные сведения об этих свойствах и о том, как их использовать, см. в дополнительных [сведениях о типах адресов MAPI.](mapi-address-types.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-151">For more information about these properties and how to use them, see [MAPI Address Types](mapi-address-types.md).</span></span>
  
<span data-ttu-id="b0ab7-152">Пользователи обмена сообщениями могут отображать коллекцию своих свойств, **поддерживая** свойство [PR_DETAILS_TABLE (PidTagDetailsTable).](pidtagdetailstable-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-152">Messaging users can display a collection of their properties by supporting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="b0ab7-153">**PR_DETAILS_TABLE** — это таблица отображения, описываемая макет диалогового окна с деталями или страница свойства на вкладке, на которую отображаются сведения о свойстве получателей.</span><span class="sxs-lookup"><span data-stu-id="b0ab7-153">**PR_DETAILS_TABLE** is a display table that describes the layout of a details dialog box or a tabbed property page that displays recipient property information.</span></span> <span data-ttu-id="b0ab7-154">MAPI создает диалоговые окна с подробными сведениями, когда клиент вызывает [метод IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-154">MAPI creates details dialog boxes when a client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
  
<span data-ttu-id="b0ab7-155">Объекты пользователей сообщений могут иметь другие необязательные свойства, связанные с ними.</span><span class="sxs-lookup"><span data-stu-id="b0ab7-155">Messaging user objects can have other optional properties associated with them.</span></span> <span data-ttu-id="b0ab7-156">MAPI определяет множество свойств, которые предоставляют дополнительные сведения о пользователе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b0ab7-156">MAPI defines many properties that provide additional addressing information about a messaging user.</span></span> <span data-ttu-id="b0ab7-157">Все эти свойства являются строками символов.</span><span class="sxs-lookup"><span data-stu-id="b0ab7-157">All of these properties are character strings.</span></span> <span data-ttu-id="b0ab7-158">В следующем списке показаны наиболее часто используемые свойства:</span><span class="sxs-lookup"><span data-stu-id="b0ab7-158">The following list shows the more commonly used properties:</span></span>
  
- <span data-ttu-id="b0ab7-159">**PR_ACCOUNT** [(PidTagAccount)](pidtagaccount-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-159">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span> 
    
- <span data-ttu-id="b0ab7-160">**PR_ASSISTANT** [(PidTagAssistant)](pidtagassistant-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-160">**PR_ASSISTANT** ([PidTagAssistant](pidtagassistant-canonical-property.md))</span></span> 
    
- <span data-ttu-id="b0ab7-161">**PR_BUSINESS_TELEPHONE_NUMBER** [(PidTagBusinessTelephoneNumber)](pidtagbusinesstelephonenumber-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-161">**PR_BUSINESS_TELEPHONE_NUMBER** ([PidTagBusinessTelephoneNumber](pidtagbusinesstelephonenumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="b0ab7-162">**PR_GIVEN_NAME** [(PidTagGivenName)](pidtaggivenname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-162">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="b0ab7-163">**PR_GOVERNMENT_ID_NUMBER** [(PidTagGovernmentIdNumber)](pidtaggovernmentidnumber-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-163">**PR_GOVERNMENT_ID_NUMBER** ([PidTagGovernmentIdNumber](pidtaggovernmentidnumber-canonical-property.md))</span></span> 
    
- <span data-ttu-id="b0ab7-164">**PR_LOCALITY** [(PidTagLocality)](pidtaglocality-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-164">**PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))</span></span> 
    
- <span data-ttu-id="b0ab7-165">**PR_POSTAL_ADDRESS** [(PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b0ab7-165">**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md))</span></span> 
    
<span data-ttu-id="b0ab7-166">Полный список свойств см. в списке Сопоставление имен канонических свойств [с именами MAPI.](mapping-canonical-property-names-to-mapi-names.md)</span><span class="sxs-lookup"><span data-stu-id="b0ab7-166">For a complete list of properties, see [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0ab7-167">См. также</span><span class="sxs-lookup"><span data-stu-id="b0ab7-167">See also</span></span>



[<span data-ttu-id="b0ab7-168">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="b0ab7-168">MAPI Interfaces</span></span>](mapi-interfaces.md)

