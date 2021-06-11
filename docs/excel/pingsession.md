---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0fa5fe57e537a7b8c7d880b934809a6f68ce27a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408364"
---
# <a name="pingsession"></a>PingSession

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Проверяет, является ли сеанс допустимым. Эта функция обычно называется, Excel необходимо определить, активен ли ранее возвращенный ID сеанса и можно ли его использовать.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Parameters

_SessionID_
  
> ID сеанса для ping. Это значение должно совпадать с ИД, возвращенным предыдущим вызовом [в OpenSession.](opensession.md)
    
## <a name="return-value"></a>Возвращаемое значение

**xlHpcRetSuccess,** если аргумент  _SessionId_ действителен; в **противном случае xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>См. также

- [OpenSession](opensession.md)
- [Функции для работы с соединителями кластеров Excel](excel-cluster-connector-functions.md)

