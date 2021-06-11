---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436386"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет зрителям форм работать с контекстами представления форм и уведомлениями форм, выполнять глаголы форм и закрывать формы.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Подвергается:  <br/> |Объекты форм  <br/> |
|Реализовано в:  <br/> |Серверы форм  <br/> |
|Вызывающая сторона:  <br/> |Просмотр форм  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIForm  <br/> |
|Тип указателя:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Создает контекст представления для формы.  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Возвращает текущий контекст представления для формы.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Закрывает форму.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Запрашивает, чтобы форма выполняла любые задачи, которые она связывает с определенным глаголом.  <br/> |
|[Консультирование](imapiform-advise.md) <br/> |Регистрирует просмотра форм для уведомлений о событиях, влияющих на форму.  <br/> |
|[Unadvise](imapiform-unadvise.md) <br/> |Отменяет регистрацию уведомлений со средством просмотра форм, ранее установленным по телефону **Advise**.  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, произошедшей в объект формы.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

