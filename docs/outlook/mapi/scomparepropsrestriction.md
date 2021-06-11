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
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440005"
---
# <a name="scomparepropsrestriction"></a>SComparePropsRestriction

**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение сравнения свойств, которое проверяет два свойства с помощью реляционного оператора. 
  
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

## <a name="members"></a>"Участники"

**relop**
  
> Реляционный оператор для сравнения этих двух свойств. Возможные значения:
    
  - RELOP_GE. Сравнение основано на большем или равном первом значении.
      
  - RELOP_GT. Сравнение выполнено на основе более первого значения.
      
  - RELOP_LE. Сравнение основано на меньшем или равном первом значении.
      
  - RELOP_LT. Сравнение выполнено на основе меньшего первого значения.
      
  - RELOP_NE. Сравнение основано на неравных значениях.
      
  - RELOP_RE. Сравнение основано на значениях LIKE (регулярное выражение).
      
  - RELOP_EQ. Сравнение основано на равных значениях.
    
**ulPropTag1**
  
> Тег свойства первого свойства, который следует сравнить. 
    
**ulPropTag2**
  
> Тег свойства второго свойства, который необходимо сравнить.
    
## <a name="remarks"></a>Примечания

Порядок сравнения _(тег свойства 1) (реляционный оператор) (тег свойства 2)._ Свойства, которые необходимо сравнить, должны иметь один и тот же тип. Попытка сравнить свойства различных типов приводит к возвращению значения MAPI_E_TOO_COMPLEX mapI или поставщика услуг из метода [IMAPITable,](imapitableiunknown.md) к которому структура передается в качестве параметра. 
  
Результат ограничения значения свойства сравнения неопределяется, если одно или оба свойства не существуют. Если клиент требует четкого поведения для такого ограничения и не уверен, существует ли свойство (например, это не обязательно столбец таблицы), он должен создать ограничение **AND,** чтобы присоединиться к ограничению сравнения свойств с ограничением на существование. Используйте [структуру SExistRestriction](sexistrestriction.md) для определения ограничения на существование и [структуры SAndRestriction](sandrestriction.md) для определения **ограничения И.** 
  
Свойства, указанные в **членах ulPropTag1** и **ulPropTag2,** могут быть многоценными, если поставщик услуг поддерживает его. 
  
Дополнительные сведения о структуре **sComparePropsRestriction** и ограничениях в целом см. в этой [информации.](about-restrictions.md)
  
## <a name="see-also"></a>См. также

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Структуры MAPI](mapi-structures.md)

