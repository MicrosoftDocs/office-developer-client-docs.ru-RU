---
title: SContentRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SContentRestriction
api_type:
- COM
ms.assetid: 784c8a5a-493e-48e6-8784-ba8122c76e3d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 87be6df27a3e6729cb514118438521d76a66b30c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423666"
---
# <a name="scontentrestriction"></a>SContentRestriction
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение контента, которое используется для ограничения представления таблицы только теми строками, которые включают столбец со содержимым, совпадающий со строкой поиска. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SContentRestriction
{
  ULONG        ulFuzzyLevel;
  ULONG        ulPropTag;
  LPSPropValue lpProp;
} SContentRestriction;

```

## <a name="members"></a>"Участники"

**ulFuzzyLevel**
  
> Параметры, определяющие уровень точности, который должно применять ограничение контента при проверке совпадения.
    
   Нижние **16** битов члена **ulFuzzyLevel** применяются к свойствам типа PT_BINARY и PT_STRING8 и должны быть задатки одному из следующих значений: 
    
   - FL_FULLSTRING. Чтобы соответствовать, строка поиска **lpProp** должна содержаться в свойстве, идентифицированного **ulPropTag**.
        
   - FL_PREFIX. Чтобы соответствовать, строка поиска **lpProp** должна отображаться в начале свойства, идентифицированного **ulPropTag**. Эти две строки следует сравнивать только с длиной строки поиска, обозначенной **lpProp.** 
        
   - FL_SUBSTRING. Чтобы соответствовать, строка поиска **lpProp** должна содержаться в любом месте свойства, идентифицированного **ulPropTag**. 
        
   Верхние **16** битов члена **ulFuzzyLevel** применяются только к свойствам типа PT_STRING8 и могут быть установлены к следующим значениям в любой комбинации: 
        
   - FL_IGNORECASE. Сравнение должно быть выполнено без рассмотрения случая. 
        
   - FL_IGNORENONSPACE. Сравнение должно игнорировать символы без интервалов, определенных Юникодом, такие как диакритические знаки. 
        
   - FL_LOOSE. Сравнение должно дать вам совпадение по возможности, игнорируя символы дела и не интервалы. 
    
**ulPropTag**
  
> Тег свойства, определяющий свойство строки, проверяемого на наличие строки поиска. 
    
**lpProp**
  
> Указатель на структуру значения свойства, содержащем строковую строку, которую необходимо использовать в качестве строки поиска.
    
## <a name="remarks"></a>Примечания

В структуре **SContentRestriction** есть два тега свойств: один в члене **ulPropTag** и другой в **члене ulPropTag** структуры **SPropValue,** на который указывает **lpProp**. В обоих тегах MAPI требует только поля типа свойств и игнорирует поле идентификатора свойств. Однако эти два типа свойств должны соответствовать, иначе значение ошибки MAPI_E_TOO_COMPLEX возвращается, когда ограничение используется в [вызове IMAPITable:::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md). 
  
Значения, FL_FULLSTRING, FL_PREFIX и FL_SUBSTRING взаимоисключающие. Можно установить только один из них, и один из них должен быть установлен. Их значения фиксируются, и поставщик должен реализовать их точно так, как определено. Поставщик должен возвращать MAPI_E_TOO_COMPLEX, если он не может поддерживать эти значения. 
  
Значения, FL_IGNORECASE, FL_IGNORENONSPACE и FL_LOOSE независимы. В любом месте от нуля до всех трех из них можно установить. Их определения предоставляются только в качестве ориентира, и поставщик может реализовать свое собственное определенное значение каждого флага. Поставщик не должен возвращать указания на ошибку, если у него нет реализации указанного флага. 
  
Результат ограничения контента, наложенного на свойство, неопределяется, если оно не существует. Если клиент требует четкого поведения для такого ограничения и не уверен, существует ли свойство, например, это не обязательно  столбец таблицы, он должен создать ограничение AND, чтобы присоединиться к ограничению контента с ограничением на существование. Используйте [структуру SExistRestriction](sexistrestriction.md) для определения ограничения на существование и [структуры SAndRestriction](sandrestriction.md) для определения **ограничения И.** 
  
Дополнительные сведения о структуре **SContentRestriction** и ограничениях в целом см. в этой [информации.](about-restrictions.md)
  
## <a name="see-also"></a>См. также

- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [Структуры MAPI](mapi-structures.md)

