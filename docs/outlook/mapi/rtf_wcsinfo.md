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
  
Эта структура позволяет указать информацию для распаковки текста сообщения в формате RTF и (при необходимости) вернуть поток текста в исходном формате.
  
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
  
> Размер структуры **RTF_WCSINFO** в байтах. 
    
 _ulFlags_
  
> Это битовая маска флагов параметров для функции [врапкомпресседртфстреамекс](wrapcompressedrtfstreamex.md) . Флаги поддерживаемых параметров: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Это указывает на то, что клиент намеревается записывать возвращаемый интерфейс упакованных потоков.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Указывает, следует ли записывать Распакованный формат RTF в поток, на который указывает указатель _лпкомпресседртфстреам_ функции [врапкомпресседртфстреамекс](wrapcompressedrtfstreamex.md) .  <br/> |
|MAPI_NATIVE_BODY  <br/> |Это указывает, будет ли Распакованный поток также преобразован в основной текст перед возвратом потока. Этот флаг не может использоваться вместе с флагом **MAPI_MODIFY** .  <br/> |
   
 _улинкодепаже_
  
> Это значение кодовой страницы сообщения. Как правило, это значение получается из [каноническое свойство PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) сообщения. Это значение используется только в том случае, если в _ulFlags_передается флаг **MAPI_NATIVE_BODY** . В противном случае это значение игнорируется.
    
 _улауткодепаже_
  
> Это значение кодовой страницы возвращенного распакованного потока, который требуется выполнить. Если для этого свойства задано значение, отличное от нуля, функция [врапкомпресседртфстреамекс](wrapcompressedrtfstreamex.md) преобразует поток в указанную кодовую страницу. Если для этого свойства задано нулевое значение, MAPI определяет, какую кодовую страницу использовать. Это значение используется только в том случае, если в _ulFlags_передается флаг **MAPI_NATIVE_BODY** , а формат текста не является RTF. В противном случае это значение игнорируется.
    
## <a name="see-also"></a>См. также



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

