---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301633"
---
# <a name="opensession"></a>OpenSession

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Создает сеанс, в котором можно выполнить пользовательские функции.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Параметры

_Параметры_
  
> Указатель на строку параметров в Юникоде, разделенных точкой с запятой для сеанса. В Excel этот аргумент не используется.
    
## <a name="return-value"></a>Возвращаемое значение

Идентификатор сеанса, используемый в других вызовах соединителя кластера, если сеанс был успешно создан; в противном случае **кслхпкреткаллфаилед**.
  
## <a name="see-also"></a>См. также

- [Функции для работы с соединителями кластеров Excel](excel-cluster-connector-functions.md)

