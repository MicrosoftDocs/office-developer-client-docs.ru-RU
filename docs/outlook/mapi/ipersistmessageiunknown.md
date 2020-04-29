---
title: Иперсистмессаже IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309606"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет читателям форм обрабатывать хранение формы и переходить между различными состояниями.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
|Предоставлено:  <br/> |Объекты хранения сообщений  <br/> |
|Реализовано в:  <br/> |Объекты форм  <br/> |
|Вызывающая сторона:  <br/> |Средства просмотра форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IPersistMessage  <br/> |
|Тип указателя:  <br/> |лпперсистмессаже  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущем сообщении об ошибке в объекте Form.  <br/> |
|[Идентификатор ClassID](ipersistmessage-getclassid.md) <br/> |Возвращает идентификатор, представляющий сервер форм, который может управлять формой.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Проверяет форму на наличие изменений, выполненных с момента последнего сохранения.  <br/> |
|[инитнев](ipersistmessage-initnew.md) <br/> |Инициализирует новое сообщение.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Загружает форму для указанного сообщения.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |Сохраняет измененную форму обратно в сообщение, из которого она была загружена или создана.  <br/> |
|[савекомплетед](ipersistmessage-savecompleted.md) <br/> |Уведомляет форму о завершении операции сохранения.  <br/> |
|[хандсоффмессаже](ipersistmessage-handsoffmessage.md) <br/> |Заставляет форму выпустить текущее сообщение.  <br/> |
   
## <a name="remarks"></a>Примечания

Для реализации интерфейса **иперсистмессаже** необходимы все формы. 
  
 **Иперсистмессаже** работает аналогично интерфейсу OLE [иперсистстораже](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) . Дополнительные сведения см. в разделе методы **иперсистстораже** . 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

