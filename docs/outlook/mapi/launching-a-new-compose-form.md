---
title: Запуск новой формы сочинения
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
# <a name="launching-a-new-compose-form"></a>Запуск новой формы сочинения

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Реализации серверов форм следует ожидать следующей последовательности вызовов метода на их сервер формы и объекты формы, когда клиентская заявка открывает новое сообщение для составления:
  
1. Клиентская заявка вызывает [метод IMAPIFormMgr::ResolveMessageClass,](imapiformmgr-resolvemessageclass.md) чтобы получить сведения о классе сообщения сервера форм. 
    
2. Клиентская заявка [вызывает IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) для получения нового объекта формы. 
    
3. Диспетчер форм MAPI загружает сервер форм, если он еще не находится в памяти, и получает интерфейс [IMAPIForm](imapiformiunknown.md) с сервера форм. 
    
4. Клиентская заявка принимает получаемый **интерфейс IMAPIForm** и вызывает метод [IUnknown::QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) для получения интерфейса [IPersistMessage](ipersistmessageiunknown.md) объекта. 
    
5. Клиентская заявка вызывает [метод IPersistMessage::InitNew,](ipersistmessage-initnew.md) чтобы связать объект формы с [IMessage,](imessageimapiprop.md)просматривать контекст и консультировать объекты раковины.
    
6. Клиентская заявка вызывает [метод IMAPIForm::D oVerb](imapiform-doverb.md) для вызова открытого глагола. 
    
## <a name="see-also"></a>См. также



[Взаимодействие с сервером форм](form-server-interactions.md)

