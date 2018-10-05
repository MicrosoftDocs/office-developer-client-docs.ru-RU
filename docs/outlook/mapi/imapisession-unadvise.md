---
title: IMAPISessionUnadvise
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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397893"
---
# <a name="imapisessionunadvise"></a>IMAPISession::Unadvise

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Показано, как отменить отправку уведомлений, ранее настройка с помощью вызова метода [IMAPISession::Advise](imapisession-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a>Параметры

 _ulConnection_
  
> [in] Номер подключения, связанный с регистрацию active уведомлений. Необходимо, с помощью предыдущей вызова **IMAPISession::Advise**были возвращается значение _ulConnection_ .
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Регистрация успешно отменена.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::Unadvise** отменяет регистрацию для уведомлений. Выпуски **Unadvise** указатель вызывающего абонента уведомить приемника, полученных в вызове **уведомлений** , используемые для регистрации. 
  
Как правило **Unadvise** вызывает метод [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) приемник уведомлений во время вызова **Unadvise** . Тем не менее если другой поток находится в процессе вызова метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) приемник уведомлений, вызов **выпуске** откладывается до возвращения методом **OnNotify** . 
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPISession::Advise](imapisession-advise.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

