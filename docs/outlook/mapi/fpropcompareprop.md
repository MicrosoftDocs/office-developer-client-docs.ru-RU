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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнивает два значения свойства с использованием указанного оператора отношения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a>Параметры

_lpSPropValue1_
  
> возврата Указатель на структуру [спропвалуе](spropvalue.md) , определяющую первое значение свойства для сравнения. 
    
_Улрелоп_
  
> возврата Оператор отношения, используемый в сравнении. Допустимые значения приведены в разделе Структура [скомпарепропсрестриктион](scomparepropsrestriction.md) . 
    
_lpSPropValue2_
  
> возврата Указатель на структуру **спропвалуе** , определяющую второе значение свойства для сравнения. 
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Значения свойств соответствуют указанному отношению. 
    
FALSE 
  
> Значения свойств не соответствуют указанному отношению.
    
## <a name="remarks"></a>Примечания

Метод сравнения зависит от типов свойств, указанных в определениях свойств [спропвалуе](spropvalue.md) . Функции **фпропкомпарепроп** и [фпропконтаинспроп](fpropcontainsprop.md) можно использовать для подготовки ограничений для создания таблицы. 
  
Порядок сравнения: _lpSPropValue1_, _ улрелоп _, _ lpSPropValue2 _. Если типы свойств для сравниваемых значений свойств не совпадают, функция **фпропкомпарепроп** ВОЗВРАЩАЕТ значение false. 
  

