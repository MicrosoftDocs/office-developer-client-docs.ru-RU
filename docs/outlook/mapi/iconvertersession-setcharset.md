---
title: IConverterSessionSetCharSet
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
ms.assetid: 25af3683-3a65-2d39-6f6e-76c8d36f866d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 14b2904e57852c564395f4b27c9d5270afd1454a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336661"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает необязательный набор символов, который используется конвертером MAPI в MIME при преобразовании сообщения MAPI в поток MIME.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Parameters

 _fApply_
  
> [in] Указывает, следует ли использовать определенный набор символов для преобразования. Установите этот параметр **верным, чтобы** применить набор символов в последующих преобразованиях. Установите этот параметр **ложным,** если вы больше не хотите применять какой-либо определенный набор символов и возвращаться к значениям по умолчанию для последующих сообщений. 
    
 _hcharset_
  
> [in] Ручка для набора символов, как определено в mimeole.h Почта Windows. Укажите **null,** чтобы указать, что не нужно применять какой-либо определенный набор символов. Для **ненуловых** значений используйте функцию [MimeOleGetCodePageCharset](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) для получения ручки для набора символов. 
    
 _csetapplytype_
  
> [in] Указывает, как применить набор символов для преобразования сообщения, как определено в mimeole.h Почта Windows.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов функции является успешным.
    
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
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

