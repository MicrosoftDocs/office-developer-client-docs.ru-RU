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
ms.openlocfilehash: ec1d826ee2b3b46685a2c03dfaf45d2843869cc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812490"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a>Корреляция TNEF в операциях транспорта и шлюзах SMTP

  
  
**Относится к**: Outlook 
  
Шлюзы и транспортов, подключение к Интернету, используя систем, те, которые использовать SMTP, используйте значение заголовка SMTP код (ID) и свойство **PR_TNEF_CORRELATION_KEY** для реализации корреляции TNEF. 
  
Значение заголовка сообщения, исходящие сообщения следует скопировать в свойство **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) и кодируются в атрибуте [attMAPIProps](attmapiprops.md) поток TNEF. Обратите внимание, что **PR_TNEF_CORRELATION_KEY** двоичного свойства, а код (ID) — это строка; нулевым кодом конца строки должны быть включены в эту копию, а также для сравнения. 
  
Этот метод используется программное обеспечение Майкрософт, который подключается к Интернету, например, Microsoft Exchange Server на основе MAPI систем обмена сообщениями. Этот метод можно использовать с любой шлюзов SMTP и транспортов, которые подключаются к системам, которые поддерживают клиентов MAPI для обеспечения максимальной взаимодействия.
  

