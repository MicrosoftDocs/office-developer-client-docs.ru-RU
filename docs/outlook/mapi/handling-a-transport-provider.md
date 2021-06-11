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
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416540"
---
# <a name="handling-a-transport-provider"></a>Обработка поставщика транспорта
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Клиенты общаются с поставщиками транспорта через объекты состояния, предоставленные поставщиками транспорта, и спулером MAPI. Клиенты получают доступ к объектам состояния, вызывая [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для получения таблицы состояния. Объекты status реализуют интерфейс [IMAPIStatus: IMAPIProp,](imapistatusimapiprop.md) который имеет методы настройки поставщиков, очистки очередей входящих и исходяющих сообщений, установки паролей и проверки состояния. Дополнительные сведения об объектах состояния см. в [таблице status Table и Status Objects.](status-table-and-status-objects.md)


- [Отправка или получение сообщения по запросу.](sending-or-receiving-a-message-on-demand.md)Описывает, как отправлять или получать сообщение по запросу.
    
- [Настройка транспортного порядка](setting-transport-order.md). Описывает, как наказать порядок транспорта.
    
- [Перенастройка](reconfiguring-a-transport-provider.md)поставщика транспорта. Описывает, как перенастроить поставщика транспорта и какие свойства можно задать.
    

