---
title: Имапимессажесите IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433369"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Управляет сообщениями и реализуется с помощью кода средства просмотра форм (как правило, клиентского приложения), который отвечает на такую манипуляцию.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
|Предоставлено:  <br/> |Объекты сайта сообщений  <br/> |
|Реализовано в:  <br/> |Средства просмотра форм  <br/> |
|Вызывающая сторона:  <br/> |Объекты форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIMessageSite  <br/> |
|Тип указателя:  <br/> |лпмапимессажесите  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Сеансы.](imapimessagesite-getsession.md) <br/> |Возвращает сеанс MAPI, в котором было создано или открыто текущее сообщение.  <br/> |
|[DataStore](imapimessagesite-getstore.md) <br/> |Возвращает хранилище сообщений, содержащее текущее сообщение, если такое хранилище существует.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Возвращает папку, в которой было создано или открыто текущее сообщение, если такая папка существует.  <br/> |
|[Сообщение о доходе](imapimessagesite-getmessage.md) <br/> |Возвращает текущее сообщение.  <br/> |
|[жетформманажер](imapimessagesite-getformmanager.md) <br/> |Возвращает интерфейс диспетчера форм, который сервер форм может использовать для открытия другого сервера форм.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Создает новое сообщение.  <br/> |
|[копимессаже](imapimessagesite-copymessage.md) <br/> |Копирует текущее сообщение в папку.  <br/> |
|[мовемессаже](imapimessagesite-movemessage.md) <br/> |Перемещает текущее сообщение в папку.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Удаляет текущее сообщение.  <br/> |
|[савемессаже](imapimessagesite-savemessage.md) <br/> |Запрашивает сохранение текущего сообщения.  <br/> |
|[субмитмессаже](imapimessagesite-submitmessage.md) <br/> |Запрашивает доставку текущего сообщения в очередь на доставку.  <br/> |
|[жетситестатус](imapimessagesite-getsitestatus.md) <br/> |Возвращает сведения из объекта сайта сообщения о возможностях сайта сообщения для текущего сообщения.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте сайта сообщения.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

