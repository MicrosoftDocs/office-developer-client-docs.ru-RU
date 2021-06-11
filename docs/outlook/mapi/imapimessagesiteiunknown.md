---
title: IMAPIMessageSite IUnknown
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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Манипулирует сообщениями и реализуется кодом просмотра форм (как правило, клиентского приложения), который реагирует на такие манипуляции.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Подвергается:  <br/> |Объекты сайта сообщений  <br/> |
|Реализовано в:  <br/> |Просмотр форм  <br/> |
|Вызывающая сторона:  <br/> |Объекты форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIMessageSite  <br/> |
|Тип указателя:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Возвращает сеанс MAPI, в котором было создано или открыто текущее сообщение.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Возвращает хранилище сообщений, содержаное текущее сообщение, если такой магазин существует.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Возвращает папку, в которой было создано или открыто текущее сообщение, если такая папка существует.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Возвращает текущее сообщение.  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Возвращает интерфейс диспетчера форм, который сервер формы может использовать для открытия другого сервера форм.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Создает новое сообщение.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Копирует текущее сообщение в папку.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Перемещает текущее сообщение в папку.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Удаляет текущее сообщение.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Запрашивает, чтобы текущее сообщение было сохранено.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Запрашивает, чтобы текущее сообщение было в очереди для доставки.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Возвращает сведения с объекта сайта сообщений о возможностях веб-сайта сообщений для текущего сообщения.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, произошедшей в объекте сайта сообщений.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

