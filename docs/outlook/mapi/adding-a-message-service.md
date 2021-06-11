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
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407237"
---
# <a name="adding-a-message-service"></a>Добавление службы сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Добавление новой службы сообщений в профиль и доступ к новой службе сообщений**
  
Вызов [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx выполняет** следующие задачи: 
  
1. Копирует всю соответствующую информацию для службы сообщений, которая находится в MAPISVC. Файл INF, создав раздел профилей для каждого раздела поставщика.
    
2. Вызывает функцию точки входа службы сообщений **MSGSERVICEENTRY** с параметром  _ulContext,_ заданным MSG_SERVICE_CREATE. 
    
3. Задает и извлекает свойство PR_SERVICE_UID **службы** сообщений [(PidTagServiceUid).](pidtagserviceuid-canonical-property.md)
    
 **Доступ к новой службе сообщений**
  
1. Позвоните [в службу IMsgServiceAdmin::GetMsgServiceTable,](imsgserviceadmin-getmsgservicetable.md) чтобы получить таблицу службы сообщений. 
    
2. Вызов метода [IMAPITable::Advise](imapitable-advise.md) таблицы службы сообщений для регистрации уведомлений таблицы. 
    
3. При отправке уведомления TABLE_ROW_ADDED MAPI найдите идентификатор записи недавно добавленной службы сообщений в структуре [SRow,](srow.md) [включенной в структуру TABLE_NOTIFICATION.](table_notification.md) 
    

