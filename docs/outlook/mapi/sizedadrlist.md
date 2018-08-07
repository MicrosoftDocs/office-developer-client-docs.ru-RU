---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 13dad61176a877295069317e4a5b51888b01bebb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812284"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Относится к**: Outlook 
  
Определяет структуру [ADRLIST](adrlist.md) с указанным именем, содержащий указанное число [ADRENTRY](adrentry.md) структуры. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные структуры:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Параметры

__centries_
  
> Число структур **ADRENTRY** должны быть включены в новой структуры **ADRLIST** . 
    
_имя_
  
> Имя для новой структуры **ADRLIST** . 
    
## <a name="remarks"></a>Замечания

Макрос **SizedADRLIST** позволяет определить список получателей, который имеет явные границы, когда известны требования к длине массива. Приведенный ниже код показано, как приведения результатов макроса **SizedADRLIST** в структуре указатель **ADRLIST** : 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>См. также

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

