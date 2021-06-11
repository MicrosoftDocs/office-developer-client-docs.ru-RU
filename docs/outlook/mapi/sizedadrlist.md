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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Определяет [структуру ADRLIST](adrlist.md) с заданным именем, которое содержит определенное количество [структур ADRENTRY.](adrentry.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанная структура:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Parameters

_ _центрис_
  
> Количество **структур ADRENTRY,** которые будут включены в новую **структуру ADRLIST.** 
    
_ _имя_
  
> Имя новой **структуры ADRLIST.** 
    
## <a name="remarks"></a>Примечания

Макрос **SizedADRLIST** позволяет определить список получателей, который имеет явные границы, когда известны требования к длине массива. В следующем коде показано, как отоадкить результат макроса **SizedADRLIST** в указатель структуры **ADRLIST:** 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>См. также

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Макросы, связанные со структурами](macros-related-to-structures.md)

