---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Переменная этого типа данных содержит значение свойства, которое имеет тип данных variant.
ms.openlocfilehash: c85af4bd4fefffb4fadf671bb7cf5b7f072d5e95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807680"
---
# <a name="acctvariant"></a>ACCT_VARIANT

Переменная этого типа данных содержит значение свойства, которое имеет тип данных variant.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct 
    { 
        DWORD dwType; 
        union  
            { 
            DWORD dw; 
            WCHAR *pwsz; 
            ACCT_BIN bin; 
            } Val; 
    } ACCT_VARIANT; 

```

## <a name="members"></a>Members

_dwType_
  
> Тип variant:
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_DW_
  
> Значение DWORD значение типа variant.
    
_pwsz_
  
> Строковое значение типа variant.
    
_корзины_
  
> Двоичное значение типа variant.
    

