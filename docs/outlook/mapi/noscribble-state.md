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
ms.openlocfilehash: 41f5acddf273de39a7d5952ccb00e868170c692d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810046"
---
# <a name="noscribble-state"></a>Состояние NoScribble

  
  
**Относится к**: Outlook 
  
Состояние NoScribble указывает на сохранение изменений в сообщение. Фактические сохранения значений, хранящихся в пользовательский интерфейс объекта формы возникает при вызове метода [IPersistMessage::Save](ipersistmessage-save.md) объекта формы клиентским приложением. В следующей таблице описываются допустимые переходы из состояния NoScribble. 
  
|IPersistMessage ** метод **|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage ==_ значение NULL)  <br/> |Если флаг _fSameAsLoad_ был TRUE на вызов [IPersistMessage::Save](ipersistmessage-save.md) , в которой обнаружен формы для ввода NoScribble состояния и сообщения были изменены, во внутренней сети пометить изменения при сохранении и вызова [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) метод.  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted** (_pMessage! =_ значение NULL)  <br/> |Метод [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) (аналогично методу OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) ) следуют обычных **SaveCompleted** действий. Если **SaveCompleted** прошла успешно, введите в обычном состоянии. В противном случае введите состояние [HandsOffAfterSave](handsoffaftersave-state.md) .  <br/> |Обычный или HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Рекурсивно вызывать метод **HandsOffMessage** на внедренных сообщений или метод OLE **IPersistStorage::HandsOffStorage** внедренных объектов OLE. Освобождение сообщения и любой внедренных сообщений или несколько объектов.  <br/> |HandsOffAfterSave  <br/> |
|**Сохраните**, [IPersistMessage::InitNew](ipersistmessage-initnew.md)или [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Значение последней ошибки и возвратить значение E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает последнюю ошибку.  <br/> |NoScribble  <br/> |
|Другие [IPersistMessage: IUnknown](ipersistmessageiunknown.md) методы или методы от других интерфейсов  <br/> |Значение последней ошибки и возвратить значение E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

