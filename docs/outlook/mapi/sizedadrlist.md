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
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423463"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет структуру [ADRLIST](adrlist.md) с указанным именем, которая содержит указанное число структур [адрентри](adrentry.md) . 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанная структура:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Параметры

__центриес_
  
> Количество структур **адрентри** , включаемых в новую структуру **ADRLIST** . 
    
__имя_
  
> Имя новой структуры **ADRLIST** . 
    
## <a name="remarks"></a>Примечания

Макрос **сизедадрлист** позволяет определить список получателей с явными границами при известных требованиях к длине массива. В приведенном ниже коде показано, как привести результат выполнения макроса **сизедадрлист** к указателю структуры **ADRLIST** : 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>См. также

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

