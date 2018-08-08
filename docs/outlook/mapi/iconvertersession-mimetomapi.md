---
title: IConverterSessionMIMEToMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.MIMEToMAPI
api_type:
- COM
ms.assetid: ee190ba7-9e71-97e4-7bf1-7b97adc73eed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 03a67371c67d5f0ac346470ec7ab38bb67d5ce2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808785"
---
# <a name="iconvertersessionmimetomapi"></a>IConverterSession::MIMEToMAPI

  
  
**Относится к**: Outlook 
  
Преобразование MIME-поток сообщений MAPI.
  
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
  
> [in] Интерфейс [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) поток MIME. 
    
 _pmsg_
  
> [out] Указатель на сообщение, чтобы загрузить. В разделе mapidefs.h для определения типа **LPMESSAGE**.
    
 _pszSrcSrv_
  
> [in] Это значение должно быть **значение null**.
    
 _ulFlags_
  
> [in] Этот параметр определяет дополнительных действий, которые требуется предпринять при преобразовании. Он должен быть нуль (0), если не определенное действие необходимо принять или сочетание следующих значений:
    
CCSF_EMBEDDED_MESSAGE
  
> Отправленные и неотправленные данные сохраняются в неотправленные X.
    
CCSF_SMTP
  
> MIME-поток — сообщение MAPI протокола SMTP (простой).
    
CCSF_INCLUDE_BCC
  
> Получателей Скрытой копии MIME-поток должно быть включено в сообщение MAPI.
    
CCSF_USE_RTF
  
> Чтобы форматированный текст (RTF) должны быть преобразованы в сообщении MAPI HTML-текста в потоке MIME.
    
## <a name="return-value"></a>������������ ��������

E_INVALIDARG
  
> Указывает, что _pstm_ имеет **значение null**, _pmsg_ имеет **значение null**или _ulFlags_ является недопустимым. 
    
## <a name="remarks"></a>Замечания

Если указаны **CCSF_USE_RTF** как часть _ulFlags_ и хранилище сообщений назначения поддерживает HTML и RTF, сообщение MAPI преобразуются в HTML или RTF. Если сообщение будет преобразовываться в формат RTF, сжимаются преобразованные формата RTF, весь HTML-код будут внедрены в строку сжатый формат RTF, а строка будет содержаться в [Каноническое свойство PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.  <br/> |
   
## <a name="see-also"></a>См. также



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[��������� MAPI](mapi-constants.md)

