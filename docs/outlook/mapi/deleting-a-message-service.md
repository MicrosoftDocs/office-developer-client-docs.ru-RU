---
title: Удаление службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316865"
---
# <a name="deleting-a-message-service"></a>Удаление службы сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Удаление службы сообщений из профиля**
  
1. Call **IMAPISession:: жетмсгсервицетабле** для доступа к таблице службы сообщений. 
    
2. Откройте строку для службы сообщений и передайте ее столбец **пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) в параметре _Лпуид_ в [имсгсервицеадмин::D елетемсгсервице](imsgserviceadmin-deletemsgservice.md). 
    
 **Делетемсгсервице** вызывает функцию точки входа службы сообщений с параметром _улконтекст_ , для которого задано значение мсг_сервице_делете. Службы сообщений перед удалением из профиля выполняют в данный момент какие – либо задачи по очистке. 
  

