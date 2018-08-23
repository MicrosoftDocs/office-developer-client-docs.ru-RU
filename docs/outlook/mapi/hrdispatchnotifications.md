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
ms.openlocfilehash: 60c5d7e980d1dc4d4263a2be2267008dbee1fd4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594700"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Принудительное диспетчеризации всех уведомлений, помещенных в очередь. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����. 
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Все уведомления о помещенных в очередь отправки.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION или WM_ENDSESSION был получен.
    
MAPI_E_NOT_INITIALIZED
  
> Не удалось инициализировать MAPI.
    
## <a name="remarks"></a>Замечания

Функция **HrDispatchNotifications** вызывает MAPI для отправки всех уведомлений, которые в настоящее время в очереди в модуль уведомлений MAPI без ожидания отправки сообщения. Это может иметь положительный эффект на использование памяти. Для получения дополнительных сведений см [принудительным уведомление](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Некоторые приложения дождитесь сообщение уведомления в цикле времени ожидания, с помощью Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) и [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) функций. На всех, кроме быстрым платформ такие приложения могут возникнуть низким быстродействием или даже блокировки уведомлений. С помощью **HrDispatchNotifications** не только уменьшает кода, но повышает производительность. 
  

