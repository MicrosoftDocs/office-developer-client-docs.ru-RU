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
ms.openlocfilehash: b14529e987b85d1dcbe3689d4e852a9efd39a396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810041"
---
# <a name="notifcallback"></a>NOTIFCALLBACK

  
  
**Относится к**: Outlook 
  
Определяет функцию обратного вызова, которая вызывает MAPI для отправки уведомления о событии. Эта функция обратного вызова используется только в том случае, если в объект приемника уведомлений, созданный с помощью вызова функции [HrAllocAdviseSink](hrallocadvisesink.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Функция реализован:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
|Вызывается функция:  <br/> |MAPI  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a>Параметры

 _lpvContext_
  
> [in] Указатель произвольных значение передается функции обратного вызова, когда она вызывается средствами MAPI. Это значение может представлять адрес важности для клиентского приложения или поставщика услуг. Обычно для кода C++ параметр _lpvContext_ представляет указатель на объект C++. 
    
 _cNotification_
  
> [in] Количество уведомлений о событиях в массива, указанного в параметре _lpNotifications_ . 
    
 _lpNotifications_
  
> [out] Указатель на место, где эта функция записывает массив структур [УВЕДОМЛЕНИЙ](notification.md) , который содержит уведомления о событиях. 
    
## <a name="return-value"></a>������������ ��������

Набор допустимый возвращаемые значения для прототипа функции **NOTIFCALLBACK** зависит от ли реализовать функцию клиентского приложения или поставщиком услуг. Клиенты должны всегда возвращает значение S_OK. Поставщики могут возвращать значение S_OK или CALLBACK_DISCONTINUE. 
  
## <a name="remarks"></a>Замечания

CALLBACK_DISCONTINUE является допустимым возвращаемое значение для функции синхронные обратного вызова. он запрашивает, что MAPI немедленной остановки обработки обратных вызовов для этого уведомления. При возвращении CALLBACK_DISCONTINUE MAPI задается параметр _lpUlFlags_ NOTIFY_CANCELED при возврате из [IMAPISupport::Notify](imapisupport-notify.md). 
  
Ниже приведены ограничения на функцию обратного вызова синхронного действия.
  
- Он не может вызывать другой синхронного уведомления был создан.
    
- Не может отображать пользовательский интерфейс.
    
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)

