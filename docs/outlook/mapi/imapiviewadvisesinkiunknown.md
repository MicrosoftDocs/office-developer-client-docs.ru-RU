---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429420"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Получает уведомления из форм. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Подвергается:  <br/> |Просмотр рекомендуемых объектов раковины  <br/> |
|Реализовано в:  <br/> |Просмотр форм  <br/> |
|Вызывающая сторона:  <br/> |Объекты форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Тип указателя:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Заветив зрителю формы, что форма закрывается.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Сообщает зрителю формы, что новое или существующее сообщение загружено в форме.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Заветив зрителю формы состояние печати формы.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Сообщает зрителю формы, что текущее сообщение было отправлено в пулер MAPI.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Сообщает зрителю формы, что текущее сообщение в форме сохранено.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

