---
title: иксплогонидле
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
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436050"
---
# <a name="ixplogonidle"></a>IXPLogon::Idle

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает на то, что система находится в режиме бездействия, что позволяет поставщику транспорта выполнять операции с низким приоритетом.
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов выполнен успешно и вернул ожидаемое значение или значения.
    
## <a name="remarks"></a>Примечания

Диспетчер очереди MAPI периодически вызывает метод **иксплогон:: Idle** при запросе, когда система простаивает, передав флаг XP_LOGON_SP в вызове метода [Иксппровидер:: транспортлогон](ixpprovider-transportlogon.md) , который открыл текущий сеанс. Иногда при простое системы поставщик транспорта может выполнять фоновые операции, которые не подходят для других вызовов, или которые должны выполняться на регулярной основе. 
  
## <a name="see-also"></a>См. также



[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

