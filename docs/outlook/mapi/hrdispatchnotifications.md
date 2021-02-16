---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348099"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Приумножу отправку всех уведомлений в очереди. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Отправлены все уведомления в очереди.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION или WM_ENDSESSION получено.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI не инициализирован.
    
## <a name="remarks"></a>Примечания

Функция **HrDispatchNotifications** заставляет MAPI отправлять все уведомления, которые в настоящее время находятся в очереди в движке уведомлений MAPI, не дожидаясь отправки сообщения. Это может положительно сказаться на использовании памяти. Дополнительные сведения см. [в принудительным уведомлении.](forcing-a-notification.md) 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Некоторые приложения ждут уведомления в цикле времени ожидания с помощью функций Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) и [DispatchMessage.](https://msdn.microsoft.com/library/ms644934.aspx) На всех самых быстрых платформах такие приложения могут испытывать низкую производительность или даже блокировку уведомлений. Использование **HrDispatchNotifications** не только уменьшает код, но и повышает производительность. 
  

