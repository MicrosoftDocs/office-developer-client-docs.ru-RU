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
ms.openlocfilehash: 140fe97662f7a2ce68c18d8e0eb991d0819da6dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808540"
---
# <a name="handling-a-transport-provider"></a>Обработка поставщика транспорта
  
**Относится к**: Outlook 
  
Клиенты связываться с поставщиками транспорта через объекты состояния, предоставляемые поставщиками транспорта и диспетчер очереди MAPI. Клиенты доступа к объектам состояние путем вызова [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для получения таблицы состояния. Объекты состояния реализовать [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейс, который содержит методы для настройки поставщиков, очистки входящих и исходящих сообщений очереди, установка паролей и проверки состояния. Дополнительные сведения о состоянии объекты можно [таблице состояния и состояния объектов](status-table-and-status-objects.md).


- [Отправки и получения сообщений по требованию](sending-or-receiving-a-message-on-demand.md): описывается, как отправлять и получать сообщения по запросу.
    
- [Параметр транспорта заказа](setting-transport-order.md): описывается, как установить порядок транспорта.
    
- [Перенастройка поставщика транспорта](reconfiguring-a-transport-provider.md): описание повторно настройте поставщика транспорта и какие свойства доступны для установки.
    

