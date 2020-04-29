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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 **Добавление новой службы сообщений в профиль и доступ к новой службе сообщений**
  
Call [IMsgServiceAdmin2:: креатемсгсервицеекс](imsgserviceadmin2-createmsgserviceex.md). **Креатемсгсервицеекс** выполняет следующие задачи: 
  
1. Копирует всю необходимую информацию для службы сообщений в MAPISVC. INF-файл, создающий раздел профиля для каждого раздела поставщика.
    
2. Вызывает функцию точки входа службы сообщений, **мсгсервицеентри**, с параметром _улконтекст_ , для которого задано значение MSG_SERVICE_CREATE. 
    
3. Задает и получает свойство **PR_SERVICE_UID** службы сообщений ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)).
    
 **Доступ к недавно добавленной службе сообщений**
  
1. Call [имсгсервицеадмин:: жетмсгсервицетабле](imsgserviceadmin-getmsgservicetable.md) для получения таблицы службы сообщений. 
    
2. Вызовите для таблицы служба сообщений метод [IMAPITable:: Advise](imapitable-advise.md) для регистрации в табличных уведомлениях. 
    
3. Когда MAPI отправляет TABLE_ROW_ADDED уведомление, нахождение идентификатора записи недавно добавленной службы сообщений в структуре [сров](srow.md) , включенной в структуру [TABLE_NOTIFICATION](table_notification.md) . 
    

