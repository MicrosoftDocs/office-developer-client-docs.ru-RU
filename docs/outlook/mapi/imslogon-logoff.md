---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399237"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поставщик хранилища, выходит из системы сообщение. 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulFlags_
  
> [in] Зарезервировано; должен быть указатель нулевое значение.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Поставщики хранилища сообщений реализуйте метод **IMSLogon::Logoff** принудительно завершить работу поставщика хранилища сообщений. **IMSLogon::Logoff** вызывается в следующих ситуациях: 
  
- Во время MAPI выхода клиента после вызова метода [IMAPISession::Logoff](imapisession-logoff.md) . 
    
- Во время выхода поставщика хранилища сообщений MAPI. В этом случае **IMSLogon::Logoff** вызывается в процессе обработки метода [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) объекта поддержки, который создает поставщика хранилища сообщений во время обработки [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) или **IUnknown MAPI:: Выпуск** вызова метода на объект хранилища сообщений. 
    
## <a name="see-also"></a>См. также



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

