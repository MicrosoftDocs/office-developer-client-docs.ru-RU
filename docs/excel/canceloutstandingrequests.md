---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 882458ab096cbced8e0635dab65fe0b1d680388f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414720"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Информирует соединители кластера о том, что Excel вычисление отменено, и поэтому все ожидающих вызовы функций в этом сеансе также могут быть отменены (и что Excel не ожидает отозвайки с их результатами).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Parameters

_SessionID_
  
> ID сеанса, используемого отмененным вычислением. Это значение соответствует значению, возвращенным [OpenSession.](opensession.md)
    
## <a name="return-value"></a>Возвращаемое значение

**xlHpcRetSuccess,** если аргумент  _SessionId_ действителен; **xlHpcRetInvalidSessionId,** если аргумент  _SessionId_ недействителен; **xlHpcRetCallFailed для** других сбоев. 
  
## <a name="remarks"></a>Примечания

Для повышения производительности необходимо остановить все процессы для сеанса, так как все результаты, полученные после этого вызова, будут отброшены Excel.
  
## <a name="see-also"></a>См. также

- [Функции для работы с соединителями кластеров Excel](excel-cluster-connector-functions.md)

