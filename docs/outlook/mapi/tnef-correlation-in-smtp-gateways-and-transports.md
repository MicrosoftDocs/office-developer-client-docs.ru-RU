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
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Корреляция TNEF в шлюзах и транспортах SMTP

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Шлюзы и транспорты, которые подключаются к системам на основе Интернета, использующие протокол SMTP, используют значение заголовка SMTP протокола MessageID и свойство **PR_TNEF_CORRELATION_KEY** для реализации корреляции TNEF. 
  
Значение заголовка MessageID исходящего сообщения копируется в свойство **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) и кодируется в атрибут [аттмапипропс](attmapiprops.md) потока TNEF. Обратите внимание, что **PR_TNEF_CORRELATION_KEY** является двоичным свойством, а MessageId — строкой; нулевой признак должен быть включен в копию и в сравнении. 
  
Этот метод используется всеми программами Майкрософт, которые подключают системы обмена сообщениями на основе MAPI к Интернету, например Microsoft Exchange Server. Этот метод должен использоваться любыми шлюзами SMTP и транспортами, которые подключаются к системам, поддерживающим клиентов MAPI, чтобы обеспечить максимальную совместимость.
  

