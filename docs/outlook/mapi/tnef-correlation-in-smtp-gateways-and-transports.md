---
title: Корреляция TNEF в шлюзах и транспортных системах SMTP
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
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Корреляция TNEF в шлюзах и транспортных системах SMTP

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Шлюзы и транспортные средства, которые подключаются к интернет-системам, которые используют SMTP, используют значение SMTP-загона MessageID и **свойство PR_TNEF_CORRELATION_KEY** для реализации корреляции TNEF. 
  
Значение заголовщика MessageID исходящие сообщения следует скопировать в свойство **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey)](pidtagtnefcorrelationkey-canonical-property.md)и закодировать в [атрибуте attMAPIProps](attmapiprops.md) потока TNEF. Обратите **внимание PR_TNEF_CORRELATION_KEY** что это двоичное свойство, а MessageID — строка; В копию и сравнение должно быть включено терминатор null. 
  
Этот метод используется всем программным обеспечением Майкрософт, которое подключает системы обмена сообщениями на основе MAPI к Интернету, например Microsoft Exchange Server. Этот способ должен использоваться любыми шлюзами и транспортными средствами SMTP, которые подключаются к системам, которые поддерживают клиенты MAPI, для максимального обеспечения максимальной производительности.
  

