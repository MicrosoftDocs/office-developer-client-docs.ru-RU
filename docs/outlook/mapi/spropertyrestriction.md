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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает ограничение свойств, которое используется для совпадения константы со значением свойства.
  
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
    
  - RELOP_GE. Сравнение основано на большем или равном первом значении.
        
  - RELOP_GT. Сравнение выполнено на основе более первого значения.
        
  - RELOP_LE. Сравнение основано на меньшем или равном первом значении.
        
  - RELOP_LT. Сравнение выполнено на основе меньшего первого значения.
        
  - RELOP_NE. Сравнение основано на неравных значениях.
        
  - RELOP_RE. Сравнение основано на значениях LIKE (регулярное выражение).
        
  - RELOP_EQ. Сравнение основано на равных значениях.
    
**ulPropTag**
  
> Тег свойства, определяющий свойство, с чем следует сравнивать. 
    
**lpProp**
  
> Указатель на [структуру SPropValue,](spropvalue.md) которая содержит постоянное значение, которое будет использоваться в сравнении. 
    
## <a name="remarks"></a>Примечания

В структуре **SPropertyRestriction** есть два тега свойств. Один находится в **члене ulPropTag,** а другой — в **члене ulPropTag** структуры **SPropValue,** на который указывает **lpProp**. MAPI требует как поля идентификатора свойства, так и поля типа свойства. **ulPropTag** в **SPropertyRestriction** — это свойство, необходимое для совпадения, а указатель **lpProp** **SPropertyRestriction** к типу **SPropTag SPropValue** указывает, как интерпретируются значения членов союза **lpProp.**  Два типа свойств должны совпадать, иначе значение ошибки MAPI_E_TOO_COMPLEX возвращается, когда ограничение используется в вызове [iMAPITable:::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md). 
  
Порядок сравнения _(значение свойства) (реляционный оператор) (постоянное значение)._
  
Когда ограничение свойства передается **в IMAPITable:::Restrict** или **IMAPITable::FindRow** и целевое свойство не существует, результаты ограничения неопределяются. Создав **ограничение AND,** которое присоединяется к ограничению свойств с ограничением **EXIST,** вызываемой может быть гарантирована точность результатов. Чтобы определить ограничение EXIST и [структуру SAndRestriction,](sandrestriction.md) используйте структуру  [SExistRestriction.](sexistrestriction.md)  
  
Теги свойств с несколькими значениями можно использовать в ограничениях свойств, если поставщик услуг, реализующий таблицу, поддерживает их. При поддержке теги свойств с несколькими значениями можно использовать в любом месте, где можно использовать теги свойств с одним значением. 
  
Теги свойств с несколькими значениями можно использовать в следующих методах:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Примечателен случай, когда два тега свойств не совпадают, если они ограничиваются для свойства с несколькими значениями. В этом случае должно быть верно следующее. > Если тип свойства **ulPropTag** **SPropertyRestriction** содержит многозначный флаг типа свойств MV_FLAG (0x1000), тип свойства **ulPropTag** **SPropValue** должен совпадать с прежним минусом флага MV_FLAG бита, то есть обратным. > Например, чтобы ограничить использование нескольких значений настраиваемого свойства строки, например категории с тегом свойства для свойства 0x8012101f, то есть PROP_TAG (MV_FLAG|PT_UNICODE, 0x8012)), соответствующий **SPropertyRestriction** будет отображаться следующим образом. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> обратите внимание, что если тип свойства **ulPropTag** **SPropValue** содержит флаг MV_FLAG бита, вероятно, возвращается MAPI_E_TOO_COMPLEX. 
  
Дополнительные сведения о структуре **SPropertyRestriction** см. в дополнительных [сведениях об ограничениях.](about-restrictions.md) 
  
## <a name="see-also"></a>См. также

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Структуры MAPI](mapi-structures.md)

