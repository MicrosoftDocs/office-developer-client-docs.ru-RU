---
title: Метод OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807315"
---
# <a name="opensession"></a>Метод OpenSession

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Создает сеанс, в котором могут быть выполнены определенные пользователем функции.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Parameters

_Параметры_
  
> Указатель, разделенных точкой с запятой строку ЮНИКОДА параметров для этого сеанса. Excel не использует этот аргумент.
    
## <a name="return-value"></a>������������ ��������

Идентификатор сеанса для использования в других вызовов соединитель кластера, если сеанс был успешно создан; в противном случае — **xlHpcRetCallFailed**.
  
## <a name="see-also"></a>См. также

- [Функции соединителя кластера Excel](excel-cluster-connector-functions.md)

