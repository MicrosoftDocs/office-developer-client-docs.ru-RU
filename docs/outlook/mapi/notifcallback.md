---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434020"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет функцию callback, которую MAPI вызывает для отправки уведомления о событии. Эту функцию вызова можно использовать только при оболочке в объекте-конвеере, созданном путем вызова функции [HrAllocAdviseSink.](hrallocadvisesink.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Определяемая функция, реализованная в:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Определяемая функция, вызванная:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Параметры

 _lpvContext_
  
> [in] Указатель на произвольное значение, передав его функции вызова при вызове MAPI. Это значение может представлять адрес важности для клиентского приложения или поставщика услуг. Обычно для кода C++ параметр  _lpvContext_ представляет указатель на объект C++. 
    
 _cNotification_
  
> [in] Количество уведомлений о событиях в массиве, указанных параметром _lpNotifications._ 
    
 _lpNotifications_
  
> [out] Указатель на расположение, где эта [](notification.md) функция записывает массив структур УВЕДОМЛЕНий, содержащий уведомления о событиях. 
    
## <a name="return-value"></a>Возвращаемое значение

Набор допустимых возвращаемых значений для прототипа функции **NOTIFCALLBACK** зависит от того, реализована ли функция клиентского приложения или поставщика услуг. Клиенты должны всегда возвращать S_OK. Поставщики могут возвращать S_OK или CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Примечания

CALLBACK_DISCONTINUE является допустимым возвращаемым значением только для синхронных функций обратного вызова; он запрашивает, чтобы MAPI немедленно остановил обработку вызовов для этого уведомления. Когда CALLBACK_DISCONTINUE возвращается, MAPI задает для параметра  _lpUlFlags_ NOTIFY_CANCELED при возвращении из [IMAPISupport::Notify](imapisupport-notify.md). 
  
Ниже действовать можно с ограничениями, которые может использовать функция синхронного вызова.
  
- Это не может привести к генерированию другого синхронного уведомления.
    
- Он не может отображать пользовательский интерфейс.
    
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

