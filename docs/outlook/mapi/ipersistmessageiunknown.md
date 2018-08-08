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
ms.openlocfilehash: 62fb2b069a50408713eea741cf837c421a749fcd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809518"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**Относится к**: Outlook 
  
Включение средств просмотра формы для обработки хранилища формы и для перехода между состояниями различные.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Сохранение объектам сообщения  <br/> |
|Реализованный:  <br/> |Объекты формы  <br/> |
|Вызывается:  <br/> |Средства просмотра формы  <br/> |
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
  
 **IPersistMessage** работает так же интерфейс OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . Для получения дополнительных сведений см **IPersistStorage** методы. 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

