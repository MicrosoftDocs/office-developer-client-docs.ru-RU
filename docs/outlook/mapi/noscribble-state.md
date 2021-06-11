---
title: Состояние NoScribble
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0246138f-c55e-4353-8e53-e973f524d52c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 239f11cf27cdebff3d51645319d7ada3b9bb9ff6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326203"
---
# <a name="noscribble-state"></a>Состояние NoScribble

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Состояние NoScribble указывает, что изменения в сообщении сохраняются. Фактическое сохранение значений, хранимых в пользовательском интерфейсе объекта формы, происходит, когда метод [IPersistMessage объекта формы::Сохранить](ipersistmessage-save.md) вызван клиентом приложения. В следующей таблице описываются разрешенные переходы из состояния NoScribble. 
  
|Метод IPersistMessage** **|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)_(pMessage ==_ NULL)  <br/> |Если _флаг fSameAsLoad_ был TRUE на [вызове IPersistMessage::Сохранить,](ipersistmessage-save.md) из-за чего форма была в состоянии NoScribble и сообщение изменено, внутренне помечайте изменения как сохраненные и вызывайте [метод IMAPIViewAdviseSink::OnSaved.](imapiviewadvisesink-onsaved.md)  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted**_(pMessage!=_ NULL)  <br/> |Вызывай метод [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) (аналогичный методу OLE [IPersistStorage::HandsOffStorage)](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) с обычным действием **SaveCompleted.** Если **saveCompleted** был успешным, введите нормальное состояние. В противном случае введите [состояние HandsOffAfterSave.](handsoffaftersave-state.md)  <br/> |Нормальный или HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Повторно вызывает метод **HandsOffMessage** на встроенных сообщениях или метод OLE **IPersistStorage::HandsOffStorage** на встроенных объектах OLE. Отпустите объект сообщения и все встроенные сообщения или объекты.  <br/> |HandsOffAfterSave  <br/> |
|**Сохранить**, [IPersistMessage::InitNew](ipersistmessage-initnew.md), или [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Установите последнюю ошибку и верни E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращаем последнюю ошибку.  <br/> |NoScribble  <br/> |
|Другие [методы IPersistMessage: методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов  <br/> |Установите последнюю ошибку и верни E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

