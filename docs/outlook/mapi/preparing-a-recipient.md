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
ms.openlocfilehash: bb6bc8b8d0199ab07d5dad353dbc25da240593e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419879"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="158ae-103">Подготовка получателя</span><span class="sxs-lookup"><span data-stu-id="158ae-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="158ae-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="158ae-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="158ae-105">Клиентская заявка подготавливает получателей путем преобразования их краткосрочных идентификаторов записей в идентификаторы долгосрочных записей и, возможно, добавления, изменения или изменения свойств.</span><span class="sxs-lookup"><span data-stu-id="158ae-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="158ae-106">Можно подготовить получателей, которые являются частью списка получателей, для сообщения или получателей, не связанных с сообщением.</span><span class="sxs-lookup"><span data-stu-id="158ae-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="158ae-107">Как правило, клиенты звонят [в IAddrBook::P repareRecips](iaddrbook-preparerecips.md) напрямую, чтобы перевести краткосрочные идентификаторы записи в долгосрочные идентификаторы записей для получателей, включенных в диалоговое окно общего адреса.</span><span class="sxs-lookup"><span data-stu-id="158ae-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="158ae-108">Для получателей, связанных с исходя из сообщения, подготовка получателей обрабатывается процессом разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="158ae-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="158ae-109">Чтобы подготовить список получателей, позвоните **в IAddrBook::P repareRecips**.</span><span class="sxs-lookup"><span data-stu-id="158ae-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="158ae-110">**PrepareRecips** принимает структуру [ADRLIST](adrlist.md) и список тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="158ae-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="158ae-111">Структура **ADRLIST содержит** получателей, которые должны быть подготовлены, а список тегов свойств представляет свойства, которые должен поддерживать каждый получатель.</span><span class="sxs-lookup"><span data-stu-id="158ae-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="158ae-112">**PrepareRecips** пытается разместить свойства, включенные в список тегов свойств в начале **структуры ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="158ae-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="158ae-113">Если какие-либо из свойств в списке отсутствуют в структуре **ADRLIST,** MAPI вызывает поставщика адресной книги для их поставки.</span><span class="sxs-lookup"><span data-stu-id="158ae-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="158ae-114">Если вам нужно проверить только долгосрочные идентификаторы записи, передайте NULL для _параметра lpSPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="158ae-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="158ae-115">Например, предположим, что вы работаете с пятью получателями.</span><span class="sxs-lookup"><span data-stu-id="158ae-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="158ae-116">Все пять получателей отображаются в **структуре ADRLIST** со следующими свойствами в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="158ae-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="158ae-117">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="158ae-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="158ae-118">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="158ae-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="158ae-119">**PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="158ae-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="158ae-120">**PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="158ae-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="158ae-121">**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="158ae-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="158ae-122">Три других свойства включены в структуру **ADRLIST** для первых двух получателей.</span><span class="sxs-lookup"><span data-stu-id="158ae-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="158ae-123">**PR_ACCOUNT** [(PidTagAccount)](pidtagaccount-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="158ae-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="158ae-124">**PR_GIVEN_NAME** [(PidTagGivenName)](pidtaggivenname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="158ae-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="158ae-125">**PR_SURNAME** [(PidTagSurname)](pidtagsurname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="158ae-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="158ae-126">Так как все получатели должны иметь в качестве первых трех свойств **PR_ADDRTYPE,** **PR_ENTRYID** и **PR_HOME_TELEPHONE_NUMBER** [(PidTagHomeTelephoneNumber),](pidtaghometelephonenumber-canonical-property.md)создайте массив тегов свойств с этими свойствами и передайте его и структуру **ADRLIST** **в PrepareRecips**.</span><span class="sxs-lookup"><span data-stu-id="158ae-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="158ae-127">**PrepareRecips** вызывает метод **IMAPIProp::GetProps** **для** получения PR_HOME_TELEPHONE_NUMBER, так как в настоящее время он не входит в структуру **ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="158ae-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="158ae-128">Когда **PrepareRecips** возвращается, список получателей представляет собой объединенный список получателей с свойствами, включенными в структуру **ADRLIST,** которые отображаются первыми для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="158ae-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="158ae-129">Список получателей для получателей 1 и 2 включает свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="158ae-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="158ae-130">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="158ae-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="158ae-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="158ae-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="158ae-132">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="158ae-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="158ae-133">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="158ae-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="158ae-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="158ae-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="158ae-135">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="158ae-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="158ae-136">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="158ae-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="158ae-137">**PR_ACCOUNT**</span><span class="sxs-lookup"><span data-stu-id="158ae-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="158ae-138">**PR_GIVEN_NAME**</span><span class="sxs-lookup"><span data-stu-id="158ae-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="158ae-139">**PR_SURNAME**</span><span class="sxs-lookup"><span data-stu-id="158ae-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="158ae-140">Список получателей для получателей 3, 4 и 5 включает свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="158ae-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="158ae-141">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="158ae-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="158ae-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="158ae-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="158ae-143">**PR_HOME_TELEPHONE_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="158ae-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="158ae-144">**PR_DISPLAY_NAME**</span><span class="sxs-lookup"><span data-stu-id="158ae-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="158ae-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="158ae-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="158ae-146">**PR_EMAIL_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="158ae-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="158ae-147">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="158ae-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="158ae-148">В качестве альтернативы вызову **IAddrBook::P repareRecips** для работы с свойствами вызываем метод [IMAPIProp::GetProps](imapiprop-getprops.md) каждого получателя и, при необходимости, его [метод IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="158ae-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="158ae-149">Если задействован только один получатель, любой метод является удовлетворительным.</span><span class="sxs-lookup"><span data-stu-id="158ae-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="158ae-150">Однако при вовлечении нескольких получателей вызов **PrepareRecips,** а не методы **IMAPIProp** экономит время и, если вы работаете удаленно, много удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="158ae-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="158ae-151">**PrepareRecips** обрабатывает всех получателей одним вызовом, в то время как **GetProps** и **SetProps** делают по одному вызову для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="158ae-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

