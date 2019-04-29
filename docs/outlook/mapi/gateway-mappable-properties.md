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
# <a name="gateway-mappable-properties"></a><span data-ttu-id="89e61-103">Свойства, сопоставляемые со шлюзами</span><span class="sxs-lookup"><span data-stu-id="89e61-103">Gateway mappable properties</span></span>

<span data-ttu-id="89e61-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89e61-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89e61-105">Gateway — свойства сопоставляемые со — это свойства, которые могут требовать преобразования при отправке из одного домена обмена сообщениями на другой.</span><span class="sxs-lookup"><span data-stu-id="89e61-105">Gateway-mappable properties are properties that may require translation when sent from one messaging domain to another.</span></span> <span data-ttu-id="89e61-106">Свойства шлюза MAPI — сопоставляемые со позволяют сообщениям включать сведения, требующие шлюза, чтобы обеспечить правильную работу конечной системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="89e61-106">MAPI's gateway-mappable properties enable messages to include information that requires a gateway to ensure the destination messaging system uses it properly.</span></span> <span data-ttu-id="89e61-107">Несмотря на то, что разработчикам шлюза не требуется предоставлять эту возможность, они должны рассмотреть свойства Gateway – сопоставляемые со в качестве возможности для оптимизации обработки содержимого сообщений.</span><span class="sxs-lookup"><span data-stu-id="89e61-107">Although gateway developers are not required to provide this translation capability, they should consider gateway-mappable properties as an opportunity to improve handling of message content.</span></span>
  
<span data-ttu-id="89e61-108">MAPI определяет пять типов свойств Gateway — сопоставляемые со:</span><span class="sxs-lookup"><span data-stu-id="89e61-108">MAPI specifies five types of gateway-mappable properties:</span></span>
  
- <span data-ttu-id="89e61-109">Различающееся имя (DN)</span><span class="sxs-lookup"><span data-stu-id="89e61-109">Display name</span></span>
    
- <span data-ttu-id="89e61-110">Краткое имя</span><span class="sxs-lookup"><span data-stu-id="89e61-110">Email address</span></span>
    
- <span data-ttu-id="89e61-111">Тип электронной почты</span><span class="sxs-lookup"><span data-stu-id="89e61-111">Email type</span></span>
    
- <span data-ttu-id="89e61-112">Идентификатор записи</span><span class="sxs-lookup"><span data-stu-id="89e61-112">Entry identifier</span></span>
    
- <span data-ttu-id="89e61-113">Ключ поиска</span><span class="sxs-lookup"><span data-stu-id="89e61-113">Search key</span></span>
    
<span data-ttu-id="89e61-114">Это набор свойств адресации, связанных с получателями, отправителями, получателями отчетов и делегированными отправителями и получателями.</span><span class="sxs-lookup"><span data-stu-id="89e61-114">This is the set of addressing properties that are associated with recipients, senders, report recipients, and delegated senders and recipients.</span></span> <span data-ttu-id="89e61-115">Чтобы помочь клиенту определить эти свойства, чтобы шлюз обрабатывал их особым образом, MAPI указывает соглашение об именовании с использованием именованных свойств и наборов свойств.</span><span class="sxs-lookup"><span data-stu-id="89e61-115">To help your client define these properties so that a gateway handles them specially, MAPI specifies a naming convention using named properties and property sets.</span></span> <span data-ttu-id="89e61-116">Для хранения именованных свойств существует пять наборов свойств адресации, для которых требуется сопоставление.</span><span class="sxs-lookup"><span data-stu-id="89e61-116">Five property sets exist to hold named properties, the addressing properties that require mapping.</span></span> <span data-ttu-id="89e61-117">Для каждого типа свойства сопоставляемые со существует один набор свойств.</span><span class="sxs-lookup"><span data-stu-id="89e61-117">There is one property set for each type of mappable property.</span></span> <span data-ttu-id="89e61-118">Ниже указаны наборы свойств, в которых будут храниться следующие именованные свойства адресации.</span><span class="sxs-lookup"><span data-stu-id="89e61-118">The property sets that will hold these named addressing properties are as follows.</span></span>
  
|<span data-ttu-id="89e61-119">**Набор свойств**</span><span class="sxs-lookup"><span data-stu-id="89e61-119">**Property set**</span></span>|<span data-ttu-id="89e61-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="89e61-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="89e61-121">ПС_РАУТИНГ_ДИСПЛАЙ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="89e61-121">PS_ROUTING_DISPLAY_NAME</span></span>  <br/> |<span data-ttu-id="89e61-122">Содержит строковые свойства, используемые в качестве отображаемых имен.</span><span class="sxs-lookup"><span data-stu-id="89e61-122">Contains string properties used as display names.</span></span>  <br/> |
|<span data-ttu-id="89e61-123">ПС_РАУТИНГ_ЕМАИЛ_АДДРЕССЕС</span><span class="sxs-lookup"><span data-stu-id="89e61-123">PS_ROUTING_EMAIL_ADDRESSES</span></span>  <br/> |<span data-ttu-id="89e61-124">Содержит строковые свойства, используемые в качестве адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="89e61-124">Contains string properties used as email addresses.</span></span>  <br/> |
|<span data-ttu-id="89e61-125">ПС_РАУТИНГ_АДДРТИПЕ</span><span class="sxs-lookup"><span data-stu-id="89e61-125">PS_ROUTING_ADDRTYPE</span></span>  <br/> |<span data-ttu-id="89e61-126">Содержит строковые свойства, используемые в качестве типов адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="89e61-126">Contains string properties used as email address types.</span></span>  <br/> |
|<span data-ttu-id="89e61-127">ПС_РАУТИНГ_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="89e61-127">PS_ROUTING_ENTRYID</span></span>  <br/> |<span data-ttu-id="89e61-128">Содержит двоичные свойства, используемые в качестве долгосрочных идентификаторов записей.</span><span class="sxs-lookup"><span data-stu-id="89e61-128">Contains binary properties used as long-term entry identifiers.</span></span>  <br/> |
|<span data-ttu-id="89e61-129">ПС_РАУТИНГ_СЕАРЧ_КЭЙ</span><span class="sxs-lookup"><span data-stu-id="89e61-129">PS_ROUTING_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="89e61-130">Содержит двоичные свойства, используемые в качестве ключей поиска.</span><span class="sxs-lookup"><span data-stu-id="89e61-130">Contains binary properties used as search keys.</span></span>  <br/> |
   

