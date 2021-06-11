---
title: Создание списка получателей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428216"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="92530-103">Создание списка получателей</span><span class="sxs-lookup"><span data-stu-id="92530-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="92530-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92530-105">Список получателей — это структура [ADRLIST,](adrlist.md) которая содержит массив структур значений свойств для каждого получателя сообщения , предназначенного для сообщения.</span><span class="sxs-lookup"><span data-stu-id="92530-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="92530-106">Получатель может представлять пользователя, машину или папку.</span><span class="sxs-lookup"><span data-stu-id="92530-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="92530-107">Для всех отправленных сообщений требуется, по крайней мере, один получатель, который прошел процесс разрешения **имен, —** процесс обеспечения того, чтобы свойство [PR_ENTRYID (PidTagEntryId)](pidtagentryid-canonical-property.md)было включено в массив свойств получателя.</span><span class="sxs-lookup"><span data-stu-id="92530-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="92530-108">Свойства получателя — это сочетание свойств адресной книги и свойств сообщений.</span><span class="sxs-lookup"><span data-stu-id="92530-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="92530-109">Свойства получателя могут применяться либо к всем сообщениям для конкретного получателя, либо только к текущему сообщению.</span><span class="sxs-lookup"><span data-stu-id="92530-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="92530-110">Оба поставщика хранения сообщений и поставщики транспорта могут устанавливать свойства получателей.</span><span class="sxs-lookup"><span data-stu-id="92530-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="92530-111">Каждый получатель должен иметь базовый набор свойств в массиве значений свойств к моменту готовности к отправлению сообщения.</span><span class="sxs-lookup"><span data-stu-id="92530-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="92530-112">Необходимый набор свойств получателей:</span><span class="sxs-lookup"><span data-stu-id="92530-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="92530-113">**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="92530-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="92530-114">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="92530-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="92530-115">**PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="92530-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="92530-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="92530-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="92530-117">**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="92530-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="92530-118">**PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="92530-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="92530-119">Эти свойства используются для доступа к получателю, отправки ему сообщений и сравнения с другими.</span><span class="sxs-lookup"><span data-stu-id="92530-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="92530-120">Не все эти свойства должны быть доступны сразу.</span><span class="sxs-lookup"><span data-stu-id="92530-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="92530-121">Вы можете добавить получателя изначально, не зная его идентификатор входа, полагаясь на процесс разрешения имен, чтобы назначить это свойство.</span><span class="sxs-lookup"><span data-stu-id="92530-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="92530-122">В какой-то момент перед отправкой сообщения позвоните [в IAddrBook::ResolveName,](iaddrbook-resolvename.md) чтобы убедиться, что все получатели в списке получателей будут устранены.</span><span class="sxs-lookup"><span data-stu-id="92530-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="92530-123">Дополнительные сведения см. в [дополнительных сведениях, в том, как разрешить имя получателя.](resolving-a-recipient-name.md)</span><span class="sxs-lookup"><span data-stu-id="92530-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="92530-124">Списки получателей можно создавать из пользователей сообщений или записей списков рассылки в контейнере адресной книги или из разных.</span><span class="sxs-lookup"><span data-stu-id="92530-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="92530-125">Отдельные получатели — это получатели, созданные в качестве временных записей, которые будут использоваться только для обращения к одному сообщению или в качестве записей, которые будут добавлены в личную адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="92530-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="92530-126">Формат идентификатора и адреса для одноавтной записи определяется MAPI.</span><span class="sxs-lookup"><span data-stu-id="92530-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="92530-127">Дополнительные сведения об этих форматах см. в [документе One-Off Addresses](one-off-addresses.md) и [One-Off Entry Identifiers.](one-off-entry-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="92530-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="92530-128">Вы можете позволить пользователям создавать списки получателей:</span><span class="sxs-lookup"><span data-stu-id="92530-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="92530-129">Только с записями из адресной книги.</span><span class="sxs-lookup"><span data-stu-id="92530-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="92530-130">Только с одноавтными записями.</span><span class="sxs-lookup"><span data-stu-id="92530-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="92530-131">Сочетание получателей адресной книги и разовая.</span><span class="sxs-lookup"><span data-stu-id="92530-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="92530-132">**Создание списка получателей с помощью общего диалогового окна адресов**</span><span class="sxs-lookup"><span data-stu-id="92530-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="92530-133">Выделение [структуры ADRPARM](adrparm.md) и указателя в [структуру ADRLIST.](adrlist.md)</span><span class="sxs-lookup"><span data-stu-id="92530-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="92530-134">Обнуление памяти в **структуре ADRPARM** и задав указатель **ADRLIST** NULL.</span><span class="sxs-lookup"><span data-stu-id="92530-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="92530-135">Вызов [IAddrBook::Address,](iaddrbook-address.md) чтобы отобразить диалоговое окно адреса и заполнить **структуру ADRPARM.**</span><span class="sxs-lookup"><span data-stu-id="92530-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="92530-136">Вызов [IMessage::ModifyRecipients,](imessage-modifyrecipients.md)передавая **указатель ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="92530-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="92530-137">Эта структура будет содержать свойства каждого получателя, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="92530-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="92530-138">**Создание списка получателей программным путем**</span><span class="sxs-lookup"><span data-stu-id="92530-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="92530-139">**Выделим структуру ADRLIST,** которая содержит одну [структуру ADRENTRY](adrentry.md) для каждого из получателей, которые будут включены в список.</span><span class="sxs-lookup"><span data-stu-id="92530-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="92530-140">Сделайте каждую структуру **ADRENTRY** достаточно большой, чтобы удерживать каждое из необходимых свойств **и** PR_RECIPIENT_TYPE [(PidTagRecipientType).](pidtagrecipienttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="92530-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="92530-141">Для каждого получателя установите массив значений свойств для его **участника aEntries** в **структуре ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="92530-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="92530-142">Вызов [IMessage::ModifyRecipients](imessage-modifyrecipients.md) с MODRECIP_ADD флагом.</span><span class="sxs-lookup"><span data-stu-id="92530-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

