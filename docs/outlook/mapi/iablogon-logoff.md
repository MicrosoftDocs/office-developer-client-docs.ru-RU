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
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808727"
---
# <a name="iablogonlogoff"></a>IABLogon::Logoff

  
  
**Относится к**: Outlook 
  
Запускает процесс выхода из системы.
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Процесс выхода из системы успешно инициировано.
    
## <a name="remarks"></a>Замечания

Процесс выхода из системы обычно запускается, когда клиент вызывает метод [IMAPISession::Logoff](imapisession-logoff.md) , чтобы завершить сеанс. MAPI затем вызывает метод **IABLogon::Logoff** каждой адресной книге для начала процесса выхода из системы. 
  
Метод **IABLogon::Logoff** выполняет следующие действия: 
  
- Освобождает все открытые объекты, такие как вложенными объектами или объекта состояния.
    
- Освобождает объект поддержки поставщика.
    
Дополнительные сведения о процессе logoff поставщиками адресных книг видеть [Завершает работу поставщика услуг](shutting-down-a-service-provider.md).
  
## <a name="see-also"></a>См. также



[IABProvider::Logon](iabprovider-logon.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

