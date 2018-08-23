---
title: Запуск новой формы создания
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffceaa03-76f2-42e0-b28d-226f1f9cc889
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 66aa5fe08b1c0be3906fa9a0483bbdec37c095c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564502"
---
# <a name="launching-a-new-compose-form"></a>Запуск новой формы создания

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Специалистов по внедрению сервера форм следует ожидать следующую последовательность вызовов к серверу формы и объекты формы при клиентского приложения откроется новое сообщение для составления:
  
1. Клиентское приложение вызывает метод [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) для получения класса сведений о класс сообщения сервера форм. 
    
2. Клиентское приложение вызывает [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) для получения объекта формы. 
    
3. Диспетчер формы MAPI загружает на сервере формы, если он еще не в памяти и получает интерфейс [IMAPIForm](imapiformiunknown.md) с сервера формы. 
    
4. Клиентское приложение принимает итоговый интерфейс **IMAPIForm** и вызывает метод [IUnknown::QueryInterface](http://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) для получения объекта [IPersistMessage](ipersistmessageiunknown.md) интерфейса. 
    
5. Клиентское приложение вызывает метод [IPersistMessage::InitNew](ipersistmessage-initnew.md) для связывания объекта формы с [IMessage](imessageimapiprop.md), контекст представления и уведомить объектов приемника.
    
6. Клиентское приложение вызывает метод [IMAPIForm::DoVerb](imapiform-doverb.md) для вызова open команды. 
    
## <a name="see-also"></a>См. также



[Взаимодействие серверов форм](form-server-interactions.md)

