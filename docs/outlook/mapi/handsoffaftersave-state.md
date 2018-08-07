---
title: Состояние HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4bc4d680903d81b51a39ed39db3861597443d116
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808577"
---
# <a name="handsoffaftersave-state"></a>Состояние HandsOffAfterSave

  
  
**Относится к**: Outlook 
  
Состояние HandsOffAfterSave является частью процесс сохранения содержимое формы в постоянном хранилище. При работе в это состояние означает, объекта формы следует отказаться от внесения изменений в памяти копии значений свойств сообщений, так как не может быть другой возможности, чтобы сохранить изменения. В следующей таблице описываются допустимые переходы из состояния HandsOffAfterSave.
  
|**Метод IPersistMessage**|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ значение NULL)  <br/> |Откройте внедренные объекты. Данные в сообщении, хранящиеся в _pMessage_ гарантированно то же, что сообщение в предыдущем вызове [IPersistMessage::Save](ipersistmessage-save.md) . Если выполнен вызов **SaveCompleted** введите обычном состоянии. В противном случае — значение E_OUTOFMEMORY последней ошибки и всегда оставаться в состоянии HandsOffAfterSave.  <br/> |[Обычный](normal-state.md) или HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage ==_ значение NULL)  <br/> |Значение E_INVALIDARG или значение E_UNEXPECTED последнюю ошибку.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Сохраните**или [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Значение последней ошибки и возвратить значение E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Загрузите объект формы с данными из целевого сообщения. Этот вызов может возникнуть при переходе объекта формы в следующий или предыдущий сообщения в папке.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает последнюю ошибку.  <br/> |HandsOffAfterSave  <br/> |
|Другие [IPersistMessage: IUnknown](ipersistmessageiunknown.md) методы или методы от других интерфейсов  <br/> |Значение последней ошибки и возвратить значение E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

