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
ms.openlocfilehash: ce0e109aad52bfc4d7f4f55abfe1001d76276f64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587133"
---
# <a name="imapiform--iunknown"></a>IMAPIForm : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Включение средств просмотра формы для работы с контекстах представления формы и формы уведомлений, для выполнения команд формы и завершение работы форм.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiform.h  <br/> |
|Предоставляемые:  <br/> |Объекты формы  <br/> |
|Реализованный:  <br/> |Серверы формы  <br/> |
|Вызывается:  <br/> |Средства просмотра формы  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIForm  <br/> |
|Тип указателя:  <br/> |LPMAPIFORM  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[SetViewContext](imapiform-setviewcontext.md) <br/> |Устанавливает контекст представления для формы.  <br/> |
|[GetViewContext](imapiform-getviewcontext.md) <br/> |Возвращает текущий контекст представления для формы.  <br/> |
|[ShutdownForm](imapiform-shutdownform.md) <br/> |Закрывает форму.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |Запросы, формы выполнить все задачи связывается с определенным команды.  <br/> |
|[Уведомить](imapiform-advise.md) <br/> |Регистрирует просмотра формы для уведомлений о событиях, которые влияют на форме.  <br/> |
|[Unadvise](imapiform-unadvise.md) <br/> |Отменяет регистрацию для уведомлений с помощью средства просмотра формы, ранее установленные путем вызова **уведомлений**.  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , содержащий сведения об ошибке предыдущей появление объекта формы.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

