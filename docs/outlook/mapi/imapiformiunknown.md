---
title: Имапиформ IUnknown
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет средствам просмотра форм работать с контекстами представления формы и уведомлениями форм, для выполнения команд форм и для завершения работы форм.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиформ. h  <br/> |
|Предоставлено:  <br/> |Объекты форм  <br/> |
|Реализовано в:  <br/> |Серверы форм  <br/> |
|Вызывающая сторона:  <br/> |Средства просмотра форм  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имапиформ  <br/> |
|Тип указателя:  <br/> |ЛПМАПИФОРМ  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Сетвиевконтекст](imapiform-setviewcontext.md) <br/> |Создает контекст представления для формы.  <br/> |
|[Жетвиевконтекст](imapiform-getviewcontext.md) <br/> |Возвращает текущий контекст представления для формы.  <br/> |
|[Шутдовнформ](imapiform-shutdownform.md) <br/> |Закрывает форму.  <br/> |
|[DoVerb](imapiform-doverb.md) <br/> |ЗаПрашивает выполнение формой любых задач, которые она связывает с определенной командой.  <br/> |
|[Рекомендуем](imapiform-advise.md) <br/> |Регистрирует средство просмотра форм для уведомлений о событиях, влияющих на форму.  <br/> |
|[Unadvise](imapiform-unadvise.md) <br/> |ОтМеняет регистрацию для уведомлений с помощью средства просмотра форм, предварительно установленного с помощью метода **advise**.  <br/> |
|[GetLastError](imapiform-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущей ошибке, возникшей в объекте Form.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

