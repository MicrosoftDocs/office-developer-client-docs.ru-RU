---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9186fb14c33d507b8c9ae709a67f1b43e6206d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304139"
---
# <a name="closesession"></a>CloseSession

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Завершает сеанс с кластером.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Параметры

_SessionId_
  
> Идентификатор сеанса, который необходимо закрыть. Это значение должно быть равно значению, возвращенному параметром [опенсессион](opensession.md).
    
## <a name="return-value"></a>Возвращаемое значение

**кслхпкретсукцесс** , если сеанс закрыт; **кслхпкретинвалидсессионид** , если аргумент _SessionID_ является недопустимым; **кслхпкреткаллфаилед** для других сбоев. 
  
## <a name="see-also"></a>См. также

- [OpenSession](opensession.md)
- [Функции для работы с соединителями кластеров Excel](excel-cluster-connector-functions.md)

