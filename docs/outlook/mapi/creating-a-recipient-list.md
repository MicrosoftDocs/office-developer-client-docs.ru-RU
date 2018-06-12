---
title: Создание списка получателей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: fa23377a8b080ae9dac3e31dfa137ca03a242c74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808255"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="6fb14-103">Создание списка получателей</span><span class="sxs-lookup"><span data-stu-id="6fb14-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="6fb14-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6fb14-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6fb14-105">Список получателей является структурой [ADRLIST](adrlist.md) , который содержит массив структур значение свойства для каждого получателя сообщения — назначения для сообщения.</span><span class="sxs-lookup"><span data-stu-id="6fb14-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="6fb14-106">Получатель может представлять человеческого пользователя, компьютера или папки.</span><span class="sxs-lookup"><span data-stu-id="6fb14-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="6fb14-107">Все сообщения, отправляемые требуется по крайней мере одного получателя, которое было через процесс разрешения имен — процесс для проверка того, что свойство **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) включается в массив значений свойств получателя.</span><span class="sxs-lookup"><span data-stu-id="6fb14-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="6fb14-108">Свойства получателя — это сочетание свойств адресной книги и свойства сообщения.</span><span class="sxs-lookup"><span data-stu-id="6fb14-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="6fb14-109">Свойствами получателя можно применять ко всем сообщениям для отдельного получателя или только для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="6fb14-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="6fb14-110">Оба сообщения хранилища и поставщиками транспорта можно задать свойствами получателя.</span><span class="sxs-lookup"><span data-stu-id="6fb14-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="6fb14-111">Каждого получателя, необходимо иметь базовый набор свойств в его массива значение свойства, время, когда сообщение Готово к отправке.</span><span class="sxs-lookup"><span data-stu-id="6fb14-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="6fb14-112">Необходимый набор параметров учетной записи получателя включают:</span><span class="sxs-lookup"><span data-stu-id="6fb14-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="6fb14-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fb14-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6fb14-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fb14-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6fb14-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fb14-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6fb14-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="6fb14-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="6fb14-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fb14-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="6fb14-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fb14-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="6fb14-119">Эти свойства используются для доступа к получателя, отправлять сообщения и сравнить его с другими пользователями.</span><span class="sxs-lookup"><span data-stu-id="6fb14-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="6fb14-120">Не все эти свойства должны быть доступны сразу.</span><span class="sxs-lookup"><span data-stu-id="6fb14-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="6fb14-121">Можно добавить получателя изначально неизвестны его идентификатор записи полагаться на процесс разрешения имен для назначения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="6fb14-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="6fb14-122">Перед отправкой сообщения вызовите [IAddrBook::ResolveName](iaddrbook-resolvename.md) , чтобы убедиться в том, что все сообщения, в список получателей разрешаются.</span><span class="sxs-lookup"><span data-stu-id="6fb14-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="6fb14-123">Для получения дополнительных сведений см [разрешения имени получателя](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="6fb14-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="6fb14-124">Можно создать списки получателей из системы обмена сообщениями пользователи или элементы списка рассылки в контейнер адресной книги или one-offs.</span><span class="sxs-lookup"><span data-stu-id="6fb14-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="6fb14-125">One-offs являются получателей, которые создаются в качестве временных записей для использования только для одного сообщения-адресов или записей для добавления к адресной книге.</span><span class="sxs-lookup"><span data-stu-id="6fb14-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="6fb14-126">Формат идентификатора единичных записей и адреса определяется MAPI.</span><span class="sxs-lookup"><span data-stu-id="6fb14-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="6fb14-127">Дополнительные сведения об этих форматах можно [Одноразовых адресов](one-off-addresses.md) и [Одноразовых идентификаторы записей](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="6fb14-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="6fb14-128">Можно разрешить пользователям создавать свои списки получателей:</span><span class="sxs-lookup"><span data-stu-id="6fb14-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="6fb14-129">Только с записями из адресной книги.</span><span class="sxs-lookup"><span data-stu-id="6fb14-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="6fb14-130">Только с одноразовых записи.</span><span class="sxs-lookup"><span data-stu-id="6fb14-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="6fb14-131">Вместе с адресной книгой получателей и one-offs.</span><span class="sxs-lookup"><span data-stu-id="6fb14-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="6fb14-132">**Чтобы создать список получателей с помощью стандартным диалоговым окном адрес**</span><span class="sxs-lookup"><span data-stu-id="6fb14-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="6fb14-133">Выделите структуру [ADRPARM](adrparm.md) и указатель на структуру [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="6fb14-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="6fb14-134">Нулевое значение памяти в структуре **ADRPARM** и установите указатель **ADRLIST** NULL.</span><span class="sxs-lookup"><span data-stu-id="6fb14-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="6fb14-135">Вызов [IAddrBook::Address](iaddrbook-address.md) для отображения диалогового окна адрес и заполнения **ADRPARM** структуры.</span><span class="sxs-lookup"><span data-stu-id="6fb14-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="6fb14-136">Вызовите [IMessage::ModifyRecipients](imessage-modifyrecipients.md), передав указатель **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="6fb14-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="6fb14-137">Эта структура будет содержать свойства каждого из получателей, выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="6fb14-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="6fb14-138">**Создание списка получателей программными средствами**</span><span class="sxs-lookup"><span data-stu-id="6fb14-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="6fb14-139">Выделите структуру **ADRLIST** , которая содержит одну структуру [ADRENTRY](adrentry.md) для каждого из получателей, которые включены в список.</span><span class="sxs-lookup"><span data-stu-id="6fb14-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="6fb14-140">Сделайте каждого **ADRENTRY** структуру, достаточное для хранения всех необходимых свойств и **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6fb14-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="6fb14-141">Для каждого получателя задайте массива значение свойства для элемента его **aEntries** в структуре **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="6fb14-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="6fb14-142">Вызов [IMessage::ModifyRecipients](imessage-modifyrecipients.md) с установленным флагом MODRECIP_ADD.</span><span class="sxs-lookup"><span data-stu-id="6fb14-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

