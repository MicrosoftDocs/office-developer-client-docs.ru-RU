---
title: иконвертерсессионмиметомапи
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
description: 'Дата последнего изменения: 06 сентября 2019 г.'
ms.openlocfilehash: f6f671cbfd5e14d602aaa31d31e54e859f068593
ms.sourcegitcommit: 27a9f3568318470e7ee09ad93a90c3f80d3ef0cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2019
ms.locfileid: "36790773"
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

 _пстм_
  
> возврата Интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) в поток MIME. 
    
 _пмсг_
  
> возврата Указатель на сообщение для загрузки. Вызывающий абонент должен предоставить сообщение для заполнения API, поэтому объект должен идти [in]. Определение типа **лпмессаже**можно найти в файле MAPIDEFS. h.
    
 _псзсрксрв_
  
> возврата Это значение должно быть **равно NULL**.
    
 _ulFlags_
  
> возврата Этот параметр определяет все специальные действия, выполняемые во время преобразования. Он должен иметь значение ноль (0), если не нужно предпринимать какие-либо действия или сочетания следующих значений:
    
CCSF_EMBEDDED_MESSAGE
  
> Отправленные и неотправленные сведения хранятся в неотправленном виде X-a.
    
CCSF_SMTP
  
> MIME-поток предназначен для простого сообщения протокола передачи MAPI.
    
CCSF_INCLUDE_BCC
  
> Получатели скрытой копии MIME необходимо включить в сообщение MAPI.
    
CCSF_USE_RTF
  
> Основной текст HTML-потока MIME должен быть преобразован в формат RTF в сообщении MAPI.

CCSF_GLOBAL_MESSAGE
> Конвертер должен обрабатывать поток MIME в виде международного сообщения (ЕАИ/RFC6530). Не поддерживается в Outlook 2013.
    
## <a name="return-value"></a>Возвращаемое значение

E_INVALIDARG
  
> Указывает, что _пстм_ имеет **значение NULL**, _ПМСГ_ имеет **значение NULL**или _ulFlags_ является недопустимым. 
    
## <a name="remarks"></a>Примечания

Если вы указали **CCSF_USE_RTF** в составе _ulFlags_ и конечный банк сообщений поддерживает как HTML, так и RTF, сообщение MAPI будет преобразовано в формат HTML или RTF. Если сообщение преобразуется в формат RTF, преобразованный формат будет сжат в формате RTF, любой HTML-код будет внедрен в сжатую строку RTF, а строка будет содержаться в [каноническое свойство PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мапимиме. cpp  <br/> |импортемлтоимессаже  <br/> |MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.  <br/> |
|Мапимиме. cpp  <br/> |експортимессажетоемл  <br/> |MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.  <br/> |
   
## <a name="see-also"></a>См. также



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Константы MAPI](mapi-constants.md)

