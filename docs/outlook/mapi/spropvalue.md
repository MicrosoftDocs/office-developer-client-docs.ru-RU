---
title: SPropValue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropValue
api_type:
- COM
ms.assetid: faf795a2-84db-432d-a05f-082f25a5cab5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c7f4e8835831af6277cef134bf3961e9928cba33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326588"
---
# <a name="spropvalue"></a>SPropValue

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Описывает свойство MAPI.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанные макросы:  <br/> |[Чанже_проп_типе](change_prop_type.md), [мви_проп](mvi_prop.md), [проп_ид](prop_id.md), [проп_таг](prop_tag.md), [проп_типе](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>Members

 **Улпроптаг**
  
> Тег свойства для свойства. Теги свойств — это 32 — битовые целые числа без знака, состоящие из уникального идентификатора свойства в высоком порядке 16 бит и тип свойства в младших 16 битах.
    
 **Двалигнпад**
  
> ЗаРезервировано для MAPI; не используйте. 
    
 **Значение**
  
> Объединение значений данных, определенное значение, которое определяется типом свойства. В приведенной ниже таблице перечислены типы свойств, элементы объединения, которые следует использовать, и связанные с ними типы данных.
    
|**Тип свойства**|**Значение**|**Тип данных value**|
|:-----|:-----|:-----|
|PT_I2 или ПТ_ШОРТ  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 или ПТ_ЛОНГ (со знаком)  <br/> |**l** <br/> |БОЛЬШОМ  <br/> |
|PT_I4 или ПТ_ЛОНГ (без знака)  <br/> |**сертифицирован** <br/> |ULONG  <br/> |
|PT_R4 или ПТ_ФЛОАТ  <br/> |**ФЛТ** <br/> |с плавающей запятой  <br/> |
|PT_R8 или ПТ_ДАУБЛЕ  <br/> |**нажат** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**з** <br/> |короткое целое без знака  <br/> |
|ПТ_КУРРЕНЦИ  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|ПТ_АППТИМЕ  <br/> |**в** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**метр** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**Лпсза** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**bin** <br/> |BYTE [Массив]  <br/> |
|PT_UNICODE  <br/> |**Лпсзв** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**лпгуид** <br/> |ЛПГУИД  <br/> |
|PT_I8 или ПТ_ЛОНГЛОНГ  <br/> |**Li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**МВИ** <br/> |[SShortArray](sshortarray.md) <br/> |
|ПТ_МВ_ЛОНГ  <br/> |**МВИ** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**Мвфлт** <br/> |[SRealArray](srealarray.md) <br/> |
|ПТ_МВ_ДАУБЛЕ  <br/> |**Мвдбл** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|ПТ_МВ_КУРРЕНЦИ  <br/> |**Мвкур** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|ПТ_МВ_АППТИМЕ  <br/> |**Мват** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|ПТ_МВ_СИСТИМЕ  <br/> |**Мвфт** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**Мвбин** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**Мвсза** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|ПТ_МВ_УНИКОДЕ  <br/> |**Мвсзв** <br/> |[SWStringArray](swstringarray.md) <br/> |
|ПТ_МВ_КЛСИД  <br/> |**Мвгуид** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**Мвли** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|ПТ_НУЛЛ или ПТ_ОБЖЕКТ  <br/> |**x** <br/> |БОЛЬШОМ  <br/> |
|ПТ_ПТР  <br/> |**лпв** <br/> |ОТМЕНИТЬ\*  <br/> |
   
## <a name="remarks"></a>Замечания

Элемент **улпроптаг** состоит из двух частей: 
  
- Идентификатор в высоком порядке 16 бит.
    
- Тип в 16 младших битах.
    
Идентификатор — это числовое значение в определенном диапазоне. MAPI определяет диапазоны для идентификаторов, описывающих, для чего используется свойство и кто отвечает за его обслуживание. MAPI определяет ограничения для каждого из тегов свойств, которые он поддерживает, в файле заголовка Мапитагс. h.
  
Тип указывает формат значения свойства. MAPI определяет константы для каждого из типов свойств, поддерживаемых в файле заголовка MAPIDEFS. h. 
  
Полный список допустимых диапазонов свойств для идентификаторов и типов свойств представлен в приложении идентификаторы [и типы](property-identifiers-and-types.md) свойств. 
  
Элемент **двалигнпад** используется в качестве заполнения для обеспечения правильного выравнивания на компьютерах, для которых требуется 8-байтное выравнивание для 8-байтовых значений. Разработчики, которые пишут код на такие компьютеры, должны использовать процедуры выделения памяти, которые распределяют массивы **спропвалуе** по 8 байтам. 
  
Для получения дополнительных сведений см. [Обзор типов свойств MAPI](mapi-property-type-overview.md) и [Обновление свойств MAPI](updating-mapi-properties.md). 
  
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

