---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426172"
---
# <a name="rtf_wcsretinfo"></a>RTF_WCSRETINFO

**Относится к**: Outlook 2013 | Outlook 2016 
  
Эта структура предоставляет сведения о потоке в собственном формате, возвращенном из распаковки текста сообщения, инкапсулированного в формате RTF.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Элементы

_size_
  
> Размер структуры **RTF_WCSRETINFO** в байтах. 
    
_улстреамфлагс_
  
> Это значение указывает формат основного текста. Это значение является допустимым только в том случае, если флаг **MAPI_NATIVE_BODY** передается в параметре _ulFlags_ структуры [RTF_WCSINFO](rtf_wcsinfo.md) , которая передается функции [врапкомпресседртфстреамекс](wrapcompressedrtfstreamex.md) . Это может быть одно из следующих значений: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , а текст имеет формат RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , а текст имеет обычный текстовый формат.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , а текст имеет формат HTML.  <br/> |
   
## <a name="see-also"></a>См. также

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

