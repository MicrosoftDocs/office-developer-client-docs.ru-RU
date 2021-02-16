---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 49e6c8254cbd527635685c3f974da57ee3ac82a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411794"
---
# <a name="fbadrowset"></a>FBadRowSet

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Проверяет все строки таблиц, включенные в набор строк таблицы.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapival.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Поставщики услуг  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a>Параметры

 _lpRowSet_
  
> [in] Указатель на [структуру SRowSet,](srowset.md) определяя набор строк для проверки. Если указатель имеет NULL, структура недействительна. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Строка указанного набора строк недействительна или сама строка недействительна. 
    
FALSE 
  
> Строки указанного набора строк и сам набор строк являются допустимым.
    
## <a name="see-also"></a>См. также



[FBadRow](fbadrow.md)

