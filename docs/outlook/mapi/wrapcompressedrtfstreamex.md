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
ms.openlocfilehash: af176c0ce327e6498a5d07f6d902c50f7323f813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325776"
---
# <a name="wrapcompressedrtfstreamex"></a>WrapCompressedRTFStreamEx

**Относится к**: Outlook 2013 | Outlook 2016 
  
Распечатывает текст сообщения электронной почты в сжатом формате RTF, указывает формат расжатого потока, при желании преобразует расжатый поток в свой собственный формат и возвращает либо расжатый поток, либо преобразованный собственный поток.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируется с помощью:  <br/> |msmapi32.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>Параметры

_lpCompressedRTFStream_
  
> [in] Это указатель на поток, который открывается в каноническом свойстве [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) сообщения. 
    
_pWCSInfo_
  
> [in] Это указатель на 
    
   [RTF_WCSINFO,](rtf_wcsinfo.md) которая содержит параметры функции. 
    
_lppUncompressedRTFStream_
  
> [out] Это указатель на расположение, в котором возвращается поток для расшифрованного RTF. 
    
_pRetInfo_
  
> [out] Это указатель на [структуру](rtf_wcsretinfo.md) RTF_WCSRETINFO, которая содержит сведения о формате возвращаемого раскодрованного потока. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
- Вызов функции успешно.
    
MAPI_E_INVALID_PARAMETER 
  
- Возвращается, если флаг **MAPI_NATIVE_BODY** с флагом **MAPI_MODIFY** в поле **ulFlags** структуры  RTF_WCSINFO, на который указывает *pWCSInfo.* 
    
## <a name="remarks"></a>Примечания

**WrapCompressedRTFStreamEx** позволяет получить доступ к тексту сообщения электронной почты, инкапсулированного в сжатый RTF путем сжатия потока, возвращает расжатый поток и его формат, а также, при желании, собственный поток тела. Встроенный поток текста может быть в формате RTF, обычном тексте или HTML. 
  
Объектная Microsoft Office Outlook предоставляет свойство **Body** для объектов **MailItem** и [свойство MailItem.BodyFormat (Outlook),](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) которое указывает формат текста текста. По проекту решение, которое не является доверенным в Outlook, вызывает диалоговые окна безопасности, созданные с помощью Безопасности Outlook. Использование экспортируемой функции MAPI **WrapCompressedRTFStreamEx** позволяет решению использовать MAPI вместо объектной модели Outlook и избегать использования этих диалоговых окной безопасности. 
  
Так как флаг **MAPI \_ NATIVE_BODY** нельзя объединить с флагом **MAPI \_ MODIFY** в поле **ulFlags** структуры **\_ WCSINFO RTF,** на который указывает *pWCSInfo,* доступ к потоку тела можно получить только в режиме только для чтения. Чтобы получить доступ к потоку тела в режиме чтения и записи, необходимо использовать функцию **WrapCompressedRTFStream.** 
  
## <a name="see-also"></a>См. также

- [Извлечение тела сообщения в сжатом формате RTF и его преобразование в собственный формат](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

