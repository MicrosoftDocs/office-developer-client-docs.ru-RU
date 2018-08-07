---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c328e79b7e474369f11f8a4002e00137659db3c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812183"
---
# <a name="rtfwcsinfo"></a>RTF_WCSINFO

  
  
**Относится к**: Outlook 
  
Эта структура позволяет указать сведения, которые распаковка к тексту сообщения в сжатом форматированный текст (RTF) и при необходимости вернуться в потоке текста в его собственном формате.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a>Members

 _size_
  
> Размер структуры **RTF_WCSINFO** в байтах. 
    
 _ulFlags_
  
> Это битовая маска флаги функции [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Поддерживаемые варианты флаги являются: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Указывает, планирует интерфейса упакованный поток, который возвращается клиенту.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Указывает, должен ли распакованных RTF для записи в поток, который указывает _lpCompressedRTFStream_ указатель функции [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .  <br/> |
|MAPI_NATIVE_BODY  <br/> |Это указывает, будет ли распакованных потока также преобразованы в собственный текст перед возвращением потока. Этот флаг нельзя использовать вместе с флагом **MAPI_MODIFY** .  <br/> |
   
 _ulInCodePage_
  
> Это значение кодовой страницы сообщения. Как правило это значение будет получен из [Каноническое свойство PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) в окне сообщения. Это значение используется только в том случае, когда флаг **MAPI_NATIVE_BODY** передается в _ulFlags_. В противном случае это значение игнорируется.
    
 _ulOutCodePage_
  
> Это значение кодовой страницы, возвращенные распакованных потока, который будет. Если это задано значение ненулевое значение, функция [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) преобразуется в потоке кодовой страницы. Если это присвоено значение 0, MAPI решает использовать кодовую страницу. Это значение используется только в том случае, когда флаг **MAPI_NATIVE_BODY** передается в _ulFlags_и формат текста сообщения не является RTF. В противном случае это значение игнорируется.
    
## <a name="see-also"></a>См. также



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

