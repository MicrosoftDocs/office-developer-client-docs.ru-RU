---
title: Таблицы получателей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812099"
---
# <a name="recipient-tables"></a><span data-ttu-id="c544f-103">Таблицы получателей</span><span class="sxs-lookup"><span data-stu-id="c544f-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="c544f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c544f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c544f-105">Получателей таблица содержит сведения о всех получателей сообщения.</span><span class="sxs-lookup"><span data-stu-id="c544f-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="c544f-106">Поставщики хранилища сообщений реализации получателей таблиц и их использования для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="c544f-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="c544f-107">Клиенты получить доступ к таблице получателей, вызвав метод [IMessage::GetRecipientTable](imessage-getrecipienttable.md) или если поставщик хранилища сообщения его поддерживает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="c544f-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="c544f-108">Для доступа клиентов к получателей таблицы с **OpenProperty** путем указания для свойства tag и IID_IMAPITable **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) для идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="c544f-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="c544f-109">Путем вызова метода [IMessage::ModifyRecipients](imessage-modifyrecipients.md) можно внесены изменения в таблицу получателей.</span><span class="sxs-lookup"><span data-stu-id="c544f-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="c544f-110">Получателей таблицы имеют набор в зависимости от того, является ли сообщение отправлено различных столбцов.</span><span class="sxs-lookup"><span data-stu-id="c544f-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="c544f-111">Следующие свойства составляют обязательный столбец, задайте в таблицах получателей:</span><span class="sxs-lookup"><span data-stu-id="c544f-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="c544f-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c544f-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="c544f-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c544f-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="c544f-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c544f-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="c544f-115">Необязательный условий.</span><span class="sxs-lookup"><span data-stu-id="c544f-115">The optional properties are:</span></span>
  
- <span data-ttu-id="c544f-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c544f-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="c544f-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c544f-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="c544f-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c544f-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="c544f-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c544f-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="c544f-120">Отправленных сообщений должен включать дополнительные свойства в их набор необходимых столбцов:</span><span class="sxs-lookup"><span data-stu-id="c544f-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="c544f-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c544f-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="c544f-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c544f-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="c544f-123">В зависимости от реализации поставщика для дополнительных столбцов, такие как **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) и [ENTRYID](entryid.md), возможно, в таблице.</span><span class="sxs-lookup"><span data-stu-id="c544f-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="c544f-124">Любой поставщика хранилища сообщений, поддерживающего передачи сообщений — как указано в STORE_SUBMIT_OK бит в свойстве поставщика **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) — следует обеспечивают поддержку для определенного набора ограничения в реализации получателей в таблице.</span><span class="sxs-lookup"><span data-stu-id="c544f-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="c544f-125">**И**, **или**, существует и ограничений свойств являются между типами ограничения, которые должны быть доступны пользователям получателей в таблице.</span><span class="sxs-lookup"><span data-stu-id="c544f-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="c544f-126">Только операторы равно и не равно должны поддерживаться в ограничении свойства.</span><span class="sxs-lookup"><span data-stu-id="c544f-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="c544f-127">Эти ограничения должны работать со следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="c544f-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="c544f-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="c544f-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="c544f-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="c544f-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="c544f-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="c544f-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="c544f-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="c544f-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="c544f-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="c544f-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c544f-133">См. также</span><span class="sxs-lookup"><span data-stu-id="c544f-133">See also</span></span>



[<span data-ttu-id="c544f-134">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="c544f-134">MAPI Tables</span></span>](mapi-tables.md)

