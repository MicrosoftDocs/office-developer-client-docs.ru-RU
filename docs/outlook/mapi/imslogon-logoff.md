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
ms.openlocfilehash: e72c947a6e0d4052d3335c3e3cfaf5ffb94da669
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593006"
---
# <a name="imslogonlogoff"></a>IMSLogon::Logoff

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Поставщик хранилища, выходит из системы сообщение. 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpulFlags_
  
> [in] Зарезервировано; должен быть указатель нулевое значение.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> ����� ������� � ������ ��������� ��������� ��� ��������.
    
## <a name="remarks"></a>���������

Поставщики хранилища сообщений реализуйте метод **IMSLogon::Logoff** принудительно завершить работу поставщика хранилища сообщений. **IMSLogon::Logoff** вызывается в следующих ситуациях: 
  
- Во время MAPI выхода клиента после вызова метода [IMAPISession::Logoff](imapisession-logoff.md) . 
    
- Во время выхода поставщика хранилища сообщений MAPI. В этом случае **IMSLogon::Logoff** вызывается в процессе обработки метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) объекта поддержки, который создает поставщика хранилища сообщений во время обработки [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) или **IUnknown MAPI:: Выпуск** вызова метода на объект хранилища сообщений. 
    
## <a name="see-also"></a>См. также



[IMAPISession::Logoff](imapisession-logoff.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)
  
[IMsgStore::StoreLogoff](imsgstore-storelogoff.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

