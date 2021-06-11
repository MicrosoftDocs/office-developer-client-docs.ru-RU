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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428125"
---
# <a name="deleting-a-message-service"></a>Удаление службы сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Удаление службы сообщений из профиля**
  
1. Вызов **IMAPISession::GetMsgServiceTable для** доступа к таблице службы сообщений. 
    
2. Найдите строку для службы сообщений **и передайте** столбец [PR_SERVICE_UID (PidTagServiceUid)](pidtagserviceuid-canonical-property.md)в параметре  _lpuid_ [в IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** вызывает функцию точки входа службы сообщений с параметром  _ulContext,_ MSG_SERVICE_DELETE. Службы сообщений выполняют все задачи по очистке перед удалением из профиля. 
  

