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
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406607"
---
# <a name="handsoffaftersave-state"></a>Состояние HandsOffAfterSave

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Состояние HandsOffAfterSave является частью процесса сохранения содержимого формы в постоянное хранилище. В этом состоянии объект формы должен отказаться от внесения изменений в копии значений свойств сообщения в памяти, так как может не быть другой возможности сохранить эти изменения. В следующей таблице описаны разрешенные переходы из состояния HandsOffAfterSave.
  
|**Метод IPersistMessage**|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Откройте все внедренные объекты. Данные в сообщении, хранимые в _pMessage,_ гарантированно будут такие же, как и в предыдущем вызове [IPersistMessage::Save.](ipersistmessage-save.md) Если вызов **SaveCompleted** был успешным, введите обычное состояние. В противном случае установите для последней ошибки E_OUTOFMEMORY состояние HandsOffAfterSave.  <br/> |[Normal](normal-state.md) или HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Установите для последней ошибки E_INVALIDARG или E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Установите последнюю ошибку и E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Загрузка объекта формы с данными из целевого сообщения. Этот вызов может происходить, когда объект формы идет к следующему или предыдущему сообщению в папке.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает последнюю ошибку.  <br/> |HandsOffAfterSave  <br/> |
|Другие [методы IPersistMessage : методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов  <br/> |Установите последнюю ошибку и E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

