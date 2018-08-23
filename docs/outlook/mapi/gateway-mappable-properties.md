---
title: Сопоставляемые свойства шлюза
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 07c215511f010741e69c08c184df0ca3ce461e13
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583619"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="613a9-103">Сопоставляемые свойства шлюза</span><span class="sxs-lookup"><span data-stu-id="613a9-103">Gateway mappable properties</span></span>

<span data-ttu-id="613a9-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="613a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="613a9-105">Шлюз сопоставляемые свойства — это свойства, которые может потребоваться перевода при отправке из одного домена обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="613a9-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="613a9-106">Шлюз сопоставляемые свойства MAPI включите сообщения со сведениями, которому требуется шлюз, чтобы убедиться, что он используется для назначения, системы обмена сообщениями должным образом.</span><span class="sxs-lookup"><span data-stu-id="613a9-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="613a9-107">Несмотря на то, что разработчики шлюза для предоставления эту возможность перевода не требуются, они шлюза сопоставляемые свойства следует рассматривать как возможности для улучшения обработки содержимого сообщения.</span><span class="sxs-lookup"><span data-stu-id="613a9-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="613a9-108">Пять типы свойств, сопоставляемые шлюза MAPI:</span><span class="sxs-lookup"><span data-stu-id="613a9-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="613a9-109">Отображаемое имя</span><span class="sxs-lookup"><span data-stu-id="613a9-109">Display name</span></span>
    
- <span data-ttu-id="613a9-110">Адрес электронной почты</span><span class="sxs-lookup"><span data-stu-id="613a9-110">Email address</span></span>
    
- <span data-ttu-id="613a9-111">Тип сообщения электронной почты</span><span class="sxs-lookup"><span data-stu-id="613a9-111">Email type</span></span>
    
- <span data-ttu-id="613a9-112">Идентификатор записи</span><span class="sxs-lookup"><span data-stu-id="613a9-112">Entry identifier</span></span>
    
- <span data-ttu-id="613a9-113">Ключ поиска</span><span class="sxs-lookup"><span data-stu-id="613a9-113">Search key</span></span>
    
<span data-ttu-id="613a9-114">Это набор адресации свойств, которые связаны с получателей, отправителей, получателей отчетов и делегированных отправителей и получателей.</span><span class="sxs-lookup"><span data-stu-id="613a9-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="613a9-115">Чтобы определить эти свойства, чтобы шлюз обрабатывает их специально клиента, MAPI указывает соглашение об именовании, с помощью именованных свойств и наборы свойств.</span><span class="sxs-lookup"><span data-stu-id="613a9-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="613a9-116">Существует пять наборы свойств для хранения именованных свойств, адресации свойства, которые требуется сопоставить.</span><span class="sxs-lookup"><span data-stu-id="613a9-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="613a9-117">Существует одно свойство для каждого типа сопоставляемые свойства.</span><span class="sxs-lookup"><span data-stu-id="613a9-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="613a9-118">Наборы свойств, которые будут храниться эти свойства адреса с именем, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="613a9-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="613a9-119">**Набор свойств**</span><span class="sxs-lookup"><span data-stu-id="613a9-119">**Property set**</span></span>|<span data-ttu-id="613a9-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="613a9-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="613a9-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="613a9-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="613a9-122">Содержит строку свойства, используемые как отображаемые имена.</span><span class="sxs-lookup"><span data-stu-id="613a9-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="613a9-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="613a9-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="613a9-124">Содержит свойства string используется в качестве адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="613a9-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="613a9-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="613a9-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="613a9-126">Содержит строковые свойства, используемые в качестве типов адреса электронной почты.</span><span class="sxs-lookup"><span data-stu-id="613a9-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="613a9-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="613a9-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="613a9-128">Содержит двоичные свойства, используемые как долгосрочного идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="613a9-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="613a9-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="613a9-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="613a9-130">Содержит двоичные свойства, используемые в качестве ключей поиска.</span><span class="sxs-lookup"><span data-stu-id="613a9-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

