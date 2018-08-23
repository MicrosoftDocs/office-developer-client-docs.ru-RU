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
ms.openlocfilehash: 157703fc9702bb954b4a5c570fc3d5c045e181cc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567190"
---
# <a name="imapiviewadvisesink--iunknown"></a>IMAPIViewAdviseSink : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Получает уведомления от форм. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Просмотр рекомендаций объектов приемника  <br/> |
|Реализованный:  <br/> |Средства просмотра формы  <br/> |
|Вызывается:  <br/> |Объекты формы  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIViewAdviseSink  <br/> |
|Тип указателя:  <br/> |LPMAPIVIEWADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[Завершении](imapiviewadvisesink-onshutdown.md) <br/> |Уведомляет средство просмотра формы, что форма закрывается.  <br/> |
|[OnNewMessage](imapiviewadvisesink-onnewmessage.md) <br/> |Уведомляет средство просмотра формы после загрузки, что новое или существующее сообщение в форме.  <br/> |
|[Печать (OnPrint)](imapiviewadvisesink-onprint.md) <br/> |Уведомляет средство просмотра формы из состояния печати формы.  <br/> |
|[OnSubmitted](imapiviewadvisesink-onsubmitted.md) <br/> |Уведомляет средство просмотра формы, что текущего сообщения были отправлены диспетчер очереди MAPI.  <br/> |
|[OnSaved](imapiviewadvisesink-onsaved.md) <br/> |Уведомляет средство просмотра формы, который был сохранен текущего сообщения в форме.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

