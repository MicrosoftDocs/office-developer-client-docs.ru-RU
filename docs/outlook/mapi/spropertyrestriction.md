---
title: SPropertyRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropertyRestriction
api_type:
- COM
ms.assetid: 2bbf13e9-05b3-4498-8e08-d9e07505190d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 29d392eba530126e06a672c10044c5b4df0618c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406089"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение свойства, используемого для совпадения константы со значением свойства.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a>"Участники"

**relop**
  
> Реляционный оператор, который будет использоваться в поиске. Возможные значения:
    
  - RELOP_GE: сравнение основано на большем или равном первом значении.
        
  - RELOP_GT: сравнение основано на большем первом значении.
        
  - RELOP_LE: сравнение основано на меньшем или равном первом значении.
        
  - RELOP_LT: сравнение основано на меньшем первом значении.
        
  - RELOP_NE: сравнение основано на значениях значений значений.
        
  - RELOP_RE: сравнение основано на значениях LIKE (регулярного выражения).
        
  - RELOP_EQ: сравнение основано на одинаковых значениях.
    
**ulPropTag**
  
> Тег свойства, определяющий свойство, для который необходимо сравнить. 
    
**lpProp**
  
> Указатель на [структуру SPropValue,](spropvalue.md) которая содержит константные значения, которые будут использоваться при сравнении. 
    
## <a name="remarks"></a>Примечания

В структуре **SPropertyRestriction** имеется два тега свойств. Один из них находится в члене **ulPropTag,** а другой — в члене **ulPropTag** структуры **SPropValue,** на который указывает **lpProp.** MAPI требует как поля идентификатора свойства, так и поля типа свойства. **ulPropTag** в **SPropertyRestriction** — это свойство, совпаное, а указатель **lpProp** **SPropertyRestriction** на тип **ulPropTag** **SPropValue** указывает, как интерпретируются значения членов объединения **lpProp.** Два типа свойств должны совпадать, иначе значение ошибки MAPI_E_TOO_COMPLEX возвращается при вызове [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md). 
  
Порядок сравнения : _(значение свойства) (реляционный оператор) (постоянное значение)._
  
Когда ограничение свойства передается в **IMAPITable::Restrict** или **IMAPITable::FindRow** и целевое свойство не существует, результаты ограничения не будут неопределенными. Создав ограничение **AND,** которое присоединяется к ограничению свойств с ограничением **EXIST,** вызываемая может получить точные результаты. Используйте [структуру SExistRestriction](sexistrestriction.md) для определения ограничений **EXIST** и [SAndRestriction](sandrestriction.md) для определения **ограничения AND.** 
  
Теги свойств с несколькими значениями можно использовать в ограничениях свойств, если поставщик услуг, реализующий таблицу, поддерживает их. При поддержке теги свойств с несколькими значениями можно использовать везде, где можно использовать теги свойств с одним значением. 
  
Теги свойств с несколькими значениями можно использовать в следующих методах:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Заметным случаем, когда два тега свойств не будут совпадать, является ограничение свойства с несколькими значениями. В этом случае должно быть истинным следующее: > Если тип свойства **ulPropTag** **SPropertyRestriction** содержит битовый флаг типа многозначного свойства MV_FLAG (0x1000), тип свойства **ulPropTag** **SPropValue** должен совпадать с прежним без флага бита MV_FLAG, то есть его обратного. > Например, чтобы ограничить использование настраиваемого свойства строки с несколькими значениями, например категории с тегом свойства 0x8012101f, то есть PROP_TAG(MV_FLAG|PT_UNICODE, 0x8012)), соответствующий **объект SPropertyRestriction** будет выглядеть следующим образом. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> обратите внимание, что если тип свойства **ulPropTag** **SPropValue** содержит флаг MV_FLAG бита, вероятно, возвращается MAPI_E_TOO_COMPLEX. 
  
Дополнительные сведения о структуре **SPropertyRestriction** см. в [подпрограмме "Об ограничениях".](about-restrictions.md) 
  
## <a name="see-also"></a>См. также

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Структуры MAPI](mapi-structures.md)

