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

**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение сравнения свойств, которое тестирует два свойства с помощью реляционного оператора. 
  
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
  
> Реляционный оператор для сравнения двух свойств. Возможные значения:
    
  - RELOP_GE: сравнение основано на большем или равном первом значении.
      
  - RELOP_GT: сравнение основано на большем первом значении.
      
  - RELOP_LE: сравнение основано на меньшем или равном первом значении.
      
  - RELOP_LT: сравнение основано на меньшем первом значении.
      
  - RELOP_NE: сравнение основано на значениях значений значений.
      
  - RELOP_RE: сравнение основано на значениях LIKE (регулярного выражения).
      
  - RELOP_EQ: сравнение основано на одинаковых значениях.
    
**ulPropTag1**
  
> Тег свойства первого сравниваемого свойства. 
    
**ulPropTag2**
  
> Тег свойства второго свойства, который необходимо сравнить.
    
## <a name="remarks"></a>Примечания

Порядок сравнения : _(тег свойства 1) (реляционный оператор) (тег свойства 2)._ Сравниваемые свойства должны иметь одинаковый тип. При попытке сравнить свойства различных типов MAPI или поставщик услуг возвращает значение ошибки MAPI_E_TOO_COMPLEX из метода [IMAPITable,](imapitableiunknown.md) в который структура передается в качестве параметра. 
  
Результат ограничения значения свойства сравнения не задается, если одно или оба свойства не существуют. Если клиент требует четкого поведения для такого ограничения и не уверен, существует ли свойство (например, это не обязательное столбец таблицы), он должен создать ограничение **AND,** чтобы присоединиться к ограничению сравнения свойств с ограничением на существование. Используйте [структуру SExistRestriction](sexistrestriction.md) для определения ограничений на существование и [структуру SAndRestriction](sandrestriction.md) для определения **ограничения AND.** 
  
Свойства, указанные в членах **ulPropTag1** и **ulPropTag2,** могут иметь несколько значений, если поставщик услуг поддерживает их. 
  
Дополнительные сведения о структуре **и ограничениях SComparePropsRestriction** в целом см. в сведениях [об ограничениях.](about-restrictions.md)
  
## <a name="see-also"></a>См. также

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Структуры MAPI](mapi-structures.md)

