---
title: Добавление службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6a8b0f8fc8c296fe4022ac28623b83d270472ca3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590696"
---
# <a name="adding-a-message-service"></a>Добавление службы сообщений

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
 **Добавление новой службы сообщений в профиль и доступ к новой службы сообщений**
  
Вызов [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** выполняет следующие задачи: 
  
1. Копирует все соответствующие сведения для службы сообщений, которая находится в файл Mapisvc.inf. INF-файл, создание раздела профиля для каждого раздела поставщика.
    
2. Вызывает функцию точки входа для службы сообщений, **MSGSERVICEENTRY**с параметром _ulContext_ , равным MSG_SERVICE_CREATE. 
    
3. Задает и получает свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) службы сообщений.
    
 **Для доступа к службе любого добавленного сообщения**
  
1. Вызов [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) для получения таблицы службы сообщений. 
    
2. Вызов метода [IMAPITable::Advise](imapitable-advise.md) таблицы службы сообщений для регистрации уведомлений в таблице. 
    
3. Когда MAPI отправляет уведомление TABLE_ROW_ADDED, найдите идентификатор записи службы новые сообщения в структуре [SRow](srow.md) в структуре [TABLE_NOTIFICATION](table_notification.md) . 
    

