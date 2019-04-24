---
title: Иконвертерсессионмиметомапи
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
ms.openlocfilehash: 356f4470be26ae3803a53af1cec34b3ac6eb0cc9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326931"
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

## <a name="parameters"></a>Параметры

 _пстм_
  
> возврата Интерфейс [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) в поток MIME. 
    
 _ПМСГ_
  
> вышли Указатель на сообщение для загрузки. Определение типа **лпмессаже**можно найти в файле MAPIDEFS. h.
    
 _Псзсрксрв_
  
> возврата Это значение должно быть **равно NULL**.
    
 _ulFlags_
  
> возврата Этот параметр определяет все специальные действия, выполняемые во время преобразования. Он должен иметь значение ноль (0), если не нужно предпринимать какие-либо действия или сочетания следующих значений:
    
ККСФ_ЕМБЕДДЕД_МЕССАЖЕ
  
> Отправленные и неотправленные сведения хранятся в неотправленном виде X-a.
    
CCSF_SMTP
  
> MIME-поток предназначен для простого сообщения протокола передачи MAPI.
    
CCSF_INCLUDE_BCC
  
> Получатели СКРЫТой копии MIME необходимо включить в сообщение MAPI.
    
CCSF_USE_RTF
  
> Основной текст HTML-потока MIME должен быть преобразован в формат RTF в сообщении MAPI.

CCSF_GLOBAL_MESSAGE
> Конвертер должен обрабатывать поток MIME в виде международного сообщения (ЕАИ/RFC6530). Не поддерживается в Outlook 2013.
    
## <a name="return-value"></a>Возвращаемое значение

E_INVALIDARG
  
> Указывает, что _пстм_ имеет **значение NULL**, _ПМСГ_ имеет **значение NULL**или _ulFlags_ является недопустимым. 
    
## <a name="remarks"></a>Замечания

Если вы указали **кксф_усе_ртф** в составе _ulFlags_ и конечный банк сообщений поддерживает как HTML, так и RTF, сообщение MAPI будет преобразовано в формат HTML или RTF. Если сообщение преобразуется в формат RTF, преобразованный формат будет сжат в формате RTF, любой HTML-код будет внедрен в сжатую строку RTF, а строка будет содержаться в [канонИческое свойство PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md).
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мапимиме. cpp  <br/> |Импортемлтоимессаже  <br/> |MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.  <br/> |
|Мапимиме. cpp  <br/> |Експортимессажетоемл  <br/> |MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.  <br/> |
   
## <a name="see-also"></a>См. также



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)


[Константы MAPI](mapi-constants.md)

