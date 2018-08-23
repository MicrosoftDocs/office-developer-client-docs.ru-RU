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
ms.openlocfilehash: 62911e0dec15002f39fff81e8c517c1cb11d0183
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574743"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

