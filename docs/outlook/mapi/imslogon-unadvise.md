---
title: IMSLogonUnadvise
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
  
Удаляет регистрацию объекта для уведомления об изменениях в хранилище сообщений, ранее установленных с помощью вызова метода [IMSLogon::Advise.](imslogon-advise.md) 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a>Parameters

 _ulConnection_
  
> [in] Номер регистрационного подключения, возвращаемого по вызову **в IMSLogon::Advise.**
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики магазинов сообщений реализуют метод **IMSLogon::Unadvise,** чтобы освободить указатель для объекта раковины рекомендации, переданного в  _параметре lpAdviseSink_ в предыдущем вызове **в IMSLogon:::Advise,** тем самым отменив регистрацию уведомлений. В рамках отбрасывания указателя к объекту раковины рекомендации используется метод [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) Как правило, **выпуск** вызываем во время вызова **Unadvise.** Однако если другой поток находится в процессе вызова [метода IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) для  объекта раковины рекомендации, вызов выпуска откладывается до тех пор, пока метод **OnNotify** не вернется. 
  
## <a name="see-also"></a>См. также



[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Advise](imslogon-advise.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

