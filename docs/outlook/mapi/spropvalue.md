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
ms.openlocfilehash: f378bdd473410b846328cbe1f911eba9401f88cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812380"
---
# <a name="spropvalue"></a>SPropValue

  
  
**Относится к**: Outlook 
  
Описывает свойство MAPI.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CHANGE_PROP_TYPE](change_prop_type.md), [MVI_PROP](mvi_prop.md), [PROP_ID](prop_id.md), [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>Members

 **ulPropTag**
  
> Свойство tag для свойства. Свойство теги являются целые числа без знака 32-разрядная версия, состоящий из свойство имеет уникальный идентификатор в 16 бит высокого приоритета и тип свойства в 16 бит низкого приоритета.
    
 **dwAlignPad**
  
> Зарезервировано для MAPI; не следует использовать. 
    
 **Значение**
  
> Объединение данных значения определенного значения, зависит от типа свойства. В следующей таблице приведены для каждого типа свойств, члена объединения, который будет использоваться и его тип данных, связанного.
    
|**Тип свойства**|**Значение**|**Тип данных значения**|
|:-----|:-----|:-----|
|PT_I2 или PT_SHORT  <br/> |**я** <br/> |короткое целое  <br/> |
|PT_I4 или PT_LONG (подпись)  <br/> |**l** <br/> |ДЛИННЫЙ  <br/> |
|PT_I4 или PT_LONG (без знака)  <br/> |**ul** <br/> |ULONG  <br/> |
|PT_R4 или PT_FLOAT  <br/> |**Сбой** <br/> |с плавающей запятой  <br/> |
|PT_R8 или PT_DOUBLE  <br/> |**двойной** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |короткое целое число  <br/> |
|PT_CURRENCY  <br/> |**по** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**в** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**FT** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**корзины** <br/> |BYTE [массива]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 или PT_LONGLONG  <br/> |**li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**MVi** <br/> |[SShortArray](sshortarray.md) <br/> |
|PT_MV_LONG  <br/> |**MVI** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**MVflt** <br/> |[SRealArray](srealarray.md) <br/> |
|PT_MV_DOUBLE  <br/> |**MVdbl** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|PT_MV_CURRENCY  <br/> |**MVcur** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|PT_MV_APPTIME  <br/> |**MVat** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|PT_MV_SYSTIME  <br/> |**MVft** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**MVbin** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**MVszA** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|PT_MV_UNICODE  <br/> |**MVszW** <br/> |[SWStringArray](swstringarray.md) <br/> |
|PT_MV_CLSID  <br/> |**MVguid** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**MVli** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|PT_NULL или PT_OBJECT  <br/> |**x** <br/> |ДЛИННЫЙ  <br/> |
|PT_PTR  <br/> |**lpv** <br/> |VOID\*  <br/> |
   
## <a name="remarks"></a>Замечания

Член **ulPropTag** состоит из двух частей: 
  
- Идентификатор в 16 бит высокого приоритета.
    
- Тип в 16 бит низкого приоритета.
    
Идентификатор — числовое значение в рамках определенного диапазона. Диапазоны идентификаторов для описания, для чего используется свойство и кто несет ответственность за обеспечение его определены MAPI. MAPI определяет ограничения для каждого из тегов свойств, поддерживаемых в файле заголовка Mapitags.h.
  
Тип указывает формат, для которых значение свойства. MAPI определяет константы для каждого типа свойства, поддерживаемые в файле заголовка Mapidefs.h. 
  
Полный список диапазонов допустимым свойством для идентификаторов и типы свойств содержатся в приложении [типов и идентификаторы свойств](property-identifiers-and-types.md) . 
  
Член **dwAlignPad** используется как внутренние поля чтобы сделать что правильного выравнивания на компьютерах, которые требуют 8-байтовое выравнивание для 8-байтовых значений. Разработчики, написание кода для таких компьютеров следует использовать процедур выделения памяти, выделить массивы **SPropValue** на 8-байтовое границы. 
  
Для получения дополнительных сведений см. [Обзор типа свойств MAPI](mapi-property-type-overview.md) и [Обновление свойств MAPI](updating-mapi-properties.md). 
  
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

