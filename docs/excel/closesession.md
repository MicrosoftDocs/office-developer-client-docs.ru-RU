---
title: CloseSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2c2371c8-b0e0-4992-b7ac-3949eadf1ebe
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8f7398ed9d5edfbf1615930874a800d8835487
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807152"
---
# <a name="closesession"></a>CloseSession

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Завершает сеанс в кластере.
  
```cpp
int CloseSession(int SessionId)
```

## <a name="parameters"></a>Параметры

_Код сеанса_
  
> Идентификатор сеанса, чтобы закрыть. Это значение должно соответствовать значение, возвращенное [метод OpenSession](opensession.md).
    
## <a name="return-value"></a>������������ ��������

**xlHpcRetSuccess** при закрытии сеанса; **xlHpcRetInvalidSessionId** Если недопустимый _SessionId_ аргумент; **xlHpcRetCallFailed** на других ошибок. 
  
## <a name="see-also"></a>См. также

- [OpenSession](opensession.md)
- [Функции для работы с соединителями кластеров Excel](excel-cluster-connector-functions.md)

