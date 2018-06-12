---
title: Добавление службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: a7735be5cfb8ff0716b6bd6eba4951563bb938ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808003"
---
# <a name="adding-a-message-service"></a>Добавление службы сообщений

  
  
**Применимо к**: Outlook 
  
 **Добавление новой службы сообщений в профиль и доступ к новой службы сообщений**
  
Вызов [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** выполняет следующие задачи: 
  
1. Копирует все соответствующие сведения для службы сообщений, которая находится в файл Mapisvc.inf. INF-файл, создание раздела профиля для каждого раздела поставщика.
    
2. Вызывает функцию точки входа для службы сообщений, **MSGSERVICEENTRY**с параметром _ulContext_ , равным MSG_SERVICE_CREATE. 
    
3. Задает и получает свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) службы сообщений.
    
 **Для доступа к службе любого добавленного сообщения**
  
1. Вызов [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) для получения таблицы службы сообщений. 
    
2. Вызов метода [IMAPITable::Advise](imapitable-advise.md) таблицы службы сообщений для регистрации уведомлений в таблице. 
    
3. Когда MAPI отправляет уведомление TABLE_ROW_ADDED, найдите идентификатор записи службы новые сообщения в структуре [SRow](srow.md) в структуре [TABLE_NOTIFICATION](table_notification.md) . 
    

