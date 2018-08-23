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
ms.openlocfilehash: f39f721d434f4e54cbfa5d25a3ba626858f2b13e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583570"
---
# <a name="deleting-a-message-service"></a>Удаление службы сообщений

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
 **Чтобы удалить службы сообщений из профиля**
  
1. Вызов **IMAPISession::GetMsgServiceTable** для доступа к таблице службы сообщений. 
    
2. Найдите строку для службы сообщений и передайте его столбец **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) с помощью параметра _lpuid_ [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** вызывает функцию точки входа службы сообщений вместе с параметром _ulContext_ , равным MSG_SERVICE_DELETE. Службы сообщений выполните какие-либо очистки задач, в настоящее время перед их удалением из профиля. 
  

