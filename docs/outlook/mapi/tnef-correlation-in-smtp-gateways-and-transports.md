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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413670"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="b2082-103">Корреляция TNEF в шлюзах и транспортах SMTP</span><span class="sxs-lookup"><span data-stu-id="b2082-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="b2082-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2082-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2082-105">Шлюзы и транспортные средства, подключенные к системам, основанным на Интернете, которые используют  SMTP, используют значение загона SMTP MessageID и свойства PR_TNEF_CORRELATION_KEY для реализации корреляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="b2082-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="b2082-106">Значение заголовка MessageID исходящие сообщения следует **скопировать** в свойство [PR_TNEF_CORRELATION_KEY (PidTagTnefCorrelationKey)](pidtagtnefcorrelationkey-canonical-property.md)и закодировать в атрибут [attMAPIProps](attmapiprops.md) потока TNEF.</span><span class="sxs-lookup"><span data-stu-id="b2082-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="b2082-107">Обратите **внимание, PR_TNEF_CORRELATION_KEY** является двоичным свойством, а MessageID — строкой; терминатор null должен быть включен в копию и сравнение.</span><span class="sxs-lookup"><span data-stu-id="b2082-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="b2082-108">Этот метод используется всем программным обеспечением Майкрософт, которое подключает системы обмена сообщениями на основе MAPI к Интернету, например Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="b2082-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="b2082-109">Этот метод следует использовать любым шлюзам SMTP и транспортным средствам, подключенным к системам, поддерживаюным клиенты MAPI, для максимальной интероперабельности.</span><span class="sxs-lookup"><span data-stu-id="b2082-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

