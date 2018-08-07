---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a7d62253baaaae7955e722874a15d05ed16e566e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809258"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**Относится к**: Outlook 
  
Управляет формы в форме просмотра клиентского приложения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Просмотр объектов контекста  <br/> |
|Реализованный:  <br/> |Средства просмотра формы  <br/> |
|Вызывается:  <br/> |Объекты формы  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIViewContext  <br/> |
|Тип указателя:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Управляет формы регистрации для получения уведомлений об изменениях в средстве просмотра.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Активирует следующий или предыдущий сообщения в средстве просмотра формы.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Извлекает сведения о текущем печати.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Получает поток, в который будет использоваться для сохранения текущего сообщения.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Извлекает текущее состояние просмотра.  <br/> |
|[GetLastError](imapiviewcontext-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущей ошибки, в объект контекста представления.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

