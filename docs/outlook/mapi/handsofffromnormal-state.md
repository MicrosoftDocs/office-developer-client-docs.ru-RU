---
title: HandsOffFromNormal State
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426473"
---
# <a name="handsofffromnormal-state"></a>HandsOffFromNormal State

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Состояние HandsOffFromNormal очень похоже на состояние [HandsOffAfterSave.](handsoffaftersave-state.md) Это часть процесса сохранения содержимого формы в постоянное хранилище. В этом состоянии объект формы должен отказаться от внесения изменений в копии значений свойств сообщения в памяти, так как может не быть другой возможности сохранить эти изменения. В следующей таблице описаны разрешенные переходы из состояния HandsOffFromNormal. 
  
|Метод IPersistMessage***|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)  <br/> |Замените сообщение объекта сообщения на _pMessage,_ которое заменяет сообщение, отозванное предыдущим вызовом [IPersistMessage::HandsOffMessage.](ipersistmessage-handsoffmessage.md) Данные в новом сообщении гарантированно будут такие же, как и в отозванных сообщениях. Сообщение не должно быть помечено как чистое и не должно вызываться после этого вызова [IMAPIViewAdviseSink::OnSaved.](imapiviewadvisesink-onsaved.md) В случае **успешного вызова SaveCompleted** введите состояние [Normal.](normal-state.md) В противном случае оставайтесь в состоянии HandsOffFromNormal.  <br/> |Normal или HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)  <br/> |Установите для последней ошибки E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Установите для последней ошибки E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает последнюю ошибку.  <br/> |HandsOffFromNormal  <br/> |
|Другие [методы IPersistMessage : методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов  <br/> |Установите для последней ошибки E_UNEXPECTED.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

