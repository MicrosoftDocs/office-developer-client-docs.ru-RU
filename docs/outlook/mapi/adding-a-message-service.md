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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328189"
---
# <a name="adding-a-message-service"></a>Добавление службы сообщений

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 **Добавление новой службы сообщений в профиль и доступ к новой службе сообщений**
  
Call [IMsgServiceAdmin2:: креатемсгсервицеекс](imsgserviceadmin2-createmsgserviceex.md). **Креатемсгсервицеекс** выполняет следующие задачи: 
  
1. Копирует всю необходимую информацию для службы сообщений в MAPISVC. INF-файл, создающий раздел профиля для каждого раздела поставщика.
    
2. Вызывает функцию точки входа службы сообщений, **мсгсервицеентри**, с параметром _улконтекст_ , равным мсг_сервице_креате. 
    
3. Задает и получает свойство **пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) службы сообщений.
    
 **Доступ к недавно добавленной службе сообщений**
  
1. Call [имсгсервицеадмин:: жетмсгсервицетабле](imsgserviceadmin-getmsgservicetable.md) для получения таблицы службы сообщений. 
    
2. ВыЗовите для таблицы служба сообщений метод [IMAPITable:: Advise](imapitable-advise.md) для регистрации в табличных уведомлениях. 
    
3. Когда MAPI отправляет уведомление ТАБЛЕ_РОВ_АДДЕД, нахождение идентификатора записи недавно добавленной службы сообщений в структуре [сров](srow.md) , включенной в структуру [табле_нотификатион](table_notification.md) . 
    

