---
title: HrThisThreadAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrThisThreadAdviseSink
api_type:
- COM
ms.assetid: 12c07302-472f-4e4f-8087-1bdf0dc09a5a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0fb867d662064dfe5ff7759dba4b36a4635a2914
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427731"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает раковину рекомендации, которая обертывания существующей раковины рекомендации для безопасности потока. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Parameters

 _lpAdviseSink_
  
> [in] Указатель на раковину рекомендации, которая должна быть завернута. 
    
 _lppAdviseSink_
  
> [вышел] Указатель на указатель на новую раковину рекомендации, которая заворачивает раковину рекомендации, указываемую _параметром lpAdviseSink._ 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Цель оболочки — убедиться, что уведомление вызвано на том же потоке, который называется функцией **HrThisThreadAdviseSink.** Эта функция используется для защиты от вызовов уведомлений, которые должны работать на определенном потоке. 
  
Клиентские приложения должны использовать **HrThisThreadAdviseSink,** чтобы ограничить время получения уведомлений, то есть при вызове в [метод IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) объекта-раковины, переданного клиентом в предыдущем вызове Посоветуйте.  Если уведомления могут быть созданы произвольно, реализация уведомлений может заставить клиента в многоуровневую операцию, если это не будет уместно. Например, клиент может использовать библиотеку, например одну из библиотек классов Microsoft Foundation, которая не поддерживает многоуровневые вызовы. Уведомление на другом потоке затруднит тестирование такого клиента и сделает его склонным к ошибке. 
  
 **HrThisThreadAdviseSink** позволяет убедиться, что **вызовы OnNotify** происходят только в указанные периоды: 
  
- Во время обработки вызова к любому методу MAPI. 
    
- Во время обработки Windows сообщений. 
    
При **реализации HrThisThreadAdviseSink** любые вызовы в метод **OnNotify** новой раковины рекомендации в любом потоке приводят к выполнению исходного метода уведомления в потоке, на котором был вызван **HrThisThreadAdviseSink.** 
  
Дополнительные сведения об уведомлениях и рекомендации по раковинам см. в примере [Event Notification in MAPI](event-notification-in-mapi.md) и [implementing an Advise Sink Object.](implementing-an-advise-sink-object.md) 
  

