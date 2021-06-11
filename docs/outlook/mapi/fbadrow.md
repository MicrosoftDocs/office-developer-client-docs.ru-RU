---
title: FBadRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRow
api_type:
- COM
ms.assetid: 205d00df-488d-4888-8782-a1f70f54d720
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 153bcbfd87ea9e85d834cba2fd9028e98fa25750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420621"
---
# <a name="fbadrow"></a>FBadRow

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет строку в таблице.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
ULONG FBadRow(
  LPSRow lprow
);
```

## <a name="parameters"></a>Параметры

 _lprow_
  
> [in] Указатель на [структуру SRow,](srow.md) определяя строку, которая должна быть проверена. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Указанная строка недействительна.
    
FALSE 
  
> Указанная строка действительна.
    
## <a name="see-also"></a>См. также



[FBadRowSet](fbadrowset.md)

