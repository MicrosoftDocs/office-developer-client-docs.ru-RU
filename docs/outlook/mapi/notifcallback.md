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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет функцию вызова, вызываемую MAPI для отправки уведомления о событии. Эту функцию вызова можно использовать только при завернутой в объект раковины рекомендации, созданный путем вызова [функции HrAllocAdviseSink.](hrallocadvisesink.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Определенные функции, реализованные в:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
|Определенная функция, вызванная:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Parameters

 _lpvContext_
  
> [in] Указатель на произвольное значение, переданного функции вызова при вызове MAPI. Это значение может представлять адрес, который имеет значение для клиентского приложения или поставщика услуг. Как правило, для кода C++ параметр  _lpvContext_ представляет указатель на объект C++. 
    
 _cNotification_
  
> [in] Количество уведомлений о событиях в массиве, указанных параметром _lpNotifications._ 
    
 _lpNotifications_
  
> [вышел] Указатель на расположение, в котором [](notification.md) эта функция записывает массив структур УВЕДОМЛЕНий, содержащий уведомления о событиях. 
    
## <a name="return-value"></a>Возвращаемое значение

Набор допустимых значений возврата для прототипа **функции NOTIFCALLBACK** зависит от того, реализуется ли эта функция клиентом или поставщиком услуг. Клиенты всегда должны возвращать S_OK. Поставщики могут возвращать S_OK или CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Примечания

CALLBACK_DISCONTINUE является допустимым возвратным значением только для синхронных функций обратного вызова; он запрашивает, чтобы MAPI немедленно прекратила обработку отозвок для этого уведомления. Когда CALLBACK_DISCONTINUE возвращается, MAPI задает параметр  _lpUlFlags_ NOTIFY_CANCELED при возвращении из [IMAPISupport:::Notify](imapisupport-notify.md). 
  
Ниже 11. Ограничения, которые может сделать синхронная функция вызова:
  
- Это не может привести к сгенерированию другого синхронного уведомления.
    
- Он не может отображать пользовательский интерфейс.
    
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

