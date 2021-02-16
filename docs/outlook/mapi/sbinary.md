---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 38263f46ccb50e1836f31d457f54f52abca7ce9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407846"
---
# <a name="sbinary"></a>SBinary

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает свойство типа PT_BINARY.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a>"Участники"

 **cb**
  
> Количество в **lpb-члене.** 
    
 **lpb**
  
> Указатель на PT_BINARY свойства.
    
## <a name="remarks"></a>Примечания

Сведения о типах свойств см. в обзоре [типов свойств MAPI.](mapi-property-type-overview.md)
  
## <a name="see-also"></a>См. также



[SPropValue](spropvalue.md)


[Структуры MAPI](mapi-structures.md)

