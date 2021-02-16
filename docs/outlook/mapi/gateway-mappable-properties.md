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
# <a name="gateway-mappable-properties"></a><span data-ttu-id="f866f-103">Свойства, сопоставляемые со шлюзами</span><span class="sxs-lookup"><span data-stu-id="f866f-103">Gateway mappable properties</span></span>

<span data-ttu-id="f866f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f866f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f866f-105">Свойства, которые можно использовать для приложения шлюза, — это свойства, которые могут требовать перевода при отправке из одного домена обмена сообщениями в другой.</span><span class="sxs-lookup"><span data-stu-id="f866f-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="f866f-106">Свойства MAPI, которые можно использовать для применения шлюза, позволяют сообщениям включать сведения, которые требуют шлюза для правильного использования системой обмена сообщениями назначения.</span><span class="sxs-lookup"><span data-stu-id="f866f-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="f866f-107">Хотя разработчики шлюзов не обязаны предоставлять эту возможность перевода, им следует рассмотреть свойства, которые можно использовать в качестве возможности для улучшения обработки содержимого сообщений.</span><span class="sxs-lookup"><span data-stu-id="f866f-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="f866f-108">MAPI указывает пять типов свойств, которые можно примесить шлюзу:</span><span class="sxs-lookup"><span data-stu-id="f866f-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="f866f-109">Различающееся имя (DN)</span><span class="sxs-lookup"><span data-stu-id="f866f-109">Display name</span></span>
    
- <span data-ttu-id="f866f-110">Краткое имя</span><span class="sxs-lookup"><span data-stu-id="f866f-110">Email address</span></span>
    
- <span data-ttu-id="f866f-111">Тип электронной почты</span><span class="sxs-lookup"><span data-stu-id="f866f-111">Email type</span></span>
    
- <span data-ttu-id="f866f-112">Идентификатор записи</span><span class="sxs-lookup"><span data-stu-id="f866f-112">Entry identifier</span></span>
    
- <span data-ttu-id="f866f-113">Ключ поиска</span><span class="sxs-lookup"><span data-stu-id="f866f-113">Search key</span></span>
    
<span data-ttu-id="f866f-114">Это набор свойств адресов, связанных с получателями, отправителями, получателями отчетов, а также делегными отправителями и получателями.</span><span class="sxs-lookup"><span data-stu-id="f866f-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="f866f-115">Чтобы клиент определял эти свойства, чтобы шлюз обрабатывал их специально, MAPI задает соглашение об именовке с использованием именующих свойств и наборов свойств.</span><span class="sxs-lookup"><span data-stu-id="f866f-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="f866f-116">Существует пять наборов свойств для удержания именуемой свойства, которые требуют сопоставления.</span><span class="sxs-lookup"><span data-stu-id="f866f-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="f866f-117">Существует один набор свойств для каждого типа свойства, к который можно приместить.</span><span class="sxs-lookup"><span data-stu-id="f866f-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="f866f-118">Наборы свойств, в которые будут вметься эти именуемые свойства адресов, следуют указанным образом.</span><span class="sxs-lookup"><span data-stu-id="f866f-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="f866f-119">**Набор свойств**</span><span class="sxs-lookup"><span data-stu-id="f866f-119">**Property set**</span></span>|<span data-ttu-id="f866f-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f866f-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f866f-121">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="f866f-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="f866f-122">Содержит строки свойства, используемые в качестве отображаемой имена.</span><span class="sxs-lookup"><span data-stu-id="f866f-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="f866f-123">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="f866f-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="f866f-124">Содержит строку свойств, используемых в качестве адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f866f-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="f866f-125">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="f866f-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="f866f-126">Содержит строку свойств, используемых в качестве типов адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="f866f-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="f866f-127">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="f866f-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="f866f-128">Содержит двоичные свойства, используемые в качестве долгосрочных идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="f866f-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="f866f-129">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="f866f-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="f866f-130">Содержит двоичные свойства, используемые в качестве ключей поиска.</span><span class="sxs-lookup"><span data-stu-id="f866f-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

