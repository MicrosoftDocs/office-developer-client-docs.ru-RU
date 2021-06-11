---
title: Свойства, сопоставляемые со шлюзами
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3a51ee7e-d030-4f04-915b-ff8bd351207d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6f1a399cac2adbae66dabf9383540bb089424d17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430478"
---
# <a name="gateway-mappable-properties"></a><span data-ttu-id="caf90-103">Свойства, сопоставляемые со шлюзами</span><span class="sxs-lookup"><span data-stu-id="caf90-103">Gateway mappable properties</span></span>

<span data-ttu-id="caf90-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="caf90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="caf90-105">Свойства, которые можно использовать для шлюза, — это свойства, которые могут требовать перевода при отправке из одного домена обмена сообщениями в другой.</span><span class="sxs-lookup"><span data-stu-id="caf90-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="caf90-106">Свойства MAPI, которые можно использовать с помощью шлюза, позволяют сообщениям включать сведения, которые требуют шлюза для обеспечения правильного использования системы обмена сообщениями назначения.</span><span class="sxs-lookup"><span data-stu-id="caf90-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="caf90-107">Несмотря на то, что разработчики шлюзов не обязаны предоставлять эту возможность перевода, они должны рассматривать свойства, которые можно использовать для шлюза, как возможность улучшения обработки контента сообщений.</span><span class="sxs-lookup"><span data-stu-id="caf90-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="caf90-108">MAPI указывает пять типов свойств, которые могут быть недоступны для шлюза:</span><span class="sxs-lookup"><span data-stu-id="caf90-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="caf90-109">Различающееся имя (DN)</span><span class="sxs-lookup"><span data-stu-id="caf90-109">Display name</span></span>
    
- <span data-ttu-id="caf90-110">Краткое имя</span><span class="sxs-lookup"><span data-stu-id="caf90-110">Email address</span></span>
    
- <span data-ttu-id="caf90-111">Тип электронной почты</span><span class="sxs-lookup"><span data-stu-id="caf90-111">Email type</span></span>
    
- <span data-ttu-id="caf90-112">Идентификатор входа</span><span class="sxs-lookup"><span data-stu-id="caf90-112">Entry identifier</span></span>
    
- <span data-ttu-id="caf90-113">Ключ поиска</span><span class="sxs-lookup"><span data-stu-id="caf90-113">Search key</span></span>
    
<span data-ttu-id="caf90-114">Это набор адресных свойств, связанных с получателями, отправителями, получателями отчетов и делегированием отправителей и получателей.</span><span class="sxs-lookup"><span data-stu-id="caf90-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="caf90-115">Чтобы помочь клиенту определить эти свойства, чтобы шлюз обрабатывал их специально, MAPI указывает конвенцию имен с использованием именных свойств и наборов свойств.</span><span class="sxs-lookup"><span data-stu-id="caf90-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="caf90-116">Существует пять наборов свойств для удержания именных свойств, которые требуют сопоставления.</span><span class="sxs-lookup"><span data-stu-id="caf90-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="caf90-117">Существует один набор свойств для каждого типа подавимого свойства.</span><span class="sxs-lookup"><span data-stu-id="caf90-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="caf90-118">Наборы свойств, которые будут удерживать указанные свойства адресов, следуют следующим образом.</span><span class="sxs-lookup"><span data-stu-id="caf90-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="caf90-119">**Набор свойств**</span><span class="sxs-lookup"><span data-stu-id="caf90-119">**Property set**</span></span>|<span data-ttu-id="caf90-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="caf90-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="caf90-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="caf90-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="caf90-122">Содержит свойства строки, используемые в качестве имен отображения.</span><span class="sxs-lookup"><span data-stu-id="caf90-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="caf90-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="caf90-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="caf90-124">Содержит свойства строки, используемые в качестве адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="caf90-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="caf90-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="caf90-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="caf90-126">Содержит свойства строки, используемые в качестве типов адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="caf90-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="caf90-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="caf90-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="caf90-128">Содержит двоичные свойства, используемые в качестве долгосрочных идентификаторов записи.</span><span class="sxs-lookup"><span data-stu-id="caf90-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="caf90-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="caf90-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="caf90-130">Содержит двоичные свойства, используемые в качестве ключей поиска.</span><span class="sxs-lookup"><span data-stu-id="caf90-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

