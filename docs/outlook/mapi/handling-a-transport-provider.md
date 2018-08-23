---
title: Обработка поставщика транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 00ae0f4be9818e0e9e4562784b4d5bf44eefe308
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567953"
---
# <a name="handling-a-transport-provider"></a>Обработка поставщика транспорта
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Клиенты связываться с поставщиками транспорта через объекты состояния, предоставляемые поставщиками транспорта и диспетчер очереди MAPI. Клиенты доступа к объектам состояние путем вызова [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для получения таблицы состояния. Объекты состояния реализовать [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейс, который содержит методы для настройки поставщиков, очистки входящих и исходящих сообщений очереди, установка паролей и проверки состояния. Дополнительные сведения о состоянии объекты можно [таблице состояния и состояния объектов](status-table-and-status-objects.md).


- [Отправки и получения сообщений по требованию](sending-or-receiving-a-message-on-demand.md): описывается, как отправлять и получать сообщения по запросу.
    
- [Параметр транспорта заказа](setting-transport-order.md): описывается, как установить порядок транспорта.
    
- [Перенастройка поставщика транспорта](reconfiguring-a-transport-provider.md): описание повторно настройте поставщика транспорта и какие свойства доступны для установки.
    

