---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7177b2f0f709939b7580fa7abb87490073bb00c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588813"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описывается ограничение свойства сравнения, предназначенный для тестирования два свойства, используя оператор сравнения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>Members

**RelOp**
  
> Оператор сравнения можно использовать для сравнения двух свойств. Ниже приведены возможные значения:
    
  - RELOP_GE: Сравнение выполняется на основе на больше или равно первого значения.
      
  - RELOP_GT: Сравнение выполняется на основе на более высокой версии первое значение.
      
  - RELOP_LE: Сравнение выполняется на основе на меньше или равно первого значения.
      
  - RELOP_LT: Сравнение выполняется на основе на меньшим первое значение.
      
  - RELOP_NE: Сравнение выполняется на основе на разные значения.
      
  - RELOP_RE: Сравнение выполняется на основе как значения (регулярное выражение).
      
  - RELOP_EQ: Сравнение выполняется на основе на равные значения.
    
**ulPropTag1**
  
> Свойство tag первого свойства для сравнения. 
    
**ulPropTag2**
  
> Свойство tag второго свойства для сравнения.
    
## <a name="remarks"></a>Замечания

Порядок сравнения _(тег свойства (1) (оператор сравнения) (тег свойства 2)_. Свойства для сравнения значения одного типа. Попытка сравнить свойства различных типов приводит MAPI или поставщик услуг для возврата значения ошибка MAPI_E_TOO_COMPLEX из метода [IMAPITable](imapitableiunknown.md) , к которому структура передается как параметр. 
  
В результате ограничение значение свойства сравнения не определен, когда один или оба свойства не существуют. Когда клиент требует некорректно для подобных ограничений и не проверьте, существует ли свойство, (например, это не обязательный столбец таблицы) его необходимо создать **и** ограничения для присоединения к ограничений свойств сравнение с exist ограничение. Используйте структуру [SExistRestriction](sexistrestriction.md) , чтобы определить ограничение exist и структуру [SAndRestriction](sandrestriction.md) для определения **и** ограничение. 
  
Свойства, указанные в разделе участники **ulPropTag1** и **ulPropTag2** может быть поддерживающий несколько значений, если поставщик услуг поддерживает его. 
  
Дополнительные сведения о структуре **SComparePropsRestriction** и ограничения в целом, обратитесь к разделу [О ограничения](about-restrictions.md).
  
## <a name="see-also"></a>См. также

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Структуры MAPI](mapi-structures.md)

