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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 69bbed644a8173bf9291ca48a63960f693108318
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808493"
---
# <a name="fpropcompareprop"></a>FPropCompareProp

**Применимо к**: Outlook 
  
Сравнение двух значений свойств с помощью указанного оператор сравнения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Parameters

_lpSPropValue1_
  
> [in] Указатель на структуру [SPropValue](spropvalue.md) определение первое значение свойства для сравнения. 
    
_ulRelOp_
  
> [in] Оператор сравнения для использования в сравнении. Допустимые значения структуры [SComparePropsRestriction](scomparepropsrestriction.md) см. 
    
_lpSPropValue2_
  
> [in] Указатель на структуру **SPropValue** определение второе значение свойства для сравнения. 
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Значения свойств удовлетворяет указанным отношением. 
    
FALSE 
  
> Значения свойств не удовлетворяет указанным отношением.
    
## <a name="remarks"></a>Замечания

Метод сравнения зависит от типы свойств, указанных в определениях свойство [SPropValue](spropvalue.md) . Функции **FPropCompareProp** и [FPropContainsProp](fpropcontainsprop.md) можно использовать для подготовки ограничения для создания таблицы. 
  
Порядок сравнения — _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _. Если типы свойств значений свойств, которые будут сравниваться не совпадают, функция **FPropCompareProp** возвращает значение FALSE. 
  

