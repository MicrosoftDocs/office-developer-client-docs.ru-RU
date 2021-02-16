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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408126"
---
# <a name="acct_bin"></a>ACCT_BIN

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
  
> Количествобайт, на которое _указывает PB._ 
    
_pb_
  
> Указатель на двоичные данные.
    

