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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348876"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выйдите из службы хранения сообщений. 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulFlags_
  
> [in] Зарезервировано; должен быть указателем на ноль.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>Примечания

Поставщики store сообщений реализуют метод **IMSLogon::Logoff** для принудительного отключения поставщика. **IMSLogon::Logoff** вызван в следующих ситуациях: 
  
- Хотя MAPI отключает клиент после вызова метода [IMAPISession::Logoff.](imapisession-logoff.md) 
    
- Хотя MAPI отключается от поставщика store сообщений. В этом случае **IMSLogon::Logoff** называется как часть обработки MAPI метода [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) объекта поддержки, создаваемого поставщиком хранилищ сообщений при обработке вызова метода [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) или **IUnknown::Release** для объекта хранилищ сообщений. 
    
## <a name="see-also"></a>См. также



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

