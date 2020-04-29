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
  
Нормальное состояние — это место, где объект формы тратит большую часть времени, ожидая, когда клиентские приложения инициируют действие, например сохранение изменений или закрытие формы. В следующей таблице описаны допустимые переходы из нормального состояния.
  
|**Метод Иперсистмессаже**|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[Иперсистмессаже:: Save](ipersistmessage-save.md)(_пмессаже = =_ null, _фсамеаслоад = =_ true)  <br/> -или-  <br/> **Иперсистмессаже:: Save**(_пмессаже! =_ null, _фсамеаслоад = =_ false)  <br/> |Рекурсивно сохраните все измененные внедренные объекты OLE. Сохраните данные сообщения обратно в объект Message. Сохраните флаг _фсамеаслоад_ для дальнейшего использования в состоянии " [каракули](noscribble-state.md) ".  <br/> |NoScribble  <br/> |
|**Иперсистмессаже:: Save**(_пмессаже! =_ null, _фсамеаслоад = =_ true)  <br/> |Это то же самое, что и в предыдущем случае, за исключением того, что этот вызов **Save** используется в ситуациях с нехваткой памяти и не может привести к нехватке памяти.  <br/> |NoScribble  <br/> |
|[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Рекурсивно вызвать метод **хандсоффмессаже** для внедренных сообщений или метод OLE [Иперсистстораже:: хандсоффстораже](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) для внедренных объектов OLE. Освободите объект Message и все внедренные сообщения или объекты.  <br/> |[HandsOffFromNormal](handsofffromnormal-state.md) <br/> |
|[Иперсистмессаже:: савекомплетед](ipersistmessage-savecompleted.md), [Иперсистмессаже:: инитнев](ipersistmessage-initnew.md) или [иперсистмессаже:: Load](ipersistmessage-load.md) <br/> |Установка последней ошибки и возврат E_UNEXPECTED.  <br/> |Normal  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возврат последней ошибки.  <br/> |Normal  <br/> |
|Другие [иперсистмессаже:](ipersistmessageiunknown.md) методы или методы IUnknown из других интерфейсов  <br/> |Реализуйте, как описано в документации для интерфейса [иперсистмессаже: IUnknown](ipersistmessageiunknown.md) .  <br/> |Normal  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

