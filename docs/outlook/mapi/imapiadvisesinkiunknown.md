---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409568"
---
# <a name="imapiadvisesink--iunknown"></a>IMAPIAdviseSink : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Реализует объект-замещение для обработки уведомлений. Указатель на объект приемника рекомендации передается в вызове метода **Advise** поставщика услуг, механизма, используемого для регистрации для уведомления. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Выставим:  <br/> |Рекомендуемые объекты-висяки  <br/> |
|Реализовано в:  <br/> |Клиентские приложения и MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIAdviseSink  <br/> |
|Тип указателя:  <br/> |LPMAPIADVISESINK  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[OnNotify](imapiadvisesink-onnotify.md) <br/> |Отвечает на уведомление, выполняя одну или несколько задач. Выполняемые задачи зависят от типа события и объекта, который создает уведомление.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

