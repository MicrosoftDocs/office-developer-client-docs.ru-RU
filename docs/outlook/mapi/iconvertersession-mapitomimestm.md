---
title: иконвертерсессионмапитомиместм
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
description: 'Дата последнего изменения: 20 сентября 2017 г.'
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

 _пмсг_
  
> возврата Указатель на сообщение, которое требуется преобразовать. Определение типа **лпмессаже**можно найти в файле MAPIDEFS. h.
    
 _пстм_
  
> вышли Интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для вывода потока. 
    
 _ulFlags_
  
>  возврата Флаги, указывающие определенные действия для конвертера: 
    
CCSF_8BITHEADERS
  
> Конвертер должен разрешить 8 – битовые заголовки.
    
CCSF_EMBEDDED_MESSAGE
  
> Отправленные и неотправленные сведения хранятся в неотправленном виде X-a.
    
CCSF_GLOBAL_MESSAGE
  
> Конвертер должен создать международный сообщение (ЕАИ/RFC6530).
    
CCSF_INCLUDE_BCC
  
> Получатели скрытой копии сообщения MAPI должны быть включены в поток MIME.
    
CCSF_NO_MSGID
  
> Не включайте поле Message — ID в исходящие сообщения.
    
CCSF_NOHEADERS
  
> Конвертер должен игнорировать заголовки внешнего сообщения.
    
CCSF_PLAIN_TEXT_ONLY
  
> Конвертер должен просто отправить обычный текст.
    
CCSF_SMTP
  
> Преобразователь передается сообщение SMTP. Этот флаг всегда должен быть установлен.
    
CCSF_USE_RTF
  
> Конвертер должен преобразовать HTML-код в формат RTF в сообщении MIME.
    
CCSF_USE_TNEF
  
> Конвертер должен использовать формат TNEF в сообщении MIME.
    
## <a name="return-values"></a>Возвращаемые значения

E_INVALIDARG
  
> Переданы недопустимые флаги, или *ПМСГ* или *ПСТМ* имеет значение null. 
    
## <a name="remarks"></a>Примечания

Поддерживается только для стандартных типов сообщений Outlook.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мапимиме. cpp  <br/> |импортемлтоимессаже  <br/> |MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.  <br/> |
|Мапимиме. cpp  <br/> |експортимессажетоемл  <br/> |MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.  <br/> |
   
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

