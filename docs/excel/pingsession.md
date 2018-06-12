---
title: PingSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4646659b-f932-4d11-a46f-4231bb397243
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 165be9eada54b2030471fc10e7a0bf0c7dcc7c8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807328"
---
# <a name="pingsession"></a>PingSession

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Проверяет, допустим ли сеанс. Эта функция обычно вызывается, когда Excel необходимо определить, если ранее возвращенные сеанс остается активным и можно использовать.
  
```cpp
int PingSession(int SessionId)
```

## <a name="parameters"></a>Parameters

_Код сеанса_
  
> Идентификатор сеанса для проверки связи. Это значение должно соответствовать идентификатор, который возвращает предыдущего вызова [метод OpenSession](opensession.md).
    
## <a name="return-value"></a>������������ ��������

**xlHpcRetSuccess** Если аргумент _SessionId_ является допустимым; в противном случае — **xlHpcRetInvalidSessionId**.
  
## <a name="see-also"></a>См. также

- [Метод OpenSession](opensession.md)
- [Функции соединителя кластера Excel](excel-cluster-connector-functions.md)

