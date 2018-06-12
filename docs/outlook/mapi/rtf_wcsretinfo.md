---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 3a38a4604230c0aa3f5b0d104ae3b838f544b31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812165"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**Применимо к**: Outlook 
  
Эта структура предоставляет сведения о потоке в собственном формате, возвращенные распаковки к тексту сообщения, инкапсулированную в сжатом форматированный текст (RTF).
  
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
    
_ulStreamFlags_
  
> Это значение, указывающее формат собственного текста. Это значение допустимо только в том случае, если флаг **MAPI_NATIVE_BODY** передается в параметре _ulFlags_ структуры [RTF_WCSINFO](rtf_wcsinfo.md) , которое передается в функцию [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Это может быть одно из следующих значений: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , и текст RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , а текста имеет формат обычного текста.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Это значение используется только в том случае, если _ulFlags_ включает флаг **MAPI_NATIVE_BODY** , и текст формате (Hypertext Markup Language).  <br/> |
   
## <a name="see-also"></a>См. также

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

