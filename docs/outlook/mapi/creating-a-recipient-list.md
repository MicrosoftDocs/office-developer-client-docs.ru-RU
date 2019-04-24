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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332909"
---
# <a name="creating-a-recipient-list"></a><span data-ttu-id="da0b9-103">Создание списка получателей</span><span class="sxs-lookup"><span data-stu-id="da0b9-103">Creating a Recipient List</span></span>

  
  
<span data-ttu-id="da0b9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da0b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da0b9-105">Список получателей — это структура [ADRLIST](adrlist.md) , содержащая массив структур значений свойств для каждого получателя сообщения — назначение сообщения.</span><span class="sxs-lookup"><span data-stu-id="da0b9-105">A recipient list is an [ADRLIST](adrlist.md) structure that contains an array of property value structures for each message recipient — destination for the message.</span></span> <span data-ttu-id="da0b9-106">Получатель может представлять пользователя, компьютер или папку.</span><span class="sxs-lookup"><span data-stu-id="da0b9-106">A recipient can represent a human user, a machine, or a folder.</span></span> <span data-ttu-id="da0b9-107">Для всех отправляемых сообщений требуется по крайней мере один получатель, проходящих через процесс разрешения имен — процесс, обеспечивающий включение свойства **пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) в массив значений свойств получателя.</span><span class="sxs-lookup"><span data-stu-id="da0b9-107">All messages to be sent require at least one recipient that has been through the name resolution process — a process for ensuring that the **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) property is included in the recipient's property value array.</span></span> 
  
<span data-ttu-id="da0b9-108">Свойства получателя — это сочетание свойств адресных книг и сообщений.</span><span class="sxs-lookup"><span data-stu-id="da0b9-108">The properties of a recipient are a combination of address book properties and message properties.</span></span> <span data-ttu-id="da0b9-109">Свойства получателей могут быть применены ко всем сообщениям определенного получателя или только к текущему сообщению.</span><span class="sxs-lookup"><span data-stu-id="da0b9-109">Recipient properties can apply either to all messages for a particular recipient or only to the current message.</span></span> <span data-ttu-id="da0b9-110">Как хранилище сообщений, так и поставщики транспорта могут задавать свойства получателей.</span><span class="sxs-lookup"><span data-stu-id="da0b9-110">Both message store and transport providers can set recipient properties.</span></span> 
  
<span data-ttu-id="da0b9-111">Каждый получатель должен иметь основной набор свойств в массиве значений свойств, когда сообщение готово к отправке.</span><span class="sxs-lookup"><span data-stu-id="da0b9-111">Each recipient must have a core set of properties in its property value array by the time the message is ready to be sent.</span></span> <span data-ttu-id="da0b9-112">Обязательный набор свойств получателя включает в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="da0b9-112">The required set of recipient properties include:</span></span>
  
- <span data-ttu-id="da0b9-113">**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="da0b9-113">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="da0b9-114">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="da0b9-114">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span> 
    
- <span data-ttu-id="da0b9-115">**Пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="da0b9-115">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="da0b9-116">**PR_ENTRYID**</span><span class="sxs-lookup"><span data-stu-id="da0b9-116">**PR_ENTRYID**</span></span>
    
- <span data-ttu-id="da0b9-117">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="da0b9-117">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span> 
    
- <span data-ttu-id="da0b9-118">**Пр_сеарч_кэй** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="da0b9-118">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span> 
    
<span data-ttu-id="da0b9-119">Эти свойства используются для доступа к получателю, отправки сообщений в него и сравнения с другими.</span><span class="sxs-lookup"><span data-stu-id="da0b9-119">These properties are used to access the recipient, send messages to it, and to compare it to others.</span></span> <span data-ttu-id="da0b9-120">Не все эти свойства должны быть доступны сразу.</span><span class="sxs-lookup"><span data-stu-id="da0b9-120">Not all of these properties need to be available right away.</span></span> <span data-ttu-id="da0b9-121">Вы можете сначала добавить получателя, не зная его идентификатора записи, используя процесс разрешения имен для назначения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="da0b9-121">You can add a recipient initially without knowing its entry identifier, relying on the name resolution process to assign this property.</span></span> <span data-ttu-id="da0b9-122">В некоторый момент перед отправкой сообщения вызовите [IAddrBook:: ресолвенаме](iaddrbook-resolvename.md) , чтобы убедиться, что все получатели в списке получателей разрешены.</span><span class="sxs-lookup"><span data-stu-id="da0b9-122">At some point before you send a message, call [IAddrBook::ResolveName](iaddrbook-resolvename.md) to make sure that all of the recipients in your recipient list are resolved.</span></span> <span data-ttu-id="da0b9-123">Дополнительные сведения см. в разделе [разрешение имени получателя](resolving-a-recipient-name.md).</span><span class="sxs-lookup"><span data-stu-id="da0b9-123">For more information, see [Resolving a Recipient Name](resolving-a-recipient-name.md).</span></span>
  
<span data-ttu-id="da0b9-124">Списки получателей можно создавать из записей "пользователи системы обмена сообщениями" или "список рассылки" в контейнере адресной книги или из одного из них.</span><span class="sxs-lookup"><span data-stu-id="da0b9-124">Recipient lists can be created from messaging users or distribution list entries in an address book container or from one-offs.</span></span> <span data-ttu-id="da0b9-125">Один из них — это получатели, которые создаются как временные записи, которые будут использоваться только для адресации одного сообщения или записи, добавляемые в личную адресную книгу.</span><span class="sxs-lookup"><span data-stu-id="da0b9-125">One-offs are recipients that are created either as temporary entries to be used only for addressing a single message or as entries to be added to a personal address book.</span></span> <span data-ttu-id="da0b9-126">Формат для одноразового идентификатора записи и адреса определяется MAPI.</span><span class="sxs-lookup"><span data-stu-id="da0b9-126">The format for a one-off entry identifier and address is defined by MAPI.</span></span> <span data-ttu-id="da0b9-127">Дополнительные сведения об этих форматах приведены в статье [одноразовЫе адреса](one-off-addresses.md) и [одноразовЫе идентификаторы записей](one-off-entry-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="da0b9-127">For more information about these formats, see [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).</span></span>
  
<span data-ttu-id="da0b9-128">Вы можете разрешить пользователям создавать свои списки получателей:</span><span class="sxs-lookup"><span data-stu-id="da0b9-128">You can enable users to build their recipient lists:</span></span>
  
- <span data-ttu-id="da0b9-129">Только с записями из адресной книги.</span><span class="sxs-lookup"><span data-stu-id="da0b9-129">Only with entries from the address book.</span></span>
    
- <span data-ttu-id="da0b9-130">Только с одноразовыми записями.</span><span class="sxs-lookup"><span data-stu-id="da0b9-130">Only with one-off entries.</span></span>
    
- <span data-ttu-id="da0b9-131">С помощью сочетаний получателей адресной книги и односторонней.</span><span class="sxs-lookup"><span data-stu-id="da0b9-131">With a combination of address book recipients and one-offs.</span></span>
    
 <span data-ttu-id="da0b9-132">**Создание списка получателей с помощью диалогового окна "общий адрес"**</span><span class="sxs-lookup"><span data-stu-id="da0b9-132">**To create a recipient list using the common address dialog box**</span></span>
  
1. <span data-ttu-id="da0b9-133">Выделение структуры [адрпарм](adrparm.md) и указателя на структуру [ADRLIST](adrlist.md) .</span><span class="sxs-lookup"><span data-stu-id="da0b9-133">Allocate an [ADRPARM](adrparm.md) structure and a pointer to an [ADRLIST](adrlist.md) structure.</span></span> 
    
2. <span data-ttu-id="da0b9-134">Обнуление памяти в структуре **адрпарм** и присвойте указателю **ADRLIST** значение null.</span><span class="sxs-lookup"><span data-stu-id="da0b9-134">Zero the memory in the **ADRPARM** structure and set the **ADRLIST** pointer to NULL.</span></span> 
    
3. <span data-ttu-id="da0b9-135">Call [IAddrBook:: Address](iaddrbook-address.md) для отображения диалогового окна адрес и заполнения структуры **адрпарм** .</span><span class="sxs-lookup"><span data-stu-id="da0b9-135">Call [IAddrBook::Address](iaddrbook-address.md) to display the address dialog box and populate the **ADRPARM** structure.</span></span> 
    
4. <span data-ttu-id="da0b9-136">Call [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md), передавая указатель **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="da0b9-136">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passing the **ADRLIST** pointer.</span></span> <span data-ttu-id="da0b9-137">Эта структура будет содержать свойства каждого получателя, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="da0b9-137">This structure will contain the properties of each of the recipients selected by the user.</span></span> 
    
 <span data-ttu-id="da0b9-138">**Порядок создания списка получателей программным способом**</span><span class="sxs-lookup"><span data-stu-id="da0b9-138">**To create a recipient list programmatically**</span></span>
  
1. <span data-ttu-id="da0b9-139">Выделить структуру **ADRLIST** , содержащую одну структуру [адрентри](adrentry.md) для каждого из получателей, которые должны быть включены в список.</span><span class="sxs-lookup"><span data-stu-id="da0b9-139">Allocate an **ADRLIST** structure that contains one [ADRENTRY](adrentry.md) structure for each of the recipients to be included in the list.</span></span> <span data-ttu-id="da0b9-140">Сделайте каждую структуру **адрентри** достаточно большой для хранения всех обязательных свойств и **пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da0b9-140">Make each **ADRENTRY** structure large enough to hold each of the required properties and **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="da0b9-141">Для каждого получателя задайте массив значений свойства для элемента **аентриес** в структуре **ADRLIST** .</span><span class="sxs-lookup"><span data-stu-id="da0b9-141">For each recipient, set the property value array for its **aEntries** member in the **ADRLIST** structure.</span></span> 
    
3. <span data-ttu-id="da0b9-142">Call [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) с установленным флагом модреЦип_адд.</span><span class="sxs-lookup"><span data-stu-id="da0b9-142">Call [IMessage::ModifyRecipients](imessage-modifyrecipients.md) with the MODRECIP_ADD flag set.</span></span> 
    

