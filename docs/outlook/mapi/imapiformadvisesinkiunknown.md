---
title: Имапиформадвисесинк IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286606"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет серверам форм получать уведомления от средств просмотра форм. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
|Предоставлено:  <br/> |Объекты приемника рекомендаций для форм  <br/> |
|Реализовано в:  <br/> |Серверы форм  <br/> |
|Вызывающая сторона:  <br/> |Средства просмотра форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Тип указателя:  <br/> |лпмапиформадвисесинк  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Указывает, что в состоянии средства просмотра форм произошло изменение.  <br/> |
|[онактиватенекст](imapiformadvisesink-onactivatenext.md) <br/> |Указывает, может ли форма обрабатывать класс сообщения следующего отображаемого сообщения.  <br/> |
   
## <a name="remarks"></a>Примечания

Серверы форм используют объект приемника уведомлений формы, чтобы реализовать **имапиформадвисесинк** , а не включать его в объект Form. Таким образом, средства просмотра форм должны ожидать неудачный вызов метода [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) формы, чтобы получить указатель на этот интерфейс. 
  
Серверы форм вызовите метод средства просмотра [имапивиевконтекст:: сетадвисесинк](imapiviewcontext-setadvisesink.md) для регистрации уведомлений. Указатель на свою реализацию **имапиформадвисесинк** включается в качестве параметра. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

