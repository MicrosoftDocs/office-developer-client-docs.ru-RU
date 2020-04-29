---
title: имаписессионунадвисе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Unadvise
api_type:
- COM
ms.assetid: 5e608cb0-808d-4418-8521-71dcbce8cdff
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 98a5faca00f5877eb10110406875b46a69244d94
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335704"
---
# <a name="imapisessionunadvise"></a>IMAPISession::Unadvise

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отменяет отправку уведомлений, ранее настроенных с помощью вызова метода [IMAPISession:: Advise](imapisession-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Параметры

 _улконнектион_
  
> возврата Номер подключения, связанный с регистрацией активной уведомления. Значение _улконнектион_ должно быть возвращено предыдущим вызовом **IMAPISession:: Advise**.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация успешно отменена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession:: unadvise** отменяет регистрацию для уведомления. **Unadvise** — освобождает свой указатель приемника уведомлений вызывающего абонента, который он получил в вызове **advise** , используемом для регистрации. 
  
Как правило, метод **unadvise** вызывает метод [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) приемника уведомлений во время вызова метода **unadvise** . Тем не менее, если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) приемника уведомлений, вызов **освобождения** задерживается до возвращения метода **OnNotify** . 
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Advise](imapisession-advise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

