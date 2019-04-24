---
title: Иксппровидершутдовн
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.Shutdown
api_type:
- COM
ms.assetid: e2d8a025-c2a3-4edb-b6e4-022e07e854dd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a57a72b413ba412154a27a08244e86b117cbea7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357199"
---
# <a name="ixpprovidershutdown"></a>IXPProvider::Shutdown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
ЗаКрывает поставщик транспорта в определенном порядке.
  
```cpp
HRESULT Shutdown (
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _Лпулфлагс_
  
> [in] ���������������; ������ ���� ����� ����.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Вызов завершился успешно при завершении работы поставщика транспорта.
    
## <a name="remarks"></a>Примечания

Диспетчер очереди MAPI вызывает метод **иксппровидер:: Shutdown** непосредственно перед освобождением объекта поставщика транспорта. Перед **завершением**вызовов Служба MAPI освобождает все объекты входа для поставщика.
  
## <a name="see-also"></a>См. также



[XPProviderInit](xpproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)

