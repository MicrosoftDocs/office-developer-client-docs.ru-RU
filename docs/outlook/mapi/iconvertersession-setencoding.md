---
title: IConverterSessionSetEncoding
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
ms.assetid: a9624d3f-a636-0267-5cbd-de0db42f9c22
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5a81e04d112e0adf201dcacf03673daac77a04ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341302"
---
# <a name="iconvertersessionsetencoding"></a>IConverterSession::SetEncoding

**Область применения**: Outlook 2013 | Outlook 2016 
  
Инициализирует кодику, которая будет использоваться во время преобразования.
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a>Parameters

_et_
  
> Значение [ENCODINGTYPE.](https://msdn.microsoft.com/library/aa374936%28VS.85%29.aspx) Поддерживаются только следующие значения: 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>Возвращаемое значение

E_INVALIDARG
  
> Пройденный тип кодии был недействительным.
    
## <a name="remarks"></a>Примечания

Вызов **SetEncoding перед** использованием [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для выполнения преобразования. 
  
Используйте **SetEncoding,** чтобы установить кодику только для внешнего тела сообщения элемента почты. Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013 выбрать кодию для любых отдельных вложений. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |MFCMAPI использует MimeToMAPI для преобразования файла EML в сообщение MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |MFCMAPI использует MAPIToMIMEStm для преобразования сообщения MAPI в файл EML.  <br/> |
   
## <a name="see-also"></a>См. также

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [Константы MAPI](mapi-constants.md)

