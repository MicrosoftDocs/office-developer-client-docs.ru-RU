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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает обертывую веху консультации, которая создает существующий обойм для обеспечения безопасности потока. 
  
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

## <a name="parameters"></a>Параметры

 _lpAdviseSink_
  
> [in] Указатель на завернутую оболочку в окну консультации. 
    
 _lppAdviseSink_
  
> [out] Указатель на указатель на новый замещений, который обтекает его, на который указывает _параметр lpAdviseSink._ 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Примечания

Цель оболочки — убедиться, что уведомление вызвано в том же потоке, что и функция **HrThisThreadAdviseSink.** Эта функция используется для защиты вызовов уведомлений, которые должны запускаться в определенном потоке. 
  
Клиентские приложения должны использовать **HrThisThreadAdviseSink,** чтобы ограничить время получения уведомлений, то есть при вызове метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) объекта приемника рекомендации, переданного клиентом в предыдущем вызове **advise.** Если уведомления могут быть созданы произвольно, реализация уведомлений может привести к принудительному принудительному выполнению клиентом многоэтабной операции, если это не подходит. Например, клиент может использовать библиотеку, например одну из библиотек классов Microsoft Foundation, которая не поддерживает многопрочитанные вызовы. Уведомление в другом потоке сделает такой клиент трудно тестировать и подвержен ошибкам. 
  
 **HrThisThreadAdviseSink** позволяет убедиться, что **вызовы OnNotify** происходят только в такое время: 
  
- Во время обработки вызова любого метода MAPI. 
    
- Во время обработки сообщений Windows. 
    
При **реализации HrThisThreadAdviseSink** все вызовы метода **OnNotify** нового приемника рекомендации в любом потоке приводят к выполнению исходного метода уведомления в потоке, в котором был вызван **HrThisThreadAdviseSink.** 
  
Дополнительные сведения об уведомлениях и уведомлениях о них см. в уведомлении о событии [в MAPI](event-notification-in-mapi.md) и [реализации объекта -висящего уведомления.](implementing-an-advise-sink-object.md) 
  

