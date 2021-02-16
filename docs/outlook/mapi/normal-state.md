---
title: Нормальное состояние
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d7b50a92c58dd7ab1f03cb4cf84acc2d4a2b404b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335747"
---
# <a name="normal-state"></a>Нормальное состояние

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Обычное состояние — это состояние, в котором объект формы большую часть времени проводит, ожидая, пока клиентские приложения инициируют действие, например сохранение изменений или закрытие формы. В следующей таблице описаны разрешенные переходы из состояния Normal.
  
|**Метод IPersistMessage**|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> -или-  <br/> **IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)  <br/> |Рекурсивно сохраните все измененные внедренные объекты OLE. Сохраните данные сообщения обратно в объект сообщения. _Сохраняем флаг fSameAsLoad для_ использования в состоянии [NoScribble.](noscribble-state.md)  <br/> |NoScribble  <br/> |
|**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)  <br/> |Это то же, что и в  предыдущем случае, за исключением того, что этот вызов save используется в ситуациях с низким объемом памяти и не должен вызывать сбой из-за нехватки памяти.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Рекурсивно вызывает метод **HandsOffMessage** для внедренных сообщений или метод OLE [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) для внедренных объектов OLE. Освобождение объекта сообщения и всех внедренных сообщений или объектов.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[IPersistMessage::SaveCompleted,](ipersistmessage-savecompleted.md) [IPersistMessage::InitNew](ipersistmessage-initnew.md) или [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Установите последнюю ошибку и E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает последнюю ошибку.  <br/> |Normal  <br/> |
|Другие [методы IPersistMessage : методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов  <br/> |Реализуются, как описано в документации для [интерфейса IPersistMessage : IUnknown.](ipersistmessageiunknown.md)  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

