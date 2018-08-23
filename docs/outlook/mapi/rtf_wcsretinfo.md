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
ms.openlocfilehash: bf8cf115c6188b5058717437c470e11797ff5b9a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564964"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Эта структура предоставляет сведения о потоке в собственном формате, возвращенные распаковки к тексту сообщения, инкапсулированную в сжатом форматированный текст (RTF).
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Members

_size_.
  
> Размер структуры **RTF_WCSRETINFO** в байтах. 
    
_ulStreamFlags_
  
> Это значение, указывающее формат собственного текста. Это значение допустимо только в том случае, если флаг **MAPI_NATIVE_BODY** передается в параметре _ulFlags_ структуры [RTF_WCSINFO](rtf_wcsinfo.md) , которое передается в функцию [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Это может быть одно из следующих значений: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , и текст RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , а текста имеет формат обычного текста.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , и текст формате (Hypertext Markup Language).  <br/> |
   
## <a name="see-also"></a>См. также

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

