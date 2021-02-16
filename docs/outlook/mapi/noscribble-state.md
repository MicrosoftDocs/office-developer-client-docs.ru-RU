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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Состояние NoScribble указывает, что изменения в сообщении сохраняются. Фактическое сохранение значений, сохраненных в пользовательском интерфейсе объекта формы, происходит, когда клиентский приложением вызван метод [IPersistMessage::Save](ipersistmessage-save.md) объекта формы. В следующей таблице описаны разрешенные переходы из состояния NoScribble. 
  
|Метод IPersistMessage***|**Действие**|**Новое состояние**|
|:-----|:-----|:-----|
|[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage ==_ NULL)  <br/> |Если для вызова [IPersistMessage::Save](ipersistmessage-save.md) флаг _fSameAsLoad_ был true, из-за чего форма вступает в состояние NoScribble и сообщение было изменено, пометите изменения как сохраненные и вызовите метод [IMAPIViewAdviseSink::OnSaved.](imapiviewadvisesink-onsaved.md)  <br/> |[Normal](normal-state.md) <br/> |
|**IPersistMessage::SaveCompleted**(_pMessage !=_ NULL)  <br/> |Вызовите метод [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) (аналогичный методу OLE [IPersistStorage::HandsOffStorage),](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) за которым следуют обычные действия **SaveCompleted.** Если **saveCompleted** был успешно, введите обычное состояние. В противном случае введите [состояние HandsOffAfterSave.](handsoffaftersave-state.md)  <br/> |Normal или HandsOffAfterSave  <br/> |
|**HandsOffMessage** <br/> |Рекурсивно вызывает метод **HandsOffMessage** для внедренных сообщений или метод OLE **IPersistStorage::HandsOffStorage** для внедренных объектов OLE. Освобождение объекта сообщения и всех внедренных сообщений или объектов.  <br/> |HandsOffAfterSave  <br/> |
|**Save**, [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md) <br/> |Установите для последней ошибки E_UNEXPECTED.  <br/> |NoScribble  <br/> |
|[IPersistMessage::GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает последнюю ошибку.  <br/> |NoScribble  <br/> |
|Другие [методы IPersistMessage : методы или методы IUnknown](ipersistmessageiunknown.md) из других интерфейсов  <br/> |Установите для последней ошибки E_UNEXPECTED.  <br/> |NoScribble  <br/> |
   
## <a name="see-also"></a>См. также



[Состояния форм](form-states.md)

