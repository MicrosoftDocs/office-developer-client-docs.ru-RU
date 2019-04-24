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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315787"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**Область применения**: Outlook 2013 | Outlook 2016 
  
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
  
> Размер структуры **ртф_вксретинфо** в байтах. 
    
_Улстреамфлагс_
  
> Это значение указывает формат основного текста. Это значение допустимо только в том случае, если в параметре _ulFlags_ структуры [ртф_вксинфо](rtf_wcsinfo.md) передается флаг **мапи_нативе_боди** , который передается в функцию [врапкомпресседртфстреамекс](wrapcompressedrtfstreamex.md) . Это может быть одно из следующих значений: 
    
|||
|:-----|:-----|
|МАПИ_НАТИВЕ_БОДИ_ТИПЕ_РТФ  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **мапи_нативе_боди** , а Body имеет значение RTF.  <br/> |
|МАПИ_НАТИВЕ_БОДИ_ТИПЕ_ПЛАИН_ТЕКСТ  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **мапи_нативе_боди** , а текст имеет обычный текстовый формат.  <br/> |
|МАПИ_НАТИВЕ_БОДИ_ТИПЕ_ХТМЛ  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **мапи_нативе_боди** , а текст имеет формат HTML.  <br/> |
   
## <a name="see-also"></a>См. также

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

