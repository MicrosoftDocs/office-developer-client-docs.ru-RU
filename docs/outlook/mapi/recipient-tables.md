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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328422"
---
# <a name="recipient-tables"></a><span data-ttu-id="acea8-103">Таблицы получателей</span><span class="sxs-lookup"><span data-stu-id="acea8-103">Recipient Tables</span></span>

  
  
<span data-ttu-id="acea8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acea8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acea8-105">Таблица Recipient содержит сведения обо всех получателях сообщения.</span><span class="sxs-lookup"><span data-stu-id="acea8-105">The recipient table contains information about all the recipients for a message.</span></span> <span data-ttu-id="acea8-106">Поставщики хранилищ сообщений реализуют таблицы получателей, а клиентские приложения используют их.</span><span class="sxs-lookup"><span data-stu-id="acea8-106">Message store providers implement recipient tables and client applications use them.</span></span> <span data-ttu-id="acea8-107">Клиенты обращаются к таблице получателей, выполнив вызов метода [iMessage:: жетреЦипиенттабле](imessage-getrecipienttable.md) , или если поставщик хранилища сообщений поддерживает его, в метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="acea8-107">Clients access a recipient table by making a call to the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, or if the message store provider supports it, to the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="acea8-108">Клиенты обращаются к таблицам получателей с помощью **опенпроперти** , указывая **пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) для тега свойства и иид_имапитабле для идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="acea8-108">Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier.</span></span> <span data-ttu-id="acea8-109">Изменения в таблице получателей можно выполнить, вызвав метод [iMessage:: модифиреЦипиентс](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="acea8-109">Changes to a recipient table can be made by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> 
  
<span data-ttu-id="acea8-110">Таблицы получателей имеют разный набор столбцов в зависимости от того, было ли отправлено сообщение.</span><span class="sxs-lookup"><span data-stu-id="acea8-110">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="acea8-111">Следующие свойства составляют обязательный набор столбцов в таблицах получателей:</span><span class="sxs-lookup"><span data-stu-id="acea8-111">The following properties make up the required column set in recipient tables:</span></span>
  
- <span data-ttu-id="acea8-112">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acea8-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>
    
- <span data-ttu-id="acea8-113">**Пр_реЦипиент_типе** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acea8-113">**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))</span></span>
    
- <span data-ttu-id="acea8-114">**Пр_ровид** ([PidTagRowid](pidtagrowid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acea8-114">**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))</span></span>
    
<span data-ttu-id="acea8-115">Необязательные свойства:</span><span class="sxs-lookup"><span data-stu-id="acea8-115">The optional properties are:</span></span>
  
- <span data-ttu-id="acea8-116">**Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acea8-116">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>
    
- <span data-ttu-id="acea8-117">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acea8-117">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>
    
- <span data-ttu-id="acea8-118">**Пр_спулер_статус** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acea8-118">**PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))</span></span>
    
- <span data-ttu-id="acea8-119">**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acea8-119">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>
    
<span data-ttu-id="acea8-120">Отправленные сообщения должны включать следующие дополнительные свойства в требуемый набор столбцов:</span><span class="sxs-lookup"><span data-stu-id="acea8-120">Submitted messages should include these additional properties in their required column set:</span></span>
  
- <span data-ttu-id="acea8-121">**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acea8-121">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>
    
- <span data-ttu-id="acea8-122">**Пр_респонсибилити** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acea8-122">**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))</span></span>
    
<span data-ttu-id="acea8-123">В зависимости от реализации поставщика дополнительные столбцы, такие как **пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md)) и [EntryID](entryid.md), могут находиться в таблице.</span><span class="sxs-lookup"><span data-stu-id="acea8-123">Depending on a provider's implementation, additional columns, such as **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) and [ENTRYID](entryid.md), might be in the table.</span></span>
  
<span data-ttu-id="acea8-124">Любой поставщик хранилища сообщений, поддерживающий передачу сообщений, как указано в битовом СТОРЕ_СУБМИТ_ОК, заданном в свойстве **пр_сторе_суппорт_маск** поставщика ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)), должен поддерживать определенный набор ограничения в реализации таблицы получателей.</span><span class="sxs-lookup"><span data-stu-id="acea8-124">Any message store provider that supports message transmission — as indicated by the STORE_SUBMIT_OK bit being set in the provider's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property — should offer support for a particular set of restrictions in a recipient table implementation.</span></span> <span data-ttu-id="acea8-125">Ограничения " **и**", "существует" и "Свойства" относятся к типам ограничений, которые должны быть доступны для пользователей таблицы получателей. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="acea8-125">The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users.</span></span> <span data-ttu-id="acea8-126">Только операторы EQUAL и Not Equals должны поддерживаться в ограничении свойства.</span><span class="sxs-lookup"><span data-stu-id="acea8-126">Only the equal and not equal operators need to be supported on the property restriction.</span></span> <span data-ttu-id="acea8-127">Эти ограничения должны работать со следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="acea8-127">These restrictions must work with the following properties:</span></span>
  
- <span data-ttu-id="acea8-128">**ПР_АДДРТИПЕ**</span><span class="sxs-lookup"><span data-stu-id="acea8-128">**PR_ADDRTYPE**</span></span>
    
- <span data-ttu-id="acea8-129">**Пр_емаил_аддресс** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="acea8-129">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span> 
    
- <span data-ttu-id="acea8-130">**ПР_РЕЦИПИЕНТ_ТИПЕ**</span><span class="sxs-lookup"><span data-stu-id="acea8-130">**PR_RECIPIENT_TYPE**</span></span>
    
- <span data-ttu-id="acea8-131">**ПР_РЕСПОНСИБИЛИТИ**</span><span class="sxs-lookup"><span data-stu-id="acea8-131">**PR_RESPONSIBILITY**</span></span>
    
- <span data-ttu-id="acea8-132">**ПР_СПУЛЕР_СТАТУС**</span><span class="sxs-lookup"><span data-stu-id="acea8-132">**PR_SPOOLER_STATUS**</span></span>
    
## <a name="see-also"></a><span data-ttu-id="acea8-133">См. также</span><span class="sxs-lookup"><span data-stu-id="acea8-133">See also</span></span>



[<span data-ttu-id="acea8-134">Таблицы MAPI</span><span class="sxs-lookup"><span data-stu-id="acea8-134">MAPI Tables</span></span>](mapi-tables.md)

