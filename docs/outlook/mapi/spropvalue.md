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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433530"
---
# <a name="spropvalue"></a>SPropValue

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Описывает свойство MAPI.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Связанные макросы:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>"Участники"

 **улпроптаг**
  
> Тег свойства для свойства. Теги свойств — это 32 — битовые целые числа без знака, состоящие из уникального идентификатора свойства в высоком порядке 16 бит и тип свойства в младших 16 битах.
    
 **двалигнпад**
  
> Зарезервировано для MAPI; не используйте. 
    
 **Значение**
  
> Объединение значений данных, определенное значение, которое определяется типом свойства. В приведенной ниже таблице перечислены типы свойств, элементы объединения, которые следует использовать, и связанные с ними типы данных.
    
|**Тип свойства**|**Значение**|**Тип данных value**|
|:-----|:-----|:-----|
|PT_I2 или PT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 или PT_LONG (со знаком)  <br/> |**l** <br/> |БОЛЬШОМ  <br/> |
|PT_I4 или PT_LONG (без знака)  <br/> |**сертифицирован** <br/> |ULONG  <br/> |
|PT_R4 или PT_FLOAT  <br/> |**флт** <br/> |с плавающей запятой  <br/> |
|PT_R8 или PT_DOUBLE  <br/> |**нажат** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**з** <br/> |короткое целое без знака  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**в** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**метр** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**лпсза** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**bin** <br/> |BYTE [Массив]  <br/> |
|PT_UNICODE  <br/> |**лпсзв** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**лпгуид** <br/> |лпгуид  <br/> |
|PT_I8 или PT_LONGLONG  <br/> |**Li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**мви** <br/> |[SShortArray](sshortarray.md) <br/> |
|PT_MV_LONG  <br/> |**мви** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**мвфлт** <br/> |[SRealArray](srealarray.md) <br/> |
|PT_MV_DOUBLE  <br/> |**мвдбл** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|PT_MV_CURRENCY  <br/> |**мвкур** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|PT_MV_APPTIME  <br/> |**мват** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|PT_MV_SYSTIME  <br/> |**мвфт** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**мвбин** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**мвсза** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|PT_MV_UNICODE  <br/> |**мвсзв** <br/> |[SWStringArray](swstringarray.md) <br/> |
|PT_MV_CLSID  <br/> |**мвгуид** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**мвли** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|PT_NULL или PT_OBJECT  <br/> |**x** <br/> |БОЛЬШОМ  <br/> |
|PT_PTR  <br/> |**лпв** <br/> |ОТМЕНИТЬ\*  <br/> |
   
## <a name="remarks"></a>Примечания

Элемент **улпроптаг** состоит из двух частей: 
  
- Идентификатор в высоком порядке 16 бит.
    
- Тип в 16 младших битах.
    
Идентификатор — это числовое значение в определенном диапазоне. MAPI определяет диапазоны для идентификаторов, описывающих, для чего используется свойство и кто отвечает за его обслуживание. MAPI определяет ограничения для каждого из тегов свойств, которые он поддерживает, в файле заголовка Мапитагс. h.
  
Тип указывает формат значения свойства. MAPI определяет константы для каждого из типов свойств, поддерживаемых в файле заголовка MAPIDEFS. h. 
  
Полный список допустимых диапазонов свойств для идентификаторов и типов свойств представлен в приложении [идентификаторы и типы](property-identifiers-and-types.md) свойств. 
  
Элемент **двалигнпад** используется в качестве заполнения для обеспечения правильного выравнивания на компьютерах, для которых требуется 8-байтное выравнивание для 8-байтовых значений. Разработчики, которые пишут код на такие компьютеры, должны использовать процедуры выделения памяти, которые распределяют массивы **спропвалуе** по 8 байтам. 
  
Для получения дополнительных сведений см. [Обзор типов свойств MAPI](mapi-property-type-overview.md) и [Обновление свойств MAPI](updating-mapi-properties.md). 
  
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

