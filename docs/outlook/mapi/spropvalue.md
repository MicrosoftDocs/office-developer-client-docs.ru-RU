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
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Связанные макросы:  <br/> |[CHANGE_PROP_TYPE,](change_prop_type.md) [MVI_PROP,](mvi_prop.md) [PROP_ID,](prop_id.md) [PROP_TAG](prop_tag.md), [PROP_TYPE](prop_type.md) <br/> |
   
```cpp
typedef struct _SPropValue
{
  ULONG ulPropTag;
  ULONG dwAlignPad;
  union _PV Value;
} SPropValue, FAR *LPSPropValue;

```

## <a name="members"></a>"Участники"

 **ulPropTag**
  
> Тег свойства для свойства. Теги свойств — это 32-битные неподписаные integers, состоящие из уникального идентификатора свойства в 16 битах высокого порядка и типа свойства в 16 битах низкого порядка.
    
 **dwAlignPad**
  
> Зарезервировано для MAPI; не используйте. 
    
 **Значение**
  
> Объединение значений данных, определенное значение, определенное типом свойства. В следующей таблице перечислены для каждого типа свойства, члена объединения, который должен использоваться, и связанного с ним типа данных.
    
|**Тип свойства**|**Значение**|**Тип данных значения**|
|:-----|:-----|:-----|
|PT_I2 или PT_SHORT  <br/> |**i** <br/> |short int  <br/> |
|PT_I4 или PT_LONG (подписан)  <br/> |**l** <br/> |LONG  <br/> |
|PT_I4 или PT_LONG (без подписи)  <br/> |**ul** <br/> |ULONG  <br/> |
|PT_R4 или PT_FLOAT  <br/> |**flt** <br/> |float  <br/> |
|PT_R8 или PT_DOUBLE  <br/> |**dbl** <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |**b** <br/> |unsigned short int  <br/> |
|PT_CURRENCY  <br/> |**cur** <br/> |[CURRENCY](currency.md) <br/> |
|PT_APPTIME  <br/> |**at** <br/> |double  <br/> |
|PT_SYSTIME  <br/> |**ft** <br/> |[FILETIME](filetime.md) <br/> |
|PT_STRING8  <br/> |**lpszA** <br/> |LPSTR  <br/> |
|PT_BINARY  <br/> |**bin** <br/> |BYTE [array]  <br/> |
|PT_UNICODE  <br/> |**lpszW** <br/> |LPWSTR  <br/> |
|PT_CLSID  <br/> |**lpguid** <br/> |LPGUID  <br/> |
|PT_I8 или PT_LONGLONG  <br/> |**li** <br/> |**LARGE_INTEGER** <br/> |
|PT_MV_I2  <br/> |**MVi** <br/> |[SShortArray](sshortarray.md) <br/> |
|PT_MV_LONG  <br/> |**MVI** <br/> |[SLongArray](slongarray.md) <br/> |
|PT_MV_R4  <br/> |**MVflt** <br/> |[SRealArray](srealarray.md) <br/> |
|PT_MV_DOUBLE  <br/> |**MVdbl** <br/> |[SDoubleArray](sdoublearray.md) <br/> |
|PT_MV_CURRENCY  <br/> |**MVcur** <br/> |[SCurrencyArray](scurrencyarray.md) <br/> |
|PT_MV_APPTIME  <br/> |**MVat** <br/> |[SAppTimeArray](sapptimearray.md) <br/> |
|PT_MV_SYSTIME  <br/> |**MVFT** <br/> |[SDateTimeArray](sdatetimearray.md) <br/> |
|PT_MV_BINARY  <br/> |**MVbin** <br/> |[SBinaryArray](sbinaryarray.md) <br/> |
|PT_MV_STRING8  <br/> |**MVSzA** <br/> |[SLPSTRArray](slpstrarray.md) <br/> |
|PT_MV_UNICODE  <br/> |**MVSzW** <br/> |[SWStringArray](swstringarray.md) <br/> |
|PT_MV_CLSID  <br/> |**MVguid** <br/> |[SGuidArray](sguidarray.md) <br/> |
|PT_MV_I8  <br/> |**MVli** <br/> |[SLargeIntegerArray](slargeintegerarray.md) <br/> |
|PT_ERROR  <br/> |**err** <br/> |[SCODE](scode.md) <br/> |
|PT_NULL или PT_OBJECT  <br/> |**x** <br/> |LONG  <br/> |
|PT_PTR  <br/> |**lpv** <br/> |VOID \*  <br/> |
   
## <a name="remarks"></a>Примечания

Член **ulPropTag** состоит из двух частей: 
  
- Идентификатор в 16 битах высокого порядка.
    
- Тип в 16 битах низкого порядка.
    
Идентификатор — это числовая величина в определенном диапазоне. MAPI определяет диапазоны для идентификаторов, чтобы описать, для чего используется свойство и кто несет ответственность за его обслуживание. MAPI определяет ограничения для каждого тега свойства, поддерживаемого в файле загона Mapitags.h.
  
Тип указывает формат значения свойства. MAPI определяет константы для каждого из типов свойств, поддерживаемые в файле загона Mapidefs.h. 
  
Полный список допустимого диапазона свойств для идентификаторов и типов свойств см. в приложении ["Идентификаторы](property-identifiers-and-types.md) и типы свойств". 
  
Член **dwAlignPad** используется в качестве заполнения для правильного выравнивания на компьютерах, которые требуют выравнивания 8 байт для 8-байтовых значений. Разработчикам, которые пишут код на таких компьютерах, следует использовать процедуры выделения памяти, которые выделяют массивы **SPropValue** на границах 8-byte. 
  
Дополнительные сведения см. в обзоре [типов свойств MAPI](mapi-property-type-overview.md) и обновлении [свойств MAPI.](updating-mapi-properties.md) 
  
## <a name="see-also"></a>См. также



[Структуры MAPI](mapi-structures.md)

