---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416400"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Инициирует процесс входа.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Успешно начался процесс входа.
    
## <a name="remarks"></a>Примечания

Процесс входа обычно начинается, когда клиент вызывает [метод IMAPISession::Logoff](imapisession-logoff.md) для окончания сеанса. Затем MAPI вызывает метод **IABLogon::Logoff** каждого поставщика адресной книги, чтобы запустить процесс входа. 
  
Метод **IABLogon::Logoff** делает следующее: 
  
- Освобождает все открытые объекты, такие как любые подобекты или объект состояния.
    
- Освобождает объект поддержки поставщика.
    
Дополнительные сведения о процессе входа поставщиков адресных книг см. в книге [Shutting Down a Service Provider.](shutting-down-a-service-provider.md)
  
## <a name="see-also"></a>См. также



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

