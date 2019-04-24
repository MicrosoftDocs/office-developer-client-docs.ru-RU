---
title: ACCT_BIN
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5b57296c-61d7-e517-7ab7-44a9cc1f7ffc
description: Переменная этого типа данных содержит двоичное значение.
ms.openlocfilehash: 3dcaaf73a04ddc608e68ca7bd1f801d0a5d99bb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316914"
---
# <a name="acctbin"></a>ACCT_BIN

Переменная этого типа данных содержит двоичное значение.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct { 
    DWORDcb; 
    BYTE * pb; 
} ACCT_BIN; 

```

## <a name="members"></a>Элементы

_cb_
  
> Число байтов, на которые _Pb_ указывает. 
    
_pb_
  
> Указатель на двоичную информацию.
    

