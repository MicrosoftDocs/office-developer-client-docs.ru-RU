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
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406033"
---
# <a name="imapiviewcontext--iunknown"></a>IMAPIViewContext : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Управляет формой в клиентских приложениях для просмотра форм. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Подвергается:  <br/> |Просмотр объектов контекста  <br/> |
|Реализовано в:  <br/> |Просмотр форм  <br/> |
|Вызывающая сторона:  <br/> |Объекты форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIViewContext  <br/> |
|Тип указателя:  <br/> |LPMAPIVIEWCONTEXT  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[SetAdviseSink](imapiviewcontext-setadvisesink.md) <br/> |Управляет регистрацией формы для получения уведомлений об изменениях в зрителье.  <br/> |
|[ActivateNext](imapiviewcontext-activatenext.md) <br/> |Активирует следующее или предыдущее сообщение в виде просмотра формы.  <br/> |
|[GetPrintSetup](imapiviewcontext-getprintsetup.md) <br/> |Извлекает текущие сведения о печати.  <br/> |
|[GetSaveStream](imapiviewcontext-getsavestream.md) <br/> |Извлекает поток, который будет использоваться для сохранения текущего сообщения.  <br/> |
|[GetViewStatus](imapiviewcontext-getviewstatus.md) <br/> |Извлекает текущее состояние просмотра.  <br/> |
|[GetLastError](imapiviewcontext-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, произошедшей в объекте контекста представления.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

