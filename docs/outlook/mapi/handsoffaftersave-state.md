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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Состояние HandsOffAfterSave является частью процесса сохранения содержимого формы в постоянное хранилище. Когда в этом состоянии объект формы должен воздерживаться от внесения изменений в копии значений свойств сообщения в памяти, так как не может быть другой возможности сохранить эти изменения. В следующей таблице описываются разрешенные переходы из состояния HandsOffAfterSave.
  
|**Метод IPersistMessage**|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)_(pMessage!=_ NULL)  <br/> |Откройте все встроенные объекты. Данные в сообщении, хранимом _в pMessage,_ гарантированно будут одинаковыми с данными предыдущего вызова [IPersistMessage:::Save.](ipersistmessage-save.md) Если вызов **SaveCompleted** удался, введите нормальное состояние. В противном случае установите последнюю ошибку E_OUTOFMEMORY и оставайтесь в состоянии HandsOffAfterSave.  <br/> |[Нормальный](normal-state.md) или HandsOffAfterSave  <br/> |
|**IPersistMessage::SaveCompleted**_(pMessage ==_ NULL)  <br/> |Установите последнюю ошибку для E_INVALIDARG или E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, [или IPersistMessage::InitNew](ipersistmessage-initnew.md) <br/> |Установите последнюю ошибку и верни E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
|[IPersistMessage::Load](ipersistmessage-load.md) <br/> |Загрузить объект формы данными из целевого сообщения. Этот вызов может произойти, когда объект формы будет отправляться к следующему или предыдущему сообщению в папке.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращаем последнюю ошибку.  <br/> |HandsOffAfterSave  <br/> |
|Другие [методы IPersistMessage: методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов  <br/> |Установите последнюю ошибку и верни E_UNEXPECTED.  <br/> |HandsOffAfterSave  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

