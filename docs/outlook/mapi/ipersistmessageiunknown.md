---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7eb65bbae2fca6648c3a701dfa5c83c5bf297ec5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396185"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Включение средств просмотра формы для обработки хранилища формы и для перехода между состояниями различные.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Сохранение объектам сообщения  <br/> |
|Реализовано в:  <br/> |Объекты формы  <br/> |
|Вызывающая сторона:  <br/> |Средства просмотра формы  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IPersistMessage  <br/> |
|Тип указателя:  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущей ошибки в объекте формы.  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Возвращает идентификатор, представляющий сервера форм для управления формы.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Проверяет формы для изменения, внесенные с момента последнего сохранения.  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |Инициализирует новое сообщение.  <br/> |
|[Нагрузки](ipersistmessage-load.md) <br/> |Загружает формы для указанного сообщения.  <br/> |
|[Сохранение](ipersistmessage-save.md) <br/> |Сохраняет измененную форму сообщение, из которого его загрузки или создан.  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Уведомляет формы, которая сохранения завершения операции.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Приводит к освобождение сообщения, его текущей формы.  <br/> |
   
## <a name="remarks"></a>Замечания

Все формы необходимы для реализации интерфейса **IPersistMessage** . 
  
 **IPersistMessage** работает так же интерфейс OLE [IPersistStorage](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . Для получения дополнительных сведений см **IPersistStorage** методы. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

