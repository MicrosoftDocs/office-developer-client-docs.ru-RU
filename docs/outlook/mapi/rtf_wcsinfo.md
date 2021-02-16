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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Эта структура позволяет указать сведения для расшифрования текста сообщения в сжатом формате RTF и при желании вернуть поток текста в основном формате.
  
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
  
> Размер структуры **RTF_WCSINFO** в количестве вбайтах. 
    
 _ulFlags_
  
> Это битоваяmas флагов параметра для функции [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md) Поддерживаемые флажки вариантов: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Это указывает, собирается ли клиент написать возвращаемого интерфейса потока с оболочкой.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Это указывает, должен ли расшифрованный RTF быть записан в поток, на который указывает указатель _lpCompressedRTFStream_ функции [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md)  <br/> |
|MAPI_NATIVE_BODY  <br/> |Это указывает, преобразуется ли также раскомпрессовавный поток в свой теле, прежде чем возвращать поток. Этот флаг нельзя объединить  с MAPI_MODIFY флагом.  <br/> |
   
 _ulInCodePage_
  
> Это значение страницы кода сообщения. Как правило, это значение получается из канонического свойства [PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) сообщения. Это значение используется, только если **флаг MAPI_NATIVE_BODY** передается в _ulFlags._ В противном случае это значение игнорируется.
    
 _ulOutCodePage_
  
> Это значение кодовой страницы возвращаемого расшифрованного потока, который вы хотите получить. Если задано ненулевой значение, функция [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) преобразует поток в указанную кодовую страницу. Если установлено нулевое значение, MAPI решает, какую кодовую страницу использовать. Это значение используется, только если флаг **MAPI_NATIVE_BODY** передается в  _ulFlags,_ а формат тела не является форматом RTF. В противном случае это значение игнорируется.
    
## <a name="see-also"></a>См. также



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

