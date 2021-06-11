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
description: 'Последнее изменение: 20 сентября 2017 г.'
ms.openlocfilehash: 55c547c4dae1acc3e9874edc7778f53a5d34f957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326946"
---
# <a name="iconvertersessionmapitomimestm"></a>IConverterSession::MAPIToMIMEStm
 
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Преобразует сообщение MAPI в поток MIME.
  
```cpp
HRESULT IConverterSession::MAPIToMIMEStm( 
    LPMESSAGE pmsg, 
    LPSTREAM pstm, 
    ULONG ulFlags 
);
```

## <a name="parameters"></a>Parameters

 _pmsg_
  
> [in] Указатель на сообщение для преобразования. См. mapidefs.h для определения типа **LPMESSAGE**.
    
 _pstm_
  
> [вышел] [Интерфейс IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) для вывода потока. 
    
 _ulFlags_
  
>  [in] Флаги, которые указывают определенные действия для конвертера: 
    
CCSF_8BITHEADERS
  
> Конвертер должен разрешить 8-битные заготки.
    
CCSF_EMBEDDED_MESSAGE
  
> В X-Unsent сохраняется отправленная/неослабеваемая информация.
    
CCSF_GLOBAL_MESSAGE
  
> Конвертер должен создать международное сообщение (EAI/RFC6530).
    
CCSF_INCLUDE_BCC
  
> Получатели сообщения MAPI BCC должны быть включены в поток MIME.
    
CCSF_NO_MSGID
  
> Не включай Message-Id поле в исходяние сообщений.
    
CCSF_NOHEADERS
  
> Преобразователь должен игнорировать заглавные главы внешнего сообщения.
    
CCSF_PLAIN_TEXT_ONLY
  
> Конвертер должен просто отправить простой текст.
    
CCSF_SMTP
  
> Преобразователь передает сообщение SMTP. Этот флаг всегда должен быть заданной.
    
CCSF_USE_RTF
  
> Конвертер должен преобразовать из ФОРМАТа HTML в формат RTF в сообщении MIME.
    
CCSF_USE_TNEF
  
> Конвертер должен использовать формат транспортной нейтральной инкапсуляции (TNEF) в сообщении MIME.
    
## <a name="return-values"></a>Возвращаемые значения

E_INVALIDARG
  
> Недействительные флаги были переданы,  *или pmsg*  или  *pstm*  является NULL. 
    
## <a name="remarks"></a>Примечания

Поддерживается только для стандартных типов Outlook сообщений.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI использует MimeToMAPI для преобразования файла EML в сообщение MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в файл EML.  <br/> |
   
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

