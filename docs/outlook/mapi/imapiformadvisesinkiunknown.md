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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392062"
---
# <a name="imapiformadvisesink--iunknown"></a>IMAPIFormAdviseSink : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет получать уведомления от средства просмотра формы серверам формы. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Форма уведомить объектов приемника  <br/> |
|Реализовано в:  <br/> |Серверы формы  <br/> |
|Вызывающая сторона:  <br/> |Средства просмотра формы  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIFormAdviseSink  <br/> |
|Тип указателя:  <br/> |LPMAPIFORMADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[OnChange](imapiformadvisesink-onchange.md) <br/> |Указывает, было изменено в состояние просмотра формы.  <br/> |
|[OnActivateNext](imapiformadvisesink-onactivatenext.md) <br/> |Указывает, является ли форма может обрабатывать класса сообщений для следующего сообщения для отображения.  <br/> |
   
## <a name="remarks"></a>Замечания

Объект приемника для реализации **IMAPIFormAdviseSink** вместо включая с их объекта формы рекомендаций использования серверов формы в форме. Таким образом формы просматривающих отчеты пользователей следует ожидать сбоя вызова метода [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) формы для получения указателя на этот интерфейс. 
  
Серверы формы вызов метода [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) средство просмотра для регистрации уведомлений. Указатель на их реализации **IMAPIFormAdviseSink** используется в качестве параметра. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

