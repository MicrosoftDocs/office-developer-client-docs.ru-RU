---
title: WrapCompressedRTFStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45abee1c-d7fb-b0f9-522d-8ba34caf1094
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4b7e59c9ffccb2e063962b2cc4947b4fa54757bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572720"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Распаковывает тело сообщения электронной почты, который является в сжатом форматированный текст (RTF), указывает формат распакованных потока, при необходимости преобразует распакованных потока в его собственном формате и возвращает распакованных поток или преобразовать собственного потока.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировать с:  <br/> |Msmapi32.dll  <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>Параметры

_lpCompressedRTFStream_
  
> [in] Это указатель на поток, который открывается на [PidTagRtfCompressed каноническое свойства](pidtagrtfcompressed-canonical-property.md) сообщения. 
    
_pWCSInfo_
  
> [in] Это указатель 
    
   Структура [RTF_WCSINFO](rtf_wcsinfo.md) , содержащая параметры для функции. 
    
_lppUncompressedRTFStream_
  
> [out] Это указатель на место, где возвращается поток для распакованных RTF. 
    
_pRetInfo_
  
> [out] Это указатель на структуру [RTF_WCSRETINFO](rtf_wcsretinfo.md) , который содержит сведения о формате возвращенные распакованных потока. 
    
## <a name="return-values"></a>Возвращаемые значения

ЗНАЧЕНИЕ S_OK 
  
- Вызов функции выполнен успешно.
    
MAPI_E_INVALID_PARAMETER 
  
- Возвращается, если флаг **MAPI_NATIVE_BODY** используется в сочетании с флагом **MAPI_MODIFY** в поле **ulFlags** структуры **RTF_WCSINFO** , на которую указывает *pWCSInfo* . 
    
## <a name="remarks"></a>Замечания

**WrapCompressedRTFStreamEx** позволяет получить доступ к тело сообщения электронной почты, инкапсулированную в сжатом формате RTF, распаковки в потоке возвращает распакованных потока и его формате, а также в потоке собственный текст. Поток собственный текст может быть в формате RTF, обычный текст или HTML. 
  
Объектная модель Microsoft Office Outlook предоставляет свойство **Body** **MailItem** объектов и [Свойств MailItem.BodyFormat (Outlook)](http://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) , которое указывает формат основного текста. В архитектуре решение, которое не является доверенным для Outlook вызывает диалоговые окна безопасности, созданные с охрана Outlook. С помощью функции экспортированного MAPI **WrapCompressedRTFStreamEx** позволяет решение, которое требуется использовать вместо объектной модели Outlook MAPI и избежать этих диалоговых окон безопасности. 
  
Так как **MAPI\_NATIVE_BODY** флаг нельзя использовать вместе с **MAPI\_изменить** флаг в поле **ulFlags** **RTF\_WCSINFO** структура указывает *pWCSInfo*доступны только собственный поток текста в режиме только для чтения. Чтобы получить доступ к потоку собственный текст в режиме чтения и записи, следует использовать функцию **WrapCompressedRTFStream** . 
  
## <a name="see-also"></a>См. также

- [Получение текста сообщения в виде сжатого RTF-файла и его преобразование в исходный формат](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

