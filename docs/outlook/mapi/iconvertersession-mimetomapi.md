---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 09/06/2019
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Последнее изменение: 06 сентября 2019 г.'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160288"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует поток MIME в сообщение MAPI.
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a>Parameters

 _pstm_
  
> [in] [Интерфейс IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) к потоку MIME. 
    
 _pmsg_
  
> [in] Указатель на сообщение для загрузки. Чтобы заполнить API, вызываемая должна предоставить сообщение, поэтому объект должен пройти [в]. См. mapidefs.h для определения типа **LPMESSAGE**.
    
 _pszSrcSrv_
  
> [in] Это значение должно быть **null**.
    
 _ulFlags_
  
> [in] Этот параметр определяет любые специальные действия, которые необходимо принять во время преобразования. Ноль (0), если не нужно принимать каких-либо конкретных действий, или сочетание следующих значений:
    
CCSF_EMBEDDED_MESSAGE
  
> В X-Unsent сохраняется отправленная/неослабеваемая информация.
    
CCSF_SMTP
  
> Поток MIME для сообщения Простой протокол передачи почты (SMTP).
    
CCSF_INCLUDE_BCC
  
> Получатели BCC потока MIME должны быть включены в сообщение MAPI.
    
CCSF_USE_RTF
  
> HTML-текст потока MIME должен быть преобразован в формат rich Text Format (RTF) в сообщении MAPI.

CCSF_GLOBAL_MESSAGE
> Конвертер должен обрабатывать поток MIME как международное сообщение (EAI/RFC6530). Не поддерживается Outlook 2013 г.
    
## <a name="return-value"></a>Возвращаемое значение

E_INVALIDARG
  
> Указывает,  _что pstm является_ **null,**  _pmsg_ является **null** или  _ulFlags_ является недействительным. 
    
## <a name="remarks"></a>Примечания

Если вы указали CCSF_USE_RTF как часть _ulFlags,_ а хранилище сообщений назначения поддерживает HTML и RTF, сообщение MAPI будет преобразовано в HTML или RTF.  Если сообщение преобразовано в RTF, преобразованный формат будет сжат RTF, любой HTML будет встроен в сжатую строку RTF, а строка будет содержаться в каноническом свойстве [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI использует MimeToMAPI для преобразования файла EML в сообщение MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в файл EML.  <br/> |
   
## <a name="see-also"></a>См. также



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Константы MAPI](mapi-constants.md)

