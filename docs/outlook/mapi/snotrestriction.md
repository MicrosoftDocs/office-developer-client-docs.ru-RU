---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426655"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение **NOT,** которое используется для применения логической **операции NOT** к ограничению. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a>"Участники"

 **ulReserved**
  
> [in] ���������������; ������ ���� ����� ����.
    
 **lpRes**
  
> Указатель на [структуру SRestriction,](srestriction.md) описывающий ограничение, присоединяемую к логическому **оператору NOT.** 
    
## <a name="remarks"></a>Примечания

Дополнительные сведения о структуре **SNotRestriction** см. в дополнительных [сведениях об ограничениях.](about-restrictions.md) 
  
## <a name="see-also"></a>См. также



[SRestriction](srestriction.md)


[Структуры MAPI](mapi-structures.md)

