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
ms.openlocfilehash: 3df5e012867623d1c5e8fb5c3c93103548ab97be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588386"
---
# <a name="hrthisthreadadvisesink"></a>HrThisThreadAdviseSink

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создание приемника уведомления, которое имеет приемника уведомления для потокобезопасность. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
   
```cpp
HrThisThreadAdviseSink(
  LPMAPIADVISESINK lpAdviseSink,
  LPMAPIADVISESINK FAR * lppAdviseSink
);
```

## <a name="parameters"></a>Параметры

 _lpAdviseSink_
  
> [in] Указатель на приемник уведомлений преобразуемый. 
    
 _lppAdviseSink_
  
> [out] Указатель на указатель на новый приемник уведомлений, который является оболочкой приемник уведомлений, на который указывает параметр _lpAdviseSink_ . 
    
## <a name="return-value"></a>Возвращаемое значение

Нет.
  
## <a name="remarks"></a>Замечания

Программа-оболочка предназначен для убедитесь в том, что уведомления вызывается в том же потоке, который вызывается функция **HrThisThreadAdviseSink** . Эта функция используется для защиты уведомлений обратных вызовов, которые необходимо выполнить в определенном потоке. 
  
Клиентские приложения следует использовать **HrThisThreadAdviseSink** для ограничения при создании уведомлений, то есть, при вызове метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) объекта приемник уведомлений, передается клиентом в предыдущем **уведомлений **вызова. Если уведомления могут создаваться произвольно, уведомления о реализации может принудительно клиента в многопоточные операции при, который может быть неприемлема. Например клиента использовать библиотеки, например один из библиотеки классов Microsoft Foundation, который не поддерживает многопоточных вызовов. Уведомления в потоке сделает такой клиент неудобен для тестирования и может привести к ошибке. 
  
 **HrThisThreadAdviseSink** следит за тем, что **OnNotify** вызовы происходят только при этом соответствующий: 
  
- Во время обработки вызова любого метода MAPI. 
    
- Во время обработки сообщений Windows. 
    
При реализации **HrThisThreadAdviseSink** все вызовы метода **OnNotify** новый приемник уведомлений в любом потоке вызвать для выполнения в потоке, на котором **HrThisThreadAdviseSink** вызван метод исходного уведомления. 
  
Дополнительные сведения о уведомлений и приемников уведомлений, [Уведомления о событии в MAPI](event-notification-in-mapi.md) и [реализация объекта уведомить приемника](implementing-an-advise-sink-object.md). 
  

