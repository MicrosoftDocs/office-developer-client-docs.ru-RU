---
title: LpValFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67461a38-bb60-467b-901b-39c645e764f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fa1588d4a58824b57c132fc8e66a0abd6e9acd0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419641"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поиск указанного свойства в наборе свойств.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Parameters

 _ulPropTag_
  
> [in] Тег свойства для поиска в наборе свойств, указанный _параметром lpPropArray._ 
    
 _cValues_
  
> [in] Количество свойств в наборе свойств, указанных параметром _lpPropArray._ 
    
 _lpPropArray_
  
> [in] Массив **структур SPropValue,** определяя свойства, которые необходимо искать. 
    
## <a name="return-value"></a>Возвращаемое значение

Функция **LpValFindProp** возвращает структуру **SPropValue,** которая определяет свойство, которое соответствует тегу свойства ввода или NULL, если нет совпадения. 
  
## <a name="remarks"></a>Примечания

Функция **LpValFindProp** идентична **функции PpropFindProp.**
  
## <a name="see-also"></a>См. также



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

