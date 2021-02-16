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
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432536"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет поставщику транспорта доступ к пулу MAPI. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapispi.h  <br/> |
|Выставим:  <br/> |Транспортные объекты для логотипа  <br/> |
|Реализовано в:  <br/> |Поставщики транспорта  <br/> |
|Вызывающая сторона:  <br/> |Пулер MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IXPLogon  <br/> |
|Тип указателя:  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Возвращает типы получателей, обрабатываемого поставщиком транспорта.  <br/> |
|**RegisterOptions** <br/> | *Не поддерживается и не документируется.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Сигнализирует о возникновении события, о котором поставщик транспорта запросил уведомление.  <br/> |
|[Бездействие](ixplogon-idle.md) <br/> |Указывает, что система простаивает, что позволяет поставщику транспорта выполнять операции с низким приоритетом.  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Инициирует процесс выйдите из нее.  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Указывает, что у пула MAPI есть сообщение, которое должен доставить поставщик транспорта.  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |Сообщает поставщику транспорта, что пул MAPI завершил обработку исходящие сообщения.  <br/> |
|[Опрос](ixplogon-poll.md) <br/> |Указывает, получил ли поставщик транспорта одно или несколько входящие сообщения.  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |Инициирует передачу входящие сообщения от поставщика транспорта в пулер MAPI.  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Открывает объект состояния поставщика транспорта.  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |Проверяет внешнее состояние поставщика транспорта.  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Запрашивает у поставщика транспорта немедленно доставить все ожидающих входящие или исходящие сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

