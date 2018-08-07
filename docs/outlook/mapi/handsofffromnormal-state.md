---
title: Состояние HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d0b7baf4ab17d12145170961a43ca4be252146a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808585"
---
# <a name="handsofffromnormal-state"></a>Состояние HandsOffFromNormal

  
  
**Относится к**: Outlook 
  
Состояние HandsOffFromNormal очень похоже на состояние [HandsOffAfterSave](handsoffaftersave-state.md) . Он является частью процесс сохранения содержимое формы в постоянном хранилище. При работе в это состояние означает, объекта формы следует отказаться от внесения изменений в памяти копии значений свойств сообщений, так как не может быть другой возможности, чтобы сохранить изменения. В следующей таблице описываются допустимые переходы из состояния HandsOffFromNormal. 
  
|IPersistMessage ** метод **|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ значение NULL)  <br/> |Замените объект message сообщение _pMessage_которого является заменой отозван предыдущего вызова [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md)сообщение. Данные в новое сообщение гарантированно такой же, как отозванного сообщения. Сообщение не должен быть помечен как чистая, а также [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) вызван после этого вызова. Если выполнен вызов **SaveCompleted** введите состояние [Normal](normal-state.md) . В противном случае остаются в состоянии HandsOffFromNormal.  <br/> |Обычный или HandsOffFromNormal  <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage ==_ значение NULL)  <br/> |Присвоено значение E_UNEXPECTED последнюю ошибку.  <br/> |HandsOffFromNormal  <br/> |
|**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)или [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Присвоено значение E_UNEXPECTED последнюю ошибку.  <br/> |HandsOffFromNormal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает последнюю ошибку.  <br/> |HandsOffFromNormal  <br/> |
|Другие [IPersistMessage: IUnknown](ipersistmessageiunknown.md) методы или методы от других интерфейсов  <br/> |Присвоено значение E_UNEXPECTED последнюю ошибку.  <br/> |HandsOffFromNormal  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

