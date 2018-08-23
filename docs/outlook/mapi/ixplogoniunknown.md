---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ecfbf33641c86d4f162c521466ca2bf0b79a61d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581407"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ очереди MAPI для поставщика транспорта. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Предоставляемые:  <br/> |Объекты входа транспорта  <br/> |
|Реализованный:  <br/> |Поставщиками транспорта  <br/> |
|Вызывается:  <br/> |Диспетчер очереди MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IXPLogon  <br/> |
|Тип указателя:  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Возвращает типы получателей, которые обрабатывают поставщика транспорта.  <br/> |
|**RegisterOptions** <br/> | *Не поддерживается, документированных.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Указывает на возникновение события, о том, какие поставщика транспорта запрошено уведомление.  <br/> |
|[Простоя](ixplogon-idle.md) <br/> |Указывает, что система не занята, включив поставщика транспорта для выполнения операций с низким приоритетом.  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Запускает процесс выхода из системы.  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Указывает, что диспетчер очереди MAPI для поставщика транспорта для доставки сообщения.  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |Информирует поставщика транспорта, что диспетчер очереди MAPI завершения обработки на исходящее сообщение.  <br/> |
|[Опрос](ixplogon-poll.md) <br/> |Указывает, поставщика транспорта, полученных одного или нескольких входящих сообщений.  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |Инициирует передачи входящих сообщений от поставщика транспорта диспетчер очереди MAPI.  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Открывает объект состояние поставщика транспорта.  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |Проверяет состояние внешних поставщика транспорта.  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Запросы, что поставщик транспорта сразу же доставить все ожидающие входящих или исходящих сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

