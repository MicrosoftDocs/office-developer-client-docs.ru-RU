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
ms.openlocfilehash: adccbaf65adec2c517c4890f722198e8262092cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564607"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнение двух значений свойств с помощью указанного оператор сравнения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Параметры

_lpSPropValue1_
  
> [in] Указатель на структуру [SPropValue](spropvalue.md) определение первое значение свойства для сравнения. 
    
_ulRelOp_
  
> [in] Оператор сравнения для использования в сравнении. Допустимые значения структуры [SComparePropsRestriction](scomparepropsrestriction.md) см. 
    
_lpSPropValue2_
  
> [in] Указатель на структуру **SPropValue** определение второе значение свойства для сравнения. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Значения свойств удовлетворяет указанным отношением. 
    
FALSE 
  
> Значения свойств не удовлетворяет указанным отношением.
    
## <a name="remarks"></a>Примечания

Метод сравнения зависит от типы свойств, указанных в определениях свойство [SPropValue](spropvalue.md) . Функции **FPropCompareProp** и [FPropContainsProp](fpropcontainsprop.md) можно использовать для подготовки ограничения для создания таблицы. 
  
Порядок сравнения — _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Если типы свойств значений свойств, которые будут сравниваться не совпадают, функция **FPropCompareProp** возвращает значение FALSE. 
  

