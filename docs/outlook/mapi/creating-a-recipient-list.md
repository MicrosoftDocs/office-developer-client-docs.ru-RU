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
# <a name="creating-a-recipient-list"></a><span data-ttu-id="616ca-103">Создание списка получателей</span><span class="sxs-lookup"><span data-stu-id="616ca-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="616ca-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="616ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="616ca-105">Список получателей — это структура [ADRLIST,](adrlist.md) которая содержит массив структур значений свойств для каждого получателя сообщения — назначения для сообщения.</span><span class="sxs-lookup"><span data-stu-id="616ca-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="616ca-106">Получатель может представлять пользователя, компьютер или папку.</span><span class="sxs-lookup"><span data-stu-id="616ca-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="616ca-107">Для всех отослаенных сообщений требуется по крайней мере один получатель, который прошел процесс разрешения **имен—** процесс, обеспечивающий, чтобы свойство PR_ENTRYID [(PidTagEntryId)](pidtagentryid-canonical-property.md)было включено в массив значений свойств получателя.</span><span class="sxs-lookup"><span data-stu-id="616ca-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="616ca-108">Свойства получателя — это сочетание свойств адресной книги и сообщений.</span><span class="sxs-lookup"><span data-stu-id="616ca-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="616ca-109">Свойства получателя могут применяться либо к всем сообщениям для определенного получателя, либо только к текущему сообщению.</span><span class="sxs-lookup"><span data-stu-id="616ca-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="616ca-110">Как поставщики хранения сообщений, так и поставщики транспорта могут устанавливать свойства получателей.</span><span class="sxs-lookup"><span data-stu-id="616ca-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="616ca-111">Каждый получатель должен иметь основной набор свойств в массиве значений свойств к моменту, когда сообщение будет готово к отправлению.</span><span class="sxs-lookup"><span data-stu-id="616ca-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="616ca-112">К обязательному набору свойств получателей относятся:</span><span class="sxs-lookup"><span data-stu-id="616ca-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="616ca-113">**PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="616ca-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="616ca-114">**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="616ca-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="616ca-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="616ca-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="616ca-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="616ca-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="616ca-117">**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="616ca-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="616ca-118">**PR_SEARCH_KEY** ([PidTagSearchKey)](pidtagsearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="616ca-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="616ca-119">Эти свойства используются для доступа к получателю, отправки ему сообщений и сравнения с другими.</span><span class="sxs-lookup"><span data-stu-id="616ca-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="616ca-120">Не все эти свойства должны быть доступны сразу.</span><span class="sxs-lookup"><span data-stu-id="616ca-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="616ca-121">Вы можете добавить получателя изначально, не зная его идентификатор записи, назначив этому свойству процесс разрешения имен.</span><span class="sxs-lookup"><span data-stu-id="616ca-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="616ca-122">В определенный момент перед отправкой сообщения вызовите [IAddrBook::ResolveName,](iaddrbook-resolvename.md) чтобы убедиться, что все получатели в списке получателей разрешены.</span><span class="sxs-lookup"><span data-stu-id="616ca-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="616ca-123">Дополнительные сведения см. в под [названием "Разрешение имени получателя".](resolving-a-recipient-name.md)</span><span class="sxs-lookup"><span data-stu-id="616ca-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="616ca-124">Списки получателей могут создаваться из записей пользователей сообщений или списков рассылки в контейнере адресной книги или из разных мест.</span><span class="sxs-lookup"><span data-stu-id="616ca-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="616ca-125">Единственными получателями являются получатели, которые создаются как временные записи, которые используются только для обращения к одному сообщению или в качестве записей, добавляемой в личную адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="616ca-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="616ca-126">Формат идентификатора и адреса однораховой записи определяется с помощью MAPI.</span><span class="sxs-lookup"><span data-stu-id="616ca-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="616ca-127">Дополнительные сведения об этих форматах см. в записях [one-off Addresses](one-off-addresses.md) и [One-Off Entry Identifiers.](one-off-entry-identifiers.md)</span><span class="sxs-lookup"><span data-stu-id="616ca-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="616ca-128">Вы можете позволить пользователям создавать списки получателей:</span><span class="sxs-lookup"><span data-stu-id="616ca-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="616ca-129">Только с записями из адресной книги.</span><span class="sxs-lookup"><span data-stu-id="616ca-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="616ca-130">Только с одновключными записями.</span><span class="sxs-lookup"><span data-stu-id="616ca-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="616ca-131">С сочетанием получателей адресной книги и одного разов.</span><span class="sxs-lookup"><span data-stu-id="616ca-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="616ca-132">**Создание списка получателей с помощью диалогового окна общего адреса**</span><span class="sxs-lookup"><span data-stu-id="616ca-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="616ca-133">Выделим [структуру ADRPARM](adrparm.md) и указатель на [структуру ADRLIST.](adrlist.md)</span><span class="sxs-lookup"><span data-stu-id="616ca-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="616ca-134">Обнуление памяти в **структуре ADRPARM** и установите для указателя **ADRLIST** значение NULL.</span><span class="sxs-lookup"><span data-stu-id="616ca-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="616ca-135">Вызовите [IAddrBook::Address,](iaddrbook-address.md) чтобы отобразить диалоговое окно адреса и заполнить структуру **ADRPARM.**</span><span class="sxs-lookup"><span data-stu-id="616ca-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="616ca-136">Вызовите [IMessage::ModifyRecipients,](imessage-modifyrecipients.md)передавая **указатель ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="616ca-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="616ca-137">Эта структура будет содержать свойства каждого получателя, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="616ca-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="616ca-138">**Создание списка получателей программным путем**</span><span class="sxs-lookup"><span data-stu-id="616ca-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="616ca-139">Выделим **структуру ADRLIST,** которая содержит одну структуру [ADRENTRY](adrentry.md) для каждого получателя, который будет включен в список.</span><span class="sxs-lookup"><span data-stu-id="616ca-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="616ca-140">Сделайте **каждую структуру ADRENTRY** достаточно большой, чтобы она удерживала все необходимые свойства **и** PR_RECIPIENT_TYPE ([PidTagRecipientType).](pidtagrecipienttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="616ca-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="616ca-141">Для каждого получателя установите массив значений свойств для его **члена aEntries** в структуре **ADRLIST.**</span><span class="sxs-lookup"><span data-stu-id="616ca-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="616ca-142">Вызовите [IMessage::ModifyRecipients](imessage-modifyrecipients.md) с MODRECIP_ADD флага.</span><span class="sxs-lookup"><span data-stu-id="616ca-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

