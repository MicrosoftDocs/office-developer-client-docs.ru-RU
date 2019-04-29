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
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Клиенты взаимодействуют с поставщиками транспорта через объекты состояния, предоставляемые поставщиками транспорта и диспетчером очереди MAPI. Клиенты получают доступ к объектам состояния, вызывая [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для получения таблицы Status. Объекты Status реализуют интерфейс [имапистатус: IMAPIProp](imapistatusimapiprop.md) , который содержит методы для настройки поставщиков, очистки входящих и исходящих очередей сообщений, установки паролей и проверки состояния. Для получения дополнительных сведений об объектах состояния просмотрите [объекты состояния таблица и состояние](status-table-and-status-objects.md).


- [Отправка или получение сообщения по запросу](sending-or-receiving-a-message-on-demand.md): сведения о том, как отправлять или получать сообщение по запросу.
    
- [Установка заказа](setting-transport-order.md)на транспортировку: в этой статье описывается, как задать транспортный заказ.
    
- Повторная [Настройка поставщика транспорта](reconfiguring-a-transport-provider.md): в этой статье описывается порядок изменения конфигурации поставщика транспорта и свойств, доступных для установки.
    

