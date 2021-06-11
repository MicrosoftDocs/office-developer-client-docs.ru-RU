---
title: IMAPIFormAdviseSink IUnknown
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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет серверам форм получать уведомления от зрителей форм. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Подвергается:  <br/> |Form advise sink objects  <br/> |
|Реализовано в:  <br/> |Серверы форм  <br/> |
|Вызывающая сторона:  <br/> |Просмотр форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Указывает, что в состоянии просмотра формы произошли изменения.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Указывает, может ли форма обрабатывать класс сообщений следующего отображаемого сообщения.  <br/> |
   
## <a name="remarks"></a>Примечания

Серверы форм используют объект раковины формы для реализации **объекта IMAPIFormAdviseSink** вместо того, чтобы включать его в объект формы. Поэтому для просмотра форм следует ожидать неудаваемого вызова метода [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) для получения указателя на этот интерфейс. 
  
Серверы форм звонят по методу [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) для регистрации уведомлений. В качестве параметра включен указатель на реализацию **IMAPIFormAdviseSink.** 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

