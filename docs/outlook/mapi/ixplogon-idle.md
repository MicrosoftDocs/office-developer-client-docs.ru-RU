---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 75607550f1d6085a670ad997238994400e08f7bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809630"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**Относится к**: Outlook 
  
Указывает, что система не занята, включив поставщика транспорта для выполнения операций с низким приоритетом.
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>���������

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Вызов успешно и возвращается ожидаемым значением или значения.
    
## <a name="remarks"></a>Замечания

Диспетчер очереди MAPI периодически вызывает метод **IXPLogon::Idle** , если запрошен периоды времени, когда система не занята, передав флаг XP_LOGON_SP в вызове метода [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) , которая открыта в текущем сеансе. В некоторых случаях, когда система не занята, поставщика транспорта можно выполнить фоновых операций, которые не соответствуют во время других вызовов или, необходимо повторить на регулярной основе. 
  
## <a name="see-also"></a>См. также



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

