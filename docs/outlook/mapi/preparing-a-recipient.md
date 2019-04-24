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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350675"
---
# <a name="preparing-a-recipient"></a><span data-ttu-id="d36d7-103">Подготовка получателя</span><span class="sxs-lookup"><span data-stu-id="d36d7-103">Preparing a Recipient</span></span>

  
  
<span data-ttu-id="d36d7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d36d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d36d7-105">Клиентское приложение подготавливает получателей путем преобразования краткосрочных идентификаторов записей в долгосрочные идентификаторы записей и, возможно, для добавления, изменения или изменения порядка свойств.</span><span class="sxs-lookup"><span data-stu-id="d36d7-105">A client application prepares recipients by converting their short-term entry identifiers to long-term entry identifiers and possibly adding, changing, or reordering properties.</span></span> <span data-ttu-id="d36d7-106">Можно подготовить получателей, которые входят в список получателей, для сообщений или получателей, не связанных с сообщением.</span><span class="sxs-lookup"><span data-stu-id="d36d7-106">You can prepare recipients that are part of a recipient list for a message or recipients that are unrelated to a message.</span></span> <span data-ttu-id="d36d7-107">Как правило, клиенты вызывают [IAddrBook::P репаререЦипс](iaddrbook-preparerecips.md) напрямую, чтобы перевести краткосрочные идентификаторы записей в долгосрочные идентификаторы записей для получателей, включенных в диалоговое окно Общий адрес.</span><span class="sxs-lookup"><span data-stu-id="d36d7-107">Typically, clients call [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) directly to translate short-term entry identifiers into long-term entry identifiers for recipients that are included in the common address dialog box.</span></span> <span data-ttu-id="d36d7-108">Для получателей, связанных с исходящим сообщением, подготовка получателей обрабатывается с помощью процесса разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="d36d7-108">For recipients that are associated with an outgoing message, recipient preparation is handled by the name resolution process.</span></span> 
  
<span data-ttu-id="d36d7-109">Чтобы подготовить список получателей, вызовите **IAddrBook::P репаререЦипс**.</span><span class="sxs-lookup"><span data-stu-id="d36d7-109">To prepare a list of recipients, call **IAddrBook::PrepareRecips**.</span></span> <span data-ttu-id="d36d7-110">**ПрепаререЦипс** принимает в качестве значения структуру [ADRLIST](adrlist.md) и список тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="d36d7-110">**PrepareRecips** accepts an [ADRLIST](adrlist.md) structure and a list of property tags.</span></span> <span data-ttu-id="d36d7-111">Структура **ADRLIST** содержит получателей для подготовки, в то время как список тегов свойств представляет свойства, которые должны поддерживаться каждым получателем.</span><span class="sxs-lookup"><span data-stu-id="d36d7-111">The **ADRLIST** structure contains the recipients to be prepared while the property tag list represents properties that each recipient should support.</span></span> <span data-ttu-id="d36d7-112">**ПрепаререЦипс** пытается поместить свойства, включенные в список тегов свойств, в начале структуры **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="d36d7-112">**PrepareRecips** attempts to place the properties that are included in the property tag list at the beginning of the **ADRLIST** structure.</span></span> <span data-ttu-id="d36d7-113">Если какое бы то ни было из свойств в списке отсутствует в структуре **ADRLIST** , MAPI вызывает поставщик адресной книги для их предоставления.</span><span class="sxs-lookup"><span data-stu-id="d36d7-113">If any of the properties in the list are missing from the **ADRLIST** structure, MAPI calls the address book provider to supply them.</span></span> <span data-ttu-id="d36d7-114">Если требуется проверить только долгосрочные идентификаторы записей, передайте значение NULL для параметра _лпспроптагаррай_ .</span><span class="sxs-lookup"><span data-stu-id="d36d7-114">If you only need to check for long-term entry identifiers, pass NULL for the  _lpSPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="d36d7-115">Например, предположим, что вы работаете с пятью получателями.</span><span class="sxs-lookup"><span data-stu-id="d36d7-115">For example, suppose you are working with five recipients.</span></span> <span data-ttu-id="d36d7-116">Все пять получателей отображаются в структуре **ADRLIST** со следующими свойствами в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="d36d7-116">All five recipients appear in the **ADRLIST** structure with the following properties in the following order:</span></span> 
  
1. <span data-ttu-id="d36d7-117">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d36d7-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
2. <span data-ttu-id="d36d7-118">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d36d7-118">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="d36d7-119">**Пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d36d7-119">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>
    
4. <span data-ttu-id="d36d7-120">**Пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d36d7-120">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>
    
5. <span data-ttu-id="d36d7-121">**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d36d7-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
<span data-ttu-id="d36d7-122">Для первых двух получателей в структуру **ADRLIST** включены три других свойства.</span><span class="sxs-lookup"><span data-stu-id="d36d7-122">Three other properties are included in the **ADRLIST** structure for the first two recipients.</span></span> 
  
1. <span data-ttu-id="d36d7-123">**Пр_аккаунт** ([PidTagAccount](pidtagaccount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d36d7-123">**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md))</span></span>
    
2. <span data-ttu-id="d36d7-124">**Пр_гивен_наме** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d36d7-124">**PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md))</span></span>
    
3. <span data-ttu-id="d36d7-125">**Пр_сурнаме** ([PidTagSurname](pidtagsurname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d36d7-125">**PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md))</span></span>
    
<span data-ttu-id="d36d7-126">Так как все получатели должны иметь в качестве первых трех свойств **пр_аддртипе**, **пр_ентрид**и **пр_хоме_телефоне_нумбер** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), создайте массив тегов свойств с этими свойствами и передайте Он и структура **ADRLIST** для **препаререЦипс**.</span><span class="sxs-lookup"><span data-stu-id="d36d7-126">Because all of the recipients need to have as their first three properties **PR_ADDRTYPE**, **PR_ENTRYID**, and **PR_HOME_TELEPHONE_NUMBER** ([PidTagHomeTelephoneNumber](pidtaghometelephonenumber-canonical-property.md)), create a property tag array with these properties and pass it and the **ADRLIST** structure to **PrepareRecips**.</span></span> <span data-ttu-id="d36d7-127">**ПрепаререЦипс** вызывает метод **IMAPIProp::** -PROPS каждого получателя, чтобы получить **пр_хоме_телефоне_нумбер** , так как он в настоящее время не является частью структуры **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="d36d7-127">**PrepareRecips** calls each recipient's **IMAPIProp::GetProps** method to retrieve **PR_HOME_TELEPHONE_NUMBER** because it is not currently part of the **ADRLIST** structure.</span></span> <span data-ttu-id="d36d7-128">Когда возвращается значение **препаререЦипс** , список получателей представляет объединенный список получателей со свойствами, включенными в структуру **ADRLIST** , которые первыми появлялись для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="d36d7-128">When **PrepareRecips** returns, the recipient list represents a merged list of recipients with the properties included in the **ADRLIST** structure appearing first for each recipient.</span></span> 
  
<span data-ttu-id="d36d7-129">Список получателей для получателей 1 и 2 содержит свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="d36d7-129">The recipient list for recipients 1 and 2 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="d36d7-130">**ПР_АДДРТИПЕ**</span><span class="sxs-lookup"><span data-stu-id="d36d7-130">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="d36d7-131">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="d36d7-131">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="d36d7-132">**ПР_ХОМЕ_ТЕЛЕФОНЕ_НУМБЕР**</span><span class="sxs-lookup"><span data-stu-id="d36d7-132">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="d36d7-133">**ПР_ДИСПЛАЙ_НАМЕ**</span><span class="sxs-lookup"><span data-stu-id="d36d7-133">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="d36d7-134">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="d36d7-134">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="d36d7-135">**ПР_ЕМАИЛ_АДДРЕСС**</span><span class="sxs-lookup"><span data-stu-id="d36d7-135">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="d36d7-136">**ПР_АДДРТИПЕ**</span><span class="sxs-lookup"><span data-stu-id="d36d7-136">**PR_ADDRTYPE**</span></span>
    
8. <span data-ttu-id="d36d7-137">**ПР_АККАУНТ**</span><span class="sxs-lookup"><span data-stu-id="d36d7-137">**PR_ACCOUNT**</span></span>
    
9. <span data-ttu-id="d36d7-138">**ПР_ГИВЕН_НАМЕ**</span><span class="sxs-lookup"><span data-stu-id="d36d7-138">**PR_GIVEN_NAME**</span></span>
    
10. <span data-ttu-id="d36d7-139">**ПР_СУРНАМЕ**</span><span class="sxs-lookup"><span data-stu-id="d36d7-139">**PR_SURNAME**</span></span>
    
<span data-ttu-id="d36d7-140">Список получателей для получателей 3, 4 и 5 содержит свойства в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="d36d7-140">The recipient list for recipients 3, 4, and 5 includes properties in the following order:</span></span>
  
1. <span data-ttu-id="d36d7-141">**ПР_АДДРТИПЕ**</span><span class="sxs-lookup"><span data-stu-id="d36d7-141">**PR_ADDRTYPE**</span></span>
    
2. <span data-ttu-id="d36d7-142">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="d36d7-142">**PR_ENTRYID**</span></span>
    
3. <span data-ttu-id="d36d7-143">**ПР_ХОМЕ_ТЕЛЕФОНЕ_НУМБЕР**</span><span class="sxs-lookup"><span data-stu-id="d36d7-143">**PR_HOME_TELEPHONE_NUMBER**</span></span>
    
4. <span data-ttu-id="d36d7-144">**ПР_ДИСПЛАЙ_НАМЕ**</span><span class="sxs-lookup"><span data-stu-id="d36d7-144">**PR_DISPLAY_NAME**</span></span>
    
5. <span data-ttu-id="d36d7-145">**PR_SEARCH_KEY**</span><span class="sxs-lookup"><span data-stu-id="d36d7-145">**PR_SEARCH_KEY**</span></span>
    
6. <span data-ttu-id="d36d7-146">**ПР_ЕМАИЛ_АДДРЕСС**</span><span class="sxs-lookup"><span data-stu-id="d36d7-146">**PR_EMAIL_ADDRESS**</span></span>
    
7. <span data-ttu-id="d36d7-147">**ПР_АДДРТИПЕ**</span><span class="sxs-lookup"><span data-stu-id="d36d7-147">**PR_ADDRTYPE**</span></span>
    
<span data-ttu-id="d36d7-148">В качестве альтернативы вызову **IAddrBook::P репаререЦипс** для работы со свойствами, вызывайте каждый метод [IMAPIProp::](imapiprop-getprops.md) и при необходимости метод [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="d36d7-148">As an alternative to calling **IAddrBook::PrepareRecips** to work with properties, call each recipient's [IMAPIProp::GetProps](imapiprop-getprops.md) method and, if necessary, its [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="d36d7-149">Если используется только один получатель, любой из способов является удовлетворительным.</span><span class="sxs-lookup"><span data-stu-id="d36d7-149">When only one recipient is involved, either technique is satisfactory.</span></span> <span data-ttu-id="d36d7-150">Однако при использовании нескольких получателей вызов **препаререЦипс** , а не методы **IMAPIProp** экономит время и, при удаленном запуске, множество вызовов удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="d36d7-150">However, when multiple recipients are involved, calling **PrepareRecips** rather than the **IMAPIProp** methods saves time and, if you are operating remotely, many remote procedure calls.</span></span> <span data-ttu-id="d36d7-151">**ПрепаререЦипс** обрабатывает все получатели в одном вызове, а \*\*\*\* в **SetProps** — один вызов для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="d36d7-151">**PrepareRecips** processes all recipients in a single call whereas **GetProps** and **SetProps** make one call for each recipient.</span></span> 
  

