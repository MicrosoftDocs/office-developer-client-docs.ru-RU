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
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430534"
---
# <a name="rtf_wcsinfo"></a>RTF_WCSINFO

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Эта структура позволяет указать сведения для декомпрессии тела сообщения в сжатом формате богатого текста (RTF) и, необязательно, вернуть поток тела в родном формате.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a>Элементы

 _size_
  
> Размер структуры **RTF_WCSINFO** в количестве bytes. 
    
 _ulFlags_
  
> Это битмаска флагов вариантов для функции [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md) Поддерживаемые флаги параметра: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Это указывает, намерен ли клиент написать возвращенный интерфейс потокового потока.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Это указывает, должен ли декомпрессированный RTF быть записан в поток, на который указывает указатель _lpCompressedRTFStream_ функции [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)  <br/> |
|MAPI_NATIVE_BODY  <br/> |Это указывает, преобразуется ли декомпрессируемый поток в родной орган перед возвращением потока. Этот флаг нельзя сочетать с **MAPI_MODIFY** флагом.  <br/> |
   
 _ulInCodePage_
  
> Это значение страницы кода сообщения. Обычно это значение получается из канонического свойства [PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) в сообщении. Это значение используется только при **MAPI_NATIVE_BODY** флага _ulFlags._ В противном случае это значение игнорируется.
    
 _ulOutCodePage_
  
> Это значение страницы кода возвращаемого декомпрессированного потока, которое необходимо. Если значение не нулевое, функция [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) преобразует поток на указанную страницу кода. Если для этого установлено нулевое значение, MAPI решает, какую страницу кода использовать. Это значение используется только тогда, **MAPI_NATIVE_BODY** флаг передается в  _ulFlags,_ и формат тела не является RTF. В противном случае это значение игнорируется.
    
## <a name="see-also"></a>См. также



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

