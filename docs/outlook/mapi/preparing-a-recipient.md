---
title: Подготовка получателя
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9573f10c-66e1-4e87-93f0-89687e906b8b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b4ccfb8cf8201a17993932acc4c0104ace80b94d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588722"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="cdbce-103">Подготовка получателя</span><span class="sxs-lookup"><span data-stu-id="cdbce-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="cdbce-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdbce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdbce-105">Клиентское приложение подготавливает получателей, преобразование их краткосрочных идентификаторы записей для долгосрочного идентификаторы записей и возможно добавления, изменения или изменение порядка свойств.</span><span class="sxs-lookup"><span data-stu-id="cdbce-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="cdbce-106">Можно подготовить получателей, которые являются частью списка получателей сообщения или получателей, не относящихся к сообщению.</span><span class="sxs-lookup"><span data-stu-id="cdbce-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="cdbce-107">Как правило клиенты вызывать [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) непосредственно для перевода краткосрочных идентификаторы записей в долгосрочного идентификаторы записей для получателей, включенных в стандартным диалоговым окном адрес.</span><span class="sxs-lookup"><span data-stu-id="cdbce-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="cdbce-108">Для получателей, которые связаны с исходящих сообщений подготовки получателями обрабатывается процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="cdbce-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="cdbce-109">Чтобы подготовить список получателей, вызовите **IAddrBook::PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="cdbce-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="cdbce-110">**PrepareRecips** принимает структуру [ADRLIST](adrlist.md) и список тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="cdbce-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="cdbce-111">Структура **ADRLIST** содержит получателей для подготовки во время список свойств тега представляет свойства, которые должны поддерживать каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="cdbce-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="cdbce-112">**PrepareRecips** предпринимает попытку свойства, которые включены в список свойств тега в начале структуры **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="cdbce-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="cdbce-113">Если какие-либо свойства в списке отсутствуют структура **ADRLIST** , MAPI вызывает поставщик адресной книги, чтобы предоставить им.</span><span class="sxs-lookup"><span data-stu-id="cdbce-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="cdbce-114">Если необходимо проверить наличие долгосрочного идентификаторы записей, передайте значение NULL для параметра _lpSPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="cdbce-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="cdbce-115">Например предположим, что вы работаете с пятью получателей.</span><span class="sxs-lookup"><span data-stu-id="cdbce-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="cdbce-116">Все получатели отображаются в структуре **ADRLIST** следующие свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="cdbce-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="cdbce-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdbce-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="cdbce-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdbce-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="cdbce-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdbce-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="cdbce-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdbce-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="cdbce-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdbce-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="cdbce-122">Три свойства включены в структуре **ADRLIST** для первых двух получателей.</span><span class="sxs-lookup"><span data-stu-id="cdbce-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="cdbce-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdbce-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="cdbce-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdbce-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="cdbce-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cdbce-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="cdbce-126">Поскольку всех получателей должны иметь свои первые три свойства **PR_ADDRTYPE**, **PR_ENTRYID**и **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), создание массива тега свойства с помощью этих свойств и передайте он и структуре **ADRLIST** для **PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="cdbce-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="cdbce-127">**PrepareRecips** вызывает метод **IMAPIProp::GetProps** каждого получателя, чтобы получить **PR_HOME_TELEPHONE_NUMBER** , так как он не является частью структуры **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="cdbce-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="cdbce-128">При возврате **PrepareRecips** списка получателей представляет объединенного списка получателей со свойствами в структуре **ADRLIST** может выглядеть для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="cdbce-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="cdbce-129">Список получателей для получателей 1 и 2 содержит свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="cdbce-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="cdbce-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="cdbce-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="cdbce-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="cdbce-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="cdbce-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="cdbce-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="cdbce-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="cdbce-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="cdbce-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="cdbce-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="cdbce-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="cdbce-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="cdbce-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="cdbce-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="cdbce-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="cdbce-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="cdbce-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="cdbce-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="cdbce-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="cdbce-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="cdbce-140">Список получателей для получателей, 3, 4 и 5 включает в себя свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="cdbce-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="cdbce-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="cdbce-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="cdbce-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="cdbce-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="cdbce-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="cdbce-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="cdbce-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="cdbce-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="cdbce-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="cdbce-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="cdbce-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="cdbce-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="cdbce-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="cdbce-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="cdbce-148">В качестве альтернативы для вызова **IAddrBook::PrepareRecips** для работы со свойствами, вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) каждого получателя и, при необходимости его метод [IMAPIProp::SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="cdbce-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="cdbce-149">Когда выполняется только один получатель, либо метод удовлетворяют.</span><span class="sxs-lookup"><span data-stu-id="cdbce-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="cdbce-150">Тем не менее, когда задействованы несколько получателей, вызов **PrepareRecips** , а не методы **IMAPIProp** экономит время и, работающие удаленно, много удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="cdbce-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="cdbce-151">**PrepareRecips** обрабатывает всех получателей в одном вызове, тогда как **GetProps** и **SetProps** выполнение одного звонка для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="cdbce-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

