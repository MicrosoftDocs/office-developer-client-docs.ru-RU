---
title: Иабпровидершутдовн
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Shutdown
api_type:
- COM
ms.assetid: 1fbe6dc1-254b-4557-92c8-9fa42a8efd64
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8b2190f77c7575d3d4f5e25fa0863bec844158bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409785"
---
# <a name="iabprovidershutdown"></a>IABProvider::Shutdown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
ОтМеняет подключение к активному сеансу.
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Параметры

 _Лпулфлагс_
  
> Возврата Резервирования должен быть нулевым указателем.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Подключение было успешно отменено.
    
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Выполните все необходимые задачи в реализации метода **завершения работы** . MAPI вызывает метод **завершения работы** только после того, как вы выпускали все объекты входа. 
  
## <a name="see-also"></a>См. также



[IABProvider : IUnknown](iabprovideriunknown.md)

