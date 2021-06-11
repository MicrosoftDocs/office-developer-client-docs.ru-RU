---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427159"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает два значения свойств с помощью указанного реляционного оператора. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Parameters

_lpSPropValue1_
  
> [in] Указатель на [структуру SPropValue,](spropvalue.md) определяющей первое значение свойства для сравнения. 
    
_ulRelOp_
  
> [in] Реляционный оператор для сравнения. Допустимые значения см. в структуре [SComparePropsRestriction.](scomparepropsrestriction.md) 
    
_lpSPropValue2_
  
> [in] Указатель на **структуру SPropValue,** определяющей второе значение свойства для сравнения. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Значения свойств удовлетворяют указанному отношению. 
    
FALSE 
  
> Значения свойств не удовлетворяют указанному отношению.
    
## <a name="remarks"></a>Примечания

Метод сравнения зависит от типов свойств, указанных в [определениях свойств SPropValue.](spropvalue.md) Функции **FPropCompareProp** и [FPropContainsProp](fpropcontainsprop.md) можно использовать для подготовки ограничений для создания таблицы. 
  
Порядок сравнения  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Если сравниваемые типы свойств не совпадают, функция **FPropCompareProp** возвращает FALSE. 
  

