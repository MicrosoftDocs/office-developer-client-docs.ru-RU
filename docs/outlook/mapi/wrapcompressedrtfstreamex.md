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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Декомпрессирует тело сообщения электронной почты, которое находится в сжатом формате богатого текста (RTF), указывает формат декомпрессируемого потока, необязательным образом преобразует декомпрессируемый поток в свой родной формат и возвращает либо декомпрессованный поток, либо преобразованный родной поток.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируемая по:  <br/> |msmapi32.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT __stdcall WrapCompressedRTFStreamEx( 
    LPSTREAM            lpCompressedRTFStream, 
    CONST RTF_WCSINFO   *pWCSInfo, 
    LPSTREAM            *lppUncompressedRTFStream, 
    RTF_WCSRETINFO      *pRetInfo); 

```

## <a name="parameters"></a>Parameters

_lpCompressedRTFStream_
  
> [in] Это указатель потока, открываемого в каноническом свойстве [сообщения PidTagRtfCompressed.](pidtagrtfcompressed-canonical-property.md) 
    
_pWCSInfo_
  
> [in] Это указатель на 
    
   [RTF_WCSINFO,](rtf_wcsinfo.md) которая содержит параметры функции. 
    
_lppUncompressedRTFStream_
  
> [вышел] Это указатель на расположение, в котором возвращается поток для декомпрессированного RTF. 
    
_pRetInfo_
  
> [вышел] Это указатель на структуру [RTF_WCSRETINFO,](rtf_wcsretinfo.md) которая содержит сведения о формате возвращенного декомпрессированного потока. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
- Вызов функции является успешным.
    
MAPI_E_INVALID_PARAMETER 
  
- Это возвращается, **если флаг MAPI_NATIVE_BODY** совмещен  с флагом MAPI_MODIFY в **поле ulFlags** структуры RTF_WCSINFO, на который указывает *pWCSInfo* .  
    
## <a name="remarks"></a>Примечания

**WrapCompressedRTFStreamEx** позволяет получить доступ к тексту сообщения электронной почты, инкапсулированного в сжатом RTF путем декомпрессии потока, возвращает декомпрессированный поток и его формат, а также необязательно родной поток тела. Поток родного тела может быть в RTF, простом тексте или HTML. 
  
Объектная Microsoft Office Outlook предоставляет свойство  Body для объектов **MailItem** и [свойство MailItem.BodyFormat (Outlook),](https://msdn.microsoft.com/library/f635a0bc-20b7-206c-f558-a4ca2519670f%28Office.15%29.aspx) которое указывает формат текста тела. По проекту решение, которому не доверяют Outlook вызывает диалоговые окна безопасности, созданные Outlook security Guard. Использование экспортируемой функции **MAPI WrapCompressedRTFStreamEx** позволяет решению использовать MAPI вместо объектной модели Outlook и избегать этих диалоговых ящиков безопасности. 
  
Так как флаг **mapi \_ NATIVE_BODY** нельзя сочетать с флагом **MAPI \_ MODIFY** в поле **ulFlags** структуры **\_ WCSINFO RTF,** на который указывает *pWCSInfo,* доступ к родному потоку тела можно получить только в режиме только для чтения. Чтобы получить доступ к родному потоку тела в режиме чтения и записи, необходимо использовать функцию **WrapCompressedRTFStream.** 
  
## <a name="see-also"></a>См. также

- [Извлечение тела сообщения в сжатых RTF и преобразование его в свой родной формат](how-to-retrieve-the-body-of-a-message-in-compressed-rtf-and-convert.md)

