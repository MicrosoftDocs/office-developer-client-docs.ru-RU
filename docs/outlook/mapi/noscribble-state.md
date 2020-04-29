---
title: Состояние "каракули"
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
# <a name="noscribble-state"></a>Состояние "каракули"

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Состояние "каракули" указывает на то, что сохраняются изменения сообщения. Фактическое сохранение значений, хранящихся в пользовательском интерфейсе объекта формы, происходит, когда клиентское приложение вызывает метод объекта формы [иперсистмессаже:: Save](ipersistmessage-save.md) . В следующей таблице описаны допустимые переходы из состояния "Scribble". 
  
|Иперсистмессаже * * метод * *|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[Иперсистмессаже:: савекомплетед](ipersistmessage-savecompleted.md)(_пмессаже = =_ null)  <br/> |Если _фсамеаслоад_ имеет значение true, в вызове [Иперсистмессаже:: Save](ipersistmessage-save.md) , которая привела к тому, что форма была введена в состояние "каракули", а сообщение было изменено, внутреннее помечайте изменения как сохраненные и вызовите метод [имапивиевадвисесинк:: onsaved](imapiviewadvisesink-onsaved.md) .  <br/> |[Normal](normal-state.md) <br/> |
|**Иперсистмессаже:: савекомплетед**(_пмессаже! =_ null)  <br/> |Вызовите метод [иперсистмессаже:: хандсоффмессаже](ipersistmessage-handsoffmessage.md) (аналогичный методу OLE [Иперсистстораже:: хандсоффстораже](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) ), за которым следуют обычные действия **савекомплетед** . Если **савекомплетед** успешно, введите нормальное состояние. В противном случае введите состояние [HandsOffAfterSave](handsoffaftersave-state.md) .  <br/> |Обычный или HandsOffAfterSave  <br/> |
|**хандсоффмессаже** <br/> |Рекурсивно вызвать метод **хандсоффмессаже** для внедренных сообщений или метод OLE **Иперсистстораже:: хандсоффстораже** для внедренных объектов OLE. Освободите объект Message и все внедренные сообщения или объекты.  <br/> |HandsOffAfterSave  <br/> |
|**Save**, [Иперсистмессаже:: инитнев](ipersistmessage-initnew.md)или [иперсистмессаже:: Load](ipersistmessage-load.md) <br/> |Установка последней ошибки и возврат E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возврат последней ошибки.  <br/> |NoScribble  <br/> |
|Другие [иперсистмессаже:](ipersistmessageiunknown.md) методы или методы IUnknown из других интерфейсов  <br/> |Установка последней ошибки и возврат E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

