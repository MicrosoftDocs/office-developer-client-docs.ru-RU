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
  
При открытии приложением для создания нового сообщения с помощью средств реализации сервера форм необходимо ожидать приведенной ниже последовательности вызовов этих методов к серверу форм и объектам формы.
  
1. Клиентское приложение вызывает метод [имапиформмгр:: ресолвемессажекласс](imapiformmgr-resolvemessageclass.md) для получения сведений о классе, посвященных классу сообщений сервера форм. 
    
2. Клиентское приложение вызывает метод [имапиформмгр:: креатеформ](imapiformmgr-createform.md) , чтобы получить новый объект Form. 
    
3. Диспетчер форм MAPI загружает сервер форм, если он еще не находится в памяти, и получает интерфейс [имапиформ](imapiformiunknown.md) от сервера форм. 
    
4. Клиентское приложение получает полученный в результате интерфейс **имапиформ** и вызывает метод [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) для получения интерфейса [иперсистмессаже](ipersistmessageiunknown.md) объекта. 
    
5. Клиентское приложение вызывает метод [иперсистмессаже:: инитнев](ipersistmessage-initnew.md) , чтобы сопоставить объект формы с объектами [iMessage](imessageimapiprop.md), View контекста и приемника уведомлений.
    
6. Клиентское приложение вызывает метод [имапиформ::D оверб](imapiform-doverb.md) для вызова команды Open. 
    
## <a name="see-also"></a>См. также



[Взаимодействие с сервером форм](form-server-interactions.md)

