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
ms.openlocfilehash: fd2575d401aa8a39d6f3b2cd08377b587b430ef1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808894"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Относится к**: Outlook 
  
Позволяет получать уведомления от средства просмотра формы серверам формы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Форма уведомить объектов приемника  <br/> |
|Реализованный:  <br/> |Серверы формы  <br/> |
|Вызывается:  <br/> |Средства просмотра формы  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Указывает, было изменено в состояние просмотра формы.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Указывает, является ли форма может обрабатывать класса сообщений для следующего сообщения для отображения.  <br/> |
   
## <a name="remarks"></a>Замечания

Объект приемника для реализации **IMAPIFormAdviseSink** вместо включая с их объекта формы рекомендаций использования серверов формы в форме. Таким образом формы просматривающих отчеты пользователей следует ожидать сбоя вызова метода [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) формы для получения указателя на этот интерфейс. 
  
Серверы формы вызов метода [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) средство просмотра для регистрации уведомлений. Указатель на их реализации **IMAPIFormAdviseSink** используется в качестве параметра. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

