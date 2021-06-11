---
title: SAppTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAppTimeArray
api_type:
- COM
ms.assetid: 5a1ff95a-9862-4165-8a70-bd2eeb7fe683
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dee1de19ed61fa4f8edab69152315d77545b01b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430387"
---
# <a name="sapptimearray"></a>SAppTimeArray

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит массив значений времени.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAppTimeArray
{
  ULONG cValues;
  double FAR *lpat;
} SAppTimeArray;

```

## <a name="members"></a>"Участники"

 **cValues**
  
> Количество значений в массиве, на который указывает **член lpat.** 
    
 **lpat**
  
> Указатель на массив значений времени приложения. 
    
## <a name="remarks"></a>Примечания

Структура **SAppTimeArray** используется для определения свойств типа PT_MV_APPTIME. Дополнительные сведения о PT_MV_APPTIME см. [в списке типов свойств.](property-types.md)
  
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

