---
title: Иконвертерсессионсетсавеформат
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetCharSet
api_type:
- COM
ms.assetid: e5308a94-5191-2109-a881-b4f4a7ff1c61
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b528d6ef45c02b27f8e07d151793fc338f9af7b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336640"
---
# <a name="iconvertersessionsetsaveformat"></a>IConverterSession::SetSaveFormat

**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает формат, в котором преобразователь будет возвращать MIME поток в [иконвертерсессион:: мапитомиместм](iconvertersession-mapitomimestm.md).
  
```cpp
HRESULT IConverterSession::SetSaveFormat ( 
     MIMESAVETYPE mstSaveFormat 
);
```

## <a name="parameters"></a>Параметры

_Мстсавеформат_
  
> возврата Формат сохранения, используемый для потока MIME. Дополнительные сведения см. в разделе enum Type [мимесаветипе](https://msdn.microsoft.com/library/ms715128%28VS.85%29.aspx).
    
  - **SAVE_RFC1521**: использовать MIME, который является значением по умолчанию.      
  - **SAVE_RFC822**: используйте кодировку UUEncode.
    
## <a name="return-values"></a>Возвращаемые значения

S_OK
  
> Вызов выполнен успешно.
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мапимиме. cpp  <br/> |Импортемлтоимессаже  <br/> |MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.  <br/> |
|Мапимиме. cpp  <br/> |Експортимессажетоемл  <br/> |MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.  <br/> |
   
## <a name="see-also"></a>См. также

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetEncoding](iconvertersession-setencoding.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [Константы MAPI](mapi-constants.md)

