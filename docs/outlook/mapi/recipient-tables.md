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
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437289"
---
# <a name="recipient-tables"></a><span data-ttu-id="db04e-103">Таблицы получателей</span><span class="sxs-lookup"><span data-stu-id="db04e-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="db04e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db04e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db04e-105">Таблица получателей содержит сведения обо всех получателях сообщения.</span><span class="sxs-lookup"><span data-stu-id="db04e-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="db04e-106">Поставщики store сообщений реализуют таблицы получателей, а клиентские приложения используют их.</span><span class="sxs-lookup"><span data-stu-id="db04e-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="db04e-107">Клиенты получают доступ к таблице получателей, звоня [методу IMessage::GetRecipientTable](imessage-getrecipienttable.md) или, если поставщик хранимых сообщений поддерживает ее, [методУ IMAPIProp::OpenProperty.](imapiprop-openproperty.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="db04e-108">Клиенты имеют доступ к таблицам  получателей с помощью **OpenProperty,** указав PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)для тега свойства и IID_IMAPITable для идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="db04e-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="db04e-109">Изменения таблицы получателей можно внести с помощью вызова метода [IMessage::ModifyRecipients.](imessage-modifyrecipients.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="db04e-110">Таблицы получателей имеют другой набор столбцов в зависимости от того, было ли сообщение отправлено.</span><span class="sxs-lookup"><span data-stu-id="db04e-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="db04e-111">Следующие свойства составляют необходимый набор столбцов в таблицах получателей:</span><span class="sxs-lookup"><span data-stu-id="db04e-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="db04e-112">**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="db04e-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType)](pidtagrecipienttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="db04e-114">**PR_ROWID** ([PidTagRowid)](pidtagrowid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="db04e-115">Дополнительные свойства:</span><span class="sxs-lookup"><span data-stu-id="db04e-115">The optional properties are:</span></span>
  
- <span data-ttu-id="db04e-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="db04e-117">**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="db04e-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus)](pidtagspoolerstatus-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="db04e-119">**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="db04e-120">Отправленные сообщения должны включать следующие дополнительные свойства в требуемом наборе столбцов:</span><span class="sxs-lookup"><span data-stu-id="db04e-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="db04e-121">**PR_ADDRTYPE** ([PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="db04e-122">**PR_RESPONSIBILITY** ([PidTagResponsibility)](pidtagresponsibility-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="db04e-123">В зависимости от реализации поставщика в таблице могут быть дополнительные столбцы, например **PR_SENDER_NAME** [(PidTagSenderName)](pidtagsendername-canonical-property.md)и [ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="db04e-124">Любой поставщик хранилищ сообщений, который поддерживает передачу сообщений ( как указано в бите STORE_SUBMIT_OK, задаваемом в свойстве **PR_STORE_SUPPORT_MASK** поставщика [(PidTagStoreSupportMask),](pidtagstoresupportmask-canonical-property.md)должен поддерживать определенный набор ограничений в реализации таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="db04e-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="db04e-125">Ограничения **AND**, **OR**, существуют и ограничения свойств являются одними из типов ограничений, которые должны быть доступны для пользователей таблиц получателей.</span><span class="sxs-lookup"><span data-stu-id="db04e-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="db04e-126">Ограничение свойств должно поддерживать только операторы "равное" и "не равное".</span><span class="sxs-lookup"><span data-stu-id="db04e-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="db04e-127">Эти ограничения должны работать со следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="db04e-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="db04e-128">**PR_ADDRTYPE**</span><span class="sxs-lookup"><span data-stu-id="db04e-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="db04e-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="db04e-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="db04e-130">**PR_RECIPIENT_TYPE**</span><span class="sxs-lookup"><span data-stu-id="db04e-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="db04e-131">**PR_RESPONSIBILITY**</span><span class="sxs-lookup"><span data-stu-id="db04e-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="db04e-132">**PR_SPOOLER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="db04e-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db04e-133">См. также</span><span class="sxs-lookup"><span data-stu-id="db04e-133">See also</span></span>



[<span data-ttu-id="db04e-134">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="db04e-134">MAPI Tables</span></span>](mapi-tables.md)

