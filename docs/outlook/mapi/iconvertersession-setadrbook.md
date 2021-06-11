---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429196"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает необязательная адресная книга MAPI, которую конвертер MAPI для MIME использует для решения неоднозначных адресов при преобразовании сообщения MAPI в поток MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Parameters

 _pab_
  
> [in] Указатель на [интерфейс IAddrBook: интерфейс IMAPIProp,](iaddrbookimapiprop.md) который будет использоваться в преобразовании MAPI в MIME. Установите этот параметр **на нуль,** если вам больше не нужна адресная книга; это освобождает интерфейс и сбрасывает конвертер, чтобы не использовать адресную книгу. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов функции является успешным.
    
## <a name="remarks"></a>Примечания

Преобразование сообщения MAPI в поток MIME обычно не требует входа в профиль MAPI. Однако для указания адресной книги MAPI для преобразования требуется вход в профиль для получения адресной книги.
  
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
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

