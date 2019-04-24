---
title: Корреляция TNEF в шлюзах и транспортах SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339692"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="bc46c-103">Корреляция TNEF в шлюзах и транспортах SMTP</span><span class="sxs-lookup"><span data-stu-id="bc46c-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="bc46c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc46c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc46c-105">Шлюзы и транспорты, которые подключаются к системам на основе Интернета, использующие SMTP, используют значение заголовка SMTP SMTP и свойство **пр_тнеф_коррелатион_кэй** для реализации корреляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="bc46c-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="bc46c-106">Значение заголовка MessageID исходящего сообщения копируется в свойство **пр_тнеф_коррелатион_кэй** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) и кодируется в атрибут [аттмапипропс](attmapiprops.md) потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="bc46c-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="bc46c-107">Обратите внимание, что **пр_тнеф_коррелатион_кэй** является двоичным свойством, а MessageId — строкой; нулевой признак должен быть включен в копию и в сравнении.</span><span class="sxs-lookup"><span data-stu-id="bc46c-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="bc46c-108">Этот метод используется всеми программами Майкрософт, которые подключают системы обмена сообщениями на основе MAPI к Интернету, например Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="bc46c-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="bc46c-109">Этот метод должен использоваться любыми шлюзами SMTP и транспортами, которые подключаются к системам, поддерживающим клиентов MAPI, чтобы обеспечить максимальную совместимость.</span><span class="sxs-lookup"><span data-stu-id="bc46c-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

