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
ms.openlocfilehash: 29d53ba1242014a501a01d161c19dade164f393a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270058"
---
# <a name="launching-a-new-compose-form"></a>Запуск новой формы создания

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
При открываемом клиентом сообщении для формирования нового сообщения для реализации серверов форм следует ожидать следующей последовательности вызовов методов к их серверам форм и объектам форм:
  
1. Клиентские приложения вызывает [метод IMAPIFormMgr::ResolveMessageClass для](imapiformmgr-resolvemessageclass.md) получения сведений о классе класса сообщения сервера форм. 
    
2. Клиентские приложения вызывает [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) для получения нового объекта формы. 
    
3. Диспетчер форм MAPI загружает сервер форм, если он еще не находится в памяти, и получает интерфейс [IMAPIForm](imapiformiunknown.md) с сервера форм. 
    
4. Клиентские приложения принимает итоговый интерфейс **IMAPIForm** и вызывает метод [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) для получения [интерфейса IPersistMessage](ipersistmessageiunknown.md) объекта. 
    
5. Клиентский приложение вызывает метод [IPersistMessage::InitNew,](ipersistmessage-initnew.md) чтобы связать объект формы с [IMessage,](imessageimapiprop.md)контекстом представления и сообщить об объектах приемника.
    
6. Клиентские приложения вызывают [метод IMAPIForm::D oVerb](imapiform-doverb.md) для вызова открытой команды. 
    
## <a name="see-also"></a>См. также



[Взаимодействие с сервером форм](form-server-interactions.md)

