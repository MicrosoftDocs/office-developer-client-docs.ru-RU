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
ms.openlocfilehash: cffa3024b8533f07f8f76fa5bbac219e23d61bdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589506"
---
# <a name="imapimessagesite--iunknown"></a>IMAPIMessageSite : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Управляет сообщений и реализуется код средства просмотра формы (обычно клиентское приложение), которая отвечает на такой обработки.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Объекты сайта сообщения  <br/> |
|Реализованный:  <br/> |Средства просмотра формы  <br/> |
|Вызывается:  <br/> |Объекты формы  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIMessageSite  <br/> |
|Тип указателя:  <br/> |LPMAPIMESSAGESITE  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetSession](imapimessagesite-getsession.md) <br/> |Возвращает сеанса MAPI, в которой была создана или открыта текущего сообщения.  <br/> |
|[GetStore](imapimessagesite-getstore.md) <br/> |Если такие хранилища возвращает хранилище сообщение, содержащее текущее сообщение.  <br/> |
|[GetFolder](imapimessagesite-getfolder.md) <br/> |Возвращает папку, в которой была создана или открыта, текущего сообщения, если такая папка существует.  <br/> |
|[GetMessage](imapimessagesite-getmessage.md) <br/> |Возвращает текущее сообщение.  <br/> |
|[GetFormManager](imapimessagesite-getformmanager.md) <br/> |Возвращает интерфейс диспетчера формы, который сервера форм можно использовать для открытия другой сервер формы.  <br/> |
|[NewMessage](imapimessagesite-newmessage.md) <br/> |Создает новое сообщение.  <br/> |
|[CopyMessage](imapimessagesite-copymessage.md) <br/> |Копирует текущего сообщения в папку.  <br/> |
|[MoveMessage](imapimessagesite-movemessage.md) <br/> |Перемещает текущего сообщения в папку.  <br/> |
|[DeleteMessage](imapimessagesite-deletemessage.md) <br/> |Удаление текущего сообщения.  <br/> |
|[SaveMessage](imapimessagesite-savemessage.md) <br/> |Запросы, которые сохранены текущего сообщения.  <br/> |
|[SubmitMessage](imapimessagesite-submitmessage.md) <br/> |Запросы в текущем сообщении очереди для доставки.  <br/> |
|[GetSiteStatus](imapimessagesite-getsitestatus.md) <br/> |Возвращает сведения из объекта сайта сообщения о сообщении возможности веб-узла для текущего сообщения.  <br/> |
|[GetLastError](imapimessagesite-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , которая содержит сведения об ошибке предыдущей появление сообщения объект сайта.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

