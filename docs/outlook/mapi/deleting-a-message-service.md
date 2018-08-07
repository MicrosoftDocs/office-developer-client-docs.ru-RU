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
ms.openlocfilehash: 34d9d6d428f39765e739ce856f3666d07b457d52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808277"
---
# <a name="deleting-a-message-service"></a>Удаление службы сообщений

  
  
**Относится к**: Outlook 
  
 **Чтобы удалить службы сообщений из профиля**
  
1. Вызов **IMAPISession::GetMsgServiceTable** для доступа к таблице службы сообщений. 
    
2. Найдите строку для службы сообщений и передайте его столбец **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) с помощью параметра _lpuid_ [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** вызывает функцию точки входа службы сообщений вместе с параметром _ulContext_ , равным MSG_SERVICE_DELETE. Службы сообщений выполните какие-либо очистки задач, в настоящее время перед их удалением из профиля. 
  

