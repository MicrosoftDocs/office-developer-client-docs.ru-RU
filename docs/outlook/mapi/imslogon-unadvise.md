---
title: Имслогонунадвисе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317278"
---
# <a name="imslogonunadvise"></a>IMSLogon::Unadvise

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаляет регистрацию объекта для уведомления об изменениях хранилища сообщений, ранее установленных с помощью вызова метода [имслогон:: Advise](imslogon-advise.md) . 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Параметры

 _Улконнектион_
  
> возврата Номер регистрационного подключения, возвращенного при вызове **имслогон:: Advise**.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Замечания

Поставщики хранилища сообщений реализуют метод **имслогон::** Unadvise для освобождения указателя на объект приемника уведомлений, переданный в параметре _Лпадвисесинк_ предыдущего вызова **имслогон:: Advise**, отменяя уведомление зарегистрировал. При отмене указателя на объект приемника уведомлений вызывается метод " [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) " объекта. Как правило, **выпуск** вызывается во время вызова метода unadvise. **** Тем не менее, если другой поток находится в процессе вызова метода [имапиадвисесинк:: OnNotify](imapiadvisesink-onnotify.md) для объекта приемника уведомлений, вызов **освобождения** задерживается до возвращения метода **OnNotify** . 
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

