---
title: CancelOutstandingRequests
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0de9d4e2-eb3f-40e7-aa24-f430892eb9ec
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 65d4257037b18c8fa68cabe0c08091ec67343fa5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807142"
---
# <a name="canceloutstandingrequests"></a>CancelOutstandingRequests

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Информирует соединитель кластера, вычисления Excel отменена, и поэтому все ожидающие вызовы функций этого сеанса может быть отменен также (и, Excel не ожидается обратных вызовов с их результаты).
  
```cpp
int CancelOutstandingRequests(int SessionId)
```

## <a name="parameters"></a>Parameters

_Код сеанса_
  
> Идентификатор сеанса, используемые отмененные вычислений. Это значение определяет соответствие значение, возвращенное [метод OpenSession](opensession.md).
    
## <a name="return-value"></a>������������ ��������

**xlHpcRetSuccess** Если аргумент _SessionId_ является допустимым; **xlHpcRetInvalidSessionId** Если недопустимый _SessionId_ аргумент; **xlHpcRetCallFailed** на других ошибок. 
  
## <a name="remarks"></a>Замечания

Специалистов по внедрению необходимо остановить все процессы для сеанса для повышения производительности, как никаких результатов, полученных после этот вызов не будет использоваться приложением Excel.
  
## <a name="see-also"></a>См. также

- [Функции соединителя кластера Excel](excel-cluster-connector-functions.md)

