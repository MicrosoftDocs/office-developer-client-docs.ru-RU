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
ms.openlocfilehash: 7d588380ccc84f51fe58bb0f092d5287b12b4270
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586538"
---
# <a name="spropertyrestriction"></a>SPropertyRestriction

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Описывает свойства ограничение, которое используется для сопоставления константу со значением свойства.
  
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

## <a name="members"></a>Members

**RelOp**
  
> Оператор, который будет использоваться в поиск. Ниже приведены возможные значения:
    
  - RELOP_GE: Сравнение выполняется на основе на больше или равно первого значения.
        
  - RELOP_GT: Сравнение выполняется на основе на более высокой версии первое значение.
        
  - RELOP_LE: Сравнение выполняется на основе на меньше или равно первого значения.
        
  - RELOP_LT: Сравнение выполняется на основе на меньшим первое значение.
        
  - RELOP_NE: Сравнение выполняется на основе на разные значения.
        
  - RELOP_RE: Сравнение выполняется на основе как значения (регулярное выражение).
        
  - RELOP_EQ: Сравнение выполняется на основе на равные значения.
    
**ulPropTag**
  
> Свойство tag идентификации свойства для сравнения. 
    
**lpProp**
  
> Указатель на структуру [SPropValue](spropvalue.md) , содержащий константа, которая будет использоваться для сравнения. 
    
## <a name="remarks"></a>Замечания

Существует два свойства теги в структуре **SPropertyRestriction** . В элемент **ulPropTag** , а другое — в член **ulPropTag** структуры **SPropValue** , на который указывает **lpProp**. MAPI требуется идентификатор поля и поле типа свойства. **UlPropTag** в **SPropertyRestriction** является свойством для сопоставления и указывает указатель **lpProp** **SPropertyRestriction** **ulPropTag**по типу **SPropValue** как значение члены Объединение **lpProp** интерпретируются. Типы два свойства должны совпадать, в противном случае MAPI_E_TOO_COMPLEX возвращается значение при ограничении удалось вызвать [IMAPITable::Restrict](imapitable-restrict.md) или [IMAPITable::FindRow](imapitable-findrow.md). 
  
Порядок сравнения _(значение свойства) (оператор сравнения) (константа)_.
  
Когда ограничение свойства передается **IMAPITable::Restrict** или **IMAPITable::FindRow** и свойства конечного объекта не существует, результаты ограничение не определено. Путем создания **и** ограничения, объединяющий ограничение свойства ограничению **EXIST** Звонящий может гарантировать точных результатов. Используйте структуру [SExistRestriction](sexistrestriction.md) , чтобы определить ограничение **EXIST** и структуру [SAndRestriction](sandrestriction.md) для определения **и** ограничение. 
  
Многозначное свойство теги можно использовать в ограничений свойств, если их поддерживает поставщик услуг, реализация в таблице. Если поддерживается, многозначное свойство теги можно использовать везде, где можно использовать теги одним значением свойства. 
  
Многозначное свойство теги можно использовать в следующих методов:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> Важные случай, когда теги два свойства могут не соответствовать — Если ограничение для многозначного свойства. В данном случае следующие вопросы должны иметь значение true. > Если тип свойства **ulPropTag** из **SPropertyRestriction** содержит многозначного свойства типа битовый флаг MV_FLAG (0x1000), тип свойства **ulPropTag** из **SPropValue** должна соответствовать бывшая минус MV_ ФЛАГ битовый флаг, то есть его обратное. > Например, чтобы ограничить использование настраиваемой строки многозначного свойства, например категории с тега свойства для свойства 0x8012101f, то есть, PROP_TAG (MV_FLAG | PT_UNICODE 0x8012)), соответствующий **SPropertyRestriction** будет отображаться как следующим образом. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Обратите внимание на то, что если тип свойства **ulPropTag** из **SPropValue** содержит битовый флаг MV_FLAG, скорее всего, возвращается MAPI_E_TOO_COMPLEX. 
  
Дополнительные сведения о структуре **SPropertyRestriction** [О ограничения](about-restrictions.md)см. 
  
## <a name="see-also"></a>См. также

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Структуры MAPI](mapi-structures.md)

