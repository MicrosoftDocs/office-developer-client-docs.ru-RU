---
title: Обычное состояние
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395793"
---
# <a name="normal-state"></a>Обычное состояние

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Обычном состоянии является, где объекта формы основную часть его время ожидания для клиентских приложений инициировать действие, например, сохранение изменений или закрытия формы. В следующей таблице описываются допустимые переходы в обычном состоянии.
  
|**Метод IPersistMessage**|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md) (_pMessage ==_ значение NULL, _fSameAsLoad ==_ TRUE)  <br/> -или-  <br/> **IPersistMessage::Save** (_pMessage! =_ значение NULL, _fSameAsLoad ==_ значение FALSE)  <br/> |Рекурсивно сохранить внедренные объекты OLE, которые были изменены. Сохраните объект message данные сообщений. Сохраните флаг _fSameAsLoad_ для последующего использования в состоянии [NoScribble](noscribble-state.md) .  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save** (_pMessage! =_ значение NULL, _fSameAsLoad ==_ TRUE)  <br/> |Это то же, как и в предыдущем, за исключением того, что этот вызов **Сохранить** используется в нехватки памяти и не должен выполнить аварийное переключение недостаток памяти.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Рекурсивно вызывать метод **HandsOffMessage** на внедренных сообщений или метод OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) внедренных объектов OLE. Освобождение сообщения и любой внедренных сообщений или несколько объектов.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) или [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Значение последней ошибки и возвратить значение E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает последнюю ошибку.  <br/> |Normal  <br/> |
|Другие [IPersistMessage: IUnknown](ipersistmessageiunknown.md) методы или методы от других интерфейсов  <br/> |Реализация, как описано в документации по [IPersistMessage: IUnknown](ipersistmessageiunknown.md) интерфейса.  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

