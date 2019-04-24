---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Переменная этого типа данных содержит значение свойства, которое относится к типу данных Variant.
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316921"
---
# <a name="acctvariant"></a>ACCT_VARIANT

Переменная этого типа данных содержит значение свойства, которое относится к типу данных Variant.
  
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

## <a name="members"></a>Элементы

_Двтипе_
  
> Тип варианта:
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_хранилищ_
  
> Значение Variant типа DWORD.
    
_пвсз_
  
> Строковое значение Variant.
    
_bin_
  
> Двоичное значение Variant.
    

