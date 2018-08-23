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
ms.openlocfilehash: c4a201411e2232a3e5fdcd97dcbc9460f657b12a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578096"
---
# <a name="lpvalfindprop"></a>LpValFindProp

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Настройка поиска для указанного свойства в свойстве.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг.  <br/> |
   
```cpp
LPSPropValue LpValFindProp(
  ULONG ulPropTag,
  ULONG cValues,
  LPSPropValue lpPropArray
);
```

## <a name="parameters"></a>Параметры

 _ulPropTag_
  
> [in] Тег для свойства для поиска в набор свойств, указанное с помощью параметра _lpPropArray_ . 
    
 _cValues_
  
> [in] Число свойств в набор свойств, указанное с помощью параметра _lpPropArray_ . 
    
 _lpPropArray_
  
> [in] Массив структур **SPropValue** , который определяет свойства для поиска. 
    
## <a name="return-value"></a>������������ ��������

Функция **LpValFindProp** возвращает структуру **SPropValue** , который определяет свойство, которое сопоставляется входного свойства tag, или значение NULL, если нет соответствия. 
  
## <a name="remarks"></a>Замечания

Функция **LpValFindProp** идентична **PpropFindProp**.
  
## <a name="see-also"></a>См. также



[PpropFindProp](ppropfindprop.md)
  
[SPropValue](spropvalue.md)

