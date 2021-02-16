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
description: 'Last modified: September 20, 2017'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326946"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Преобразует сообщение MAPI в поток MIME.
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Параметры

 _pmsg_
  
> [in] Указатель на сообщение, которое необходимо преобразовать. Определение типа **LPMESSAGE** см. в mapidefs.h.
    
 _pstm_
  
> [out] [Интерфейс IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для вывода потока. 
    
 _ulFlags_
  
>  [in] Флаги, которые указывают определенные действия для конвертера: 
    
CCSF_8BITHEADERS
  
> Преобразователь должен разрешить 8-битные headers.
    
CCSF_EMBEDDED_MESSAGE
  
> Отправленные или неавентные сведения сохраняются в X-Unsent.
    
CCSF_GLOBAL_MESSAGE
  
> Преобразователь должен создать международное сообщение (EAI/RFC6530).
    
CCSF_INCLUDE_BCC
  
> Получатели сообщения MAPI должны быть включены в поток MIME.
    
CCSF_NO_MSGID
  
> Не включаем Message-Id поле в исходяющие сообщения.
    
CCSF_NOHEADERS
  
> Преобразователь должен игнорировать заглавные тексты внешнего сообщения.
    
CCSF_PLAIN_TEXT_ONLY
  
> Преобразователь должен просто отправить обычный текст.
    
CCSF_SMTP
  
> Преобразователь передается smTP-сообщение. Этот флаг всегда должен быть установлен.
    
CCSF_USE_RTF
  
> Преобразователь в сообщении MIME должен преобразовываться из формата HTML в формат RTF.
    
CCSF_USE_TNEF
  
> Преобразователь должен использовать формат TNEF в сообщении MIME.
    
## <a name="return-values"></a>Возвращаемые значения

E_INVALIDARG
  
> Были переданы недопустимые флаги,  *или pmsg*  или  *pstm*  имеет NULL. 
    
## <a name="remarks"></a>Примечания

Поддерживается только для стандартных типов сообщений Outlook.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI использует MimeToMAPI для преобразования EML-файла в сообщение MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в EML-файл.  <br/> |
   
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


[Константы MAPI](mapi-constants.md)

