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
  
Описывает ограничение свойства, которое используется для сравнения константы со значением свойства.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
```cpp
typedef struct _SPropertyRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  LPSPropValue lpProp;
} SPropertyRestriction;

```

## <a name="members"></a>"Участники"

**релоп**
  
> Оператор отношения, который будет использоваться при поиске. Возможны следующие значения:
    
  - RELOP_GE: сравнение выполняется на основе более высокого или равного первого значения.
        
  - RELOP_GT: сравнение выполняется на основе большего первого значения.
        
  - RELOP_LE: сравнение выполняется на основе меньшего или равного первого значения.
        
  - RELOP_LT: сравнение выполняется с использованием меньшего значения.
        
  - RELOP_NE: сравнение выполняется на основе неодинаковых значений.
        
  - RELOP_RE: сравнение выполняется на основе значений LIKE (регулярное выражение).
        
  - RELOP_EQ: сравнение выполняется на основе равных значений.
    
**улпроптаг**
  
> Тег свойства, определяющий свойство, которое требуется сравнить. 
    
**лппроп**
  
> Указатель на структуру [спропвалуе](spropvalue.md) , которая содержит значение константы, которое будет использоваться при сравнении. 
    
## <a name="remarks"></a>Примечания

Структура **спропертирестриктион** содержит два тега свойств. Один находится в элементе **улпроптаг** , а другой — в элементе **улпроптаг** структуры **Спропвалуе** , на которую указывает **лппроп**. Для MAPI требуются поля "идентификатор свойства" и "тип свойства". **Улпроптаг** в **спропертирестриктион** — это свойство, для которого выполняется сравнение, а указатель **Лппроп** **спропертирестриктион** к типу **улпроптаг** **спропвалуе** указывает, как интерпретируются значения членов объединения **лппроп** . Два типа свойств должны быть совпадают, иначе значение ошибки MAPI_E_TOO_COMPLEX возвращается, если ограничение используется при вызове [IMAPITable:: restrict](imapitable-restrict.md) или [IMAPITable:: FindRow](imapitable-findrow.md). 
  
Порядок сравнения: _(значение свойства) (оператор отношения) (постоянное значение)_.
  
Если ограничение свойства передается в **IMAPITable:: Restricts** или **IMAPITable:: FindRow** , а свойство Target не существует, результаты ограничения не определены. Создавая **ограничение,** которое присоединяется к ограничению свойств с ограничением **Exists** , вызывающий абонент может гарантировать точный результат. Используйте структуру [сексистрестриктион](sexistrestriction.md) , чтобы определить ограничение **exist** и структуру [сандрестриктион](sandrestriction.md) для **определения ограничения.** 
  
Теги свойств с несколькими значениями можно использовать в ограничениях свойств, если поставщик услуг, реализующий эту таблицу, поддерживает их. Если поддерживается, можно использовать теги свойств с несколькими значениями везде. 
  
Теги свойств с несколькими значениями можно использовать в следующих методах:
  
- [IMAPIProp::SetProps](imapiprop-setprops.md)
    
- [IMAPIProp::GetProps](imapiprop-getprops.md)
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
- [IMAPITable::SortTable](imapitable-sorttable.md)
    
- [IMAPITable::Restrict](imapitable-restrict.md)
    
> [!IMPORTANT]
> В важном случае, если два тега свойства не совпадают, то в случае ограничения для свойства с несколькими значениями. В этом случае должны быть соблюдены следующие условия. > если тип свойства **улпроптаг** объекта **спропертирестриктион** содержит флаг битов многозначного многозначного типа MV_FLAG (0x1000), тип свойства **улпроптаг** **спропвалуе** должен быть равен предыдущему минусу MV_FLAG разрядного флага, то есть обратному значению. > например, чтобы ограничить использование настраиваемых строкового свойства с несколькими значениями, например категории с тегом свойства для свойства 0x8012101f, то есть PROP_TAG (MV_FLAG | PT_UNICODE, 0x8012)), соответствующий **спропертирестриктион** будет выглядеть следующим образом. >  `SPropertyRestriction.ulPropTag = 0x8012101f; // attempt to restrict a MultiValue property`>  `SPropertyRestriction.lpProp->ulPropTag = 0x8012001f; // the lpszW member of the Value property is valid`>  `SPropertyRestriction.lpProp.Value->lpszW = L"My Category";`> Обратите внимание, что если тип свойства **улпроптаг** объекта **спропвалуе** содержит MV_FLAG битовый флаг, скорее всего возвращается MAPI_E_TOO_COMPLEX. 
  
Более подробную информацию о структуре **спропертирестриктион** можно узнать в статье [ограничения](about-restrictions.md). 
  
## <a name="see-also"></a>См. также

- [SExistRestriction](sexistrestriction.md)
- [SAndRestriction](sandrestriction.md)
- [SPropValue](spropvalue.md)
- [SRestriction](srestriction.md)
- [IMAPITable::FindRow](imapitable-findrow.md)
- [IMAPITable::Restrict](imapitable-restrict.md)
- [Структуры MAPI](mapi-structures.md)

