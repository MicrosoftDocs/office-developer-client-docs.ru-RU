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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Получает уведомления из форм. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Выставим:  <br/> |Просмотр рекомендуемых объектов-тонух  <br/> |
|Реализовано в:  <br/> |Просмотр форм  <br/> |
|Вызывающая сторона:  <br/> |Объекты форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Тип указателя:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[OnShutdown](imapiviewadvisesink-onshutdown.md) <br/> |Извеирует просматриваемую форму о закрытии формы.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Сообщает просмотру формы о том, что новое или существующее сообщение загружено в форме.  <br/> |
|[OnPrint](imapiviewadvisesink-onprint.md) <br/> |Извеирует просмотр формы о состоянии печати формы.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Сообщает просмотру формы, что текущее сообщение отправлено в пул MAPI.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Сообщает просмотру формы о том, что текущее сообщение в форме сохранено.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

