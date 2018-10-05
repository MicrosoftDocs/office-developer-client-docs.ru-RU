---
title: IConverterSessionMAPIToMIMEStm
ms.date: 9/20/2017
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MAPIToMIMEStm
api_type:
- COM
ms.assetid: 8660c701-f7f4-8d92-7984-5dae7f677783
description: 'Последнее изменение: 20 сентября 2017'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400119"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Преобразование сообщения MAPI в MIME-поток.
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Параметры

 _pmsg_
  
> [in] Указатель на сообщение для преобразования. В разделе mapidefs.h для определения типа **LPMESSAGE**.
    
 _pstm_
  
> [out] Интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для вывода в потоке. 
    
 _ulFlags_
  
>  [in] Флаги, указывающие конкретные действия для преобразователя: 
    
CCSF_8BITHEADERS
  
> Преобразователь, должна поддерживать 8-разрядных заголовков.
    
CCSF_EMBEDDED_MESSAGE
  
> Отправленные и неотправленные данные сохраняются в неотправленные X.
    
CCSF_GLOBAL_MESSAGE
  
> Преобразователь следует создавать международные сообщения (EAI/RFC6530).
    
CCSF_INCLUDE_BCC
  
> Получателей Скрытой копии сообщения MAPI должно быть включено в MIME-поток.
    
CCSF_NO_MSGID
  
> Не включайте поле идентификатор сообщения в исходящих сообщений.
    
CCSF_NOHEADERS
  
> Преобразователь следует игнорировать заголовки сообщений за пределы организации.
    
CCSF_PLAIN_TEXT_ONLY
  
> Преобразователь только что следует отправить обычный текст.
    
CCSF_SMTP
  
> Преобразователь, передается SMTP-сообщения. Этот флаг всегда должно иметь значение.
    
CCSF_USE_RTF
  
> Преобразователь следует преобразовать из HTML в формат RTF в сообщения MIME.
    
CCSF_USE_TNEF
  
> Преобразователь следует использовать формат транспорта Neutral Encapsulation формата TNEF в сообщения MIME.
    
## <a name="return-values"></a>Возвращаемые значения

E_INVALIDARG
  
> Были переданы недопустимые флаги или *pmsg* или *pstm* имеет значение NULL. 
    
## <a name="remarks"></a>Замечания

Поддерживается только для стандартных типов сообщений Outlook.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.  <br/> |
   
## <a name="see-also"></a>См. также



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
  
[Каноническое свойство PidTagMessageEditorFormat](pidtagmessageeditorformat-canonical-property.md)
  
[������������ �������� PidLidUseTnef](pidlidusetnef-canonical-property.md)


[��������� MAPI](mapi-constants.md)

