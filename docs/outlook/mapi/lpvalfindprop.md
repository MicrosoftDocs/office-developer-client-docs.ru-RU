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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Выполняет поиск указанного свойства в наборе свойств.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Параметры

 _улпроптаг_
  
> возврата Для свойства, которое требуется найти в наборе свойств, указанном с помощью параметра _лппропаррай_ . 
    
 _квалуес_
  
> возврата Количество свойств в наборе свойств, определяемое параметром _лппропаррай_ . 
    
 _лппропаррай_
  
> возврата Массив структур **спропвалуе** , определяющий свойства для поиска. 
    
## <a name="return-value"></a>Возвращаемое значение

Функция **лпвалфиндпроп** возвращает структуру **спропвалуе** , определяющую свойство, которое соответствует тегу входного свойства, или значение null, если совпадение отсутствует. 
  
## <a name="remarks"></a>Примечания

Функция **лпвалфиндпроп** идентична **ппропфиндпроп**.
  
## <a name="see-also"></a>См. также



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

