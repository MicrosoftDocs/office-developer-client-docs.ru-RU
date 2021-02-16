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
description: 'Last modified: September 06, 2019'
ms.openlocfilehash: c9fcffa8ad4dc982e869f4ccd449e1377fb1ea57
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160288"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Преобразует поток MIME в сообщение MAPI.
  
```cpp
HRESULT IConverterSession:: MIMEToMAPI ( 
     LPSTREAM pstm, 
     LPMESSAGE pmsg, 
     LPCSTR pszSrcSrv, 
     ULONG ulFlags 
);
```

## <a name="parameters"></a>Параметры

 _pstm_
  
> [in] [Интерфейс IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) в поток MIME. 
    
 _pmsg_
  
> [in] Указатель на сообщение для загрузки. Вызываемая группа должна предоставить сообщение, чтобы API заполнил его, поэтому объект должен пройти [в]. Определение типа **LPMESSAGE** см. в mapidefs.h.
    
 _pszSrcSrv_
  
> [in] Это значение должно быть **null.**
    
 _ulFlags_
  
> [in] Этот параметр определяет любые специальные действия, которые необходимо принять во время преобразования. Значение должно быть нулем (0), если не нужно никаких конкретных действий, или сочетание следующих значений:
    
CCSF_EMBEDDED_MESSAGE
  
> Отправленные или неавентные сведения сохраняются в X-Unsent.
    
CCSF_SMTP
  
> Поток MIME для сообщения SMTP.
    
CCSF_INCLUDE_BCC
  
> Получатели BCC потока MIME должны быть включены в сообщение MAPI.
    
CCSF_USE_RTF
  
> Текст HTML-текста потока MIME должен быть преобразован в формат RTF в сообщении MAPI.

CCSF_GLOBAL_MESSAGE
> Преобразователь должен обрабатывать поток MIME как международное сообщение (EAI/RFC6530). Не поддерживается в Outlook 2013.
    
## <a name="return-value"></a>Возвращаемое значение

E_INVALIDARG
  
> Указывает,  _что pstm_ имеет **null,**  _pmsg_ — **null,**  _или ulFlags_ является недопустимым. 
    
## <a name="remarks"></a>Примечания

Если вы указали CCSF_USE_RTF как часть _ulFlags,_ а конечное хранилище сообщений поддерживает htmL и RTF, сообщение MAPI будет преобразовано в HTML или RTF.  Если сообщение преобразуется в формат RTF, преобразованный формат будет сжатым форматом RTF, любой HTML-код будет внедрен в сжатую строку RTF, а строка будет содержаться в каноническом свойстве [PidTagRtfCompressed.](pidtagrtfcompressed-canonical-property.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI использует MimeToMAPI для преобразования EML-файла в сообщение MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в EML-файл.  <br/> |
   
## <a name="see-also"></a>См. также



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Константы MAPI](mapi-constants.md)

