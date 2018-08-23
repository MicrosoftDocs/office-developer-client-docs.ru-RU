---
title: Корреляция TNEF в операциях транспорта и шлюзах SMTP
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8192646007e8935a750a70e46b8210eebbc353f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578537"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="4321b-103">Корреляция TNEF в операциях транспорта и шлюзах SMTP</span><span class="sxs-lookup"><span data-stu-id="4321b-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="4321b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4321b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4321b-105">Шлюзы и транспортов, подключение к Интернету, используя систем, те, которые использовать SMTP, используйте значение заголовка SMTP код (ID) и свойство **PR_TNEF_CORRELATION_KEY** для реализации корреляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="4321b-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="4321b-106">Значение заголовка сообщения, исходящие сообщения следует скопировать в свойство **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) и кодируются в атрибуте [attMAPIProps](attmapiprops.md) поток TNEF.</span><span class="sxs-lookup"><span data-stu-id="4321b-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="4321b-107">Обратите внимание, что **PR_TNEF_CORRELATION_KEY** двоичного свойства, а код (ID) — это строка; нулевым кодом конца строки должны быть включены в эту копию, а также для сравнения.</span><span class="sxs-lookup"><span data-stu-id="4321b-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="4321b-108">Этот метод используется программное обеспечение Майкрософт, который подключается к Интернету, например, Microsoft Exchange Server на основе MAPI систем обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="4321b-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="4321b-109">Этот метод можно использовать с любой шлюзов SMTP и транспортов, которые подключаются к системам, которые поддерживают клиентов MAPI для обеспечения максимальной взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="4321b-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

