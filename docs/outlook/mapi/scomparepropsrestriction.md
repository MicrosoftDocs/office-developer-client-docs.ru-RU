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
  
Описывает ограничение свойства Compare, которое проверяет два свойства с помощью оператора отношения. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a>"Участники"

**релоп**
  
> Оператор отношения, который используется для сравнения двух свойств. Возможны следующие значения:
    
  - RELOP_GE: сравнение выполняется на основе более высокого или равного первого значения.
      
  - RELOP_GT: сравнение выполняется на основе большего первого значения.
      
  - RELOP_LE: сравнение выполняется на основе меньшего или равного первого значения.
      
  - RELOP_LT: сравнение выполняется с использованием меньшего значения.
      
  - RELOP_NE: сравнение выполняется на основе неодинаковых значений.
      
  - RELOP_RE: сравнение выполняется на основе значений LIKE (регулярное выражение).
      
  - RELOP_EQ: сравнение выполняется на основе равных значений.
    
**ulPropTag1**
  
> Тег свойства первого сравниваемого свойства. 
    
**ulPropTag2**
  
> Тег свойства второго свойства, которое требуется сравнить.
    
## <a name="remarks"></a>Примечания

Порядок сравнения _(тег свойства 1) (оператор отношения) (тег свойства 2)_. Сравниваемые свойства должны относиться к одному и тому же типу. Попытка сравнить свойства различных типов приводит к тому, что MAPI или поставщик услуг возвращает значение ошибки MAPI_E_TOO_COMPLEX из метода [IMAPITable](imapitableiunknown.md) , для которого структура передается в качестве параметра. 
  
Результат ограничения значения свойства Compare не определен, если одно или оба свойства не существуют. Если клиенту требуется строго определенное поведение для такого ограничения и не известно, существует ли свойство (например, это не обязательный столбец таблицы), следует **создать ограничение свойства** Compare с ограничением EXISTS, чтобы присоединиться к ограничению свойства Compare. Используйте структуру [сексистрестриктион](sexistrestriction.md) , чтобы определить ограничение exist и структуру [сандрестриктион](sandrestriction.md) для **определения ограничения.** 
  
Свойства, указанные в членах **ulPropTag1** и **ulPropTag2** , могут быть многозначными, если поставщик услуг поддерживает ее. 
  
Для получения дополнительных сведений о структуре и ограничениях **скомпарепропсрестриктион** в целом ознакомьтесь с [ограничениями](about-restrictions.md).
  
## <a name="see-also"></a>См. также

- [SBitMaskRestriction](sbitmaskrestriction.md)
- [SRestriction](srestriction.md)
- [Структуры MAPI](mapi-structures.md)

