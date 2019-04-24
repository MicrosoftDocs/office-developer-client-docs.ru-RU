---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310999"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Информирует соединитель кластера о том, что вычисление Excel было отменено, поэтому все незавершенные вызовы функций в этом сеансе также могут быть отменены (и приложение Excel не ожидает обратных вызовов с результатами).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Параметры

_SessionID_
  
> Идентификатор сеанса, используемого отмененным вычислением. Это значение соответствует значению, возвращенному параметром [опенсессион](opensession.md).
    
## <a name="return-value"></a>Возвращаемое значение

**кслхпкретсукцесс** , если аргумент _SessionID_ является допустимым; **кслхпкретинвалидсессионид** , если аргумент _SessionID_ является недопустимым; **кслхпкреткаллфаилед** для других сбоев. 
  
## <a name="remarks"></a>Замечания

Разработчикам следует остановить все процессы для сеанса, чтобы повысить производительность, так как все результаты, полученные после этого вызова, будут отклонены приложением Excel.
  
## <a name="see-also"></a>См. также

- [Функции для работы с соединителями кластеров Excel](excel-cluster-connector-functions.md)

