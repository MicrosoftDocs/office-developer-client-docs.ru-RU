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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309606"
---
# <a name="ipersistmessage--iunknown"></a>IPersistMessage : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет зрителям форм обрабатывать хранение формы и переход между различными состояниями.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Подвергается:  <br/> |Объекты сохраняемой почты  <br/> |
|Реализовано в:  <br/> |Объекты форм  <br/> |
|Вызывающая сторона:  <br/> |Просмотр форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IPersistMessage  <br/> |
|Тип указателя:  <br/> |LPPERSISTMESSAGE  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetLastError](ipersistmessage-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке в объекте формы.  <br/> |
|[GetClassID](ipersistmessage-getclassid.md) <br/> |Возвращает идентификатор, который представляет сервер форм, который может управлять формой.  <br/> |
|[IsDirty](ipersistmessage-isdirty.md) <br/> |Проверяет форму для изменений, которые были сделаны с момента последнего сохранения.  <br/> |
|[InitNew](ipersistmessage-initnew.md) <br/> |Инициализирует новое сообщение.  <br/> |
|[Load](ipersistmessage-load.md) <br/> |Загружает форму для указанного сообщения.  <br/> |
|[Save](ipersistmessage-save.md) <br/> |Сохраняет измененную форму обратно в сообщение, из которого она была загружена или создана.  <br/> |
|[SaveCompleted](ipersistmessage-savecompleted.md) <br/> |Сообщает форму о том, что операция сохранения завершена.  <br/> |
|[HandsOffMessage](ipersistmessage-handsoffmessage.md) <br/> |Вызывает выпуск текущего сообщения формы.  <br/> |
   
## <a name="remarks"></a>Примечания

Все формы необходимы для реализации **интерфейса IPersistMessage.** 
  
 **Интерфейс IPersistMessage** работает аналогично интерфейсу OLE [IPersistStorage.](https://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) Дополнительные сведения см. в методе **IPersistStorage.** 
  
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

