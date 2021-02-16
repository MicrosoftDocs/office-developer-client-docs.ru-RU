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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает необязательные адресные книги MAPI, которые преобразователь MAPI в MIME использует для разрешения неоднозначных адресов при преобразовании сообщения MAPI в поток MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Параметры

 _pab_
  
> [in] Указатель на [IAddrBook : интерфейс IMAPIProp](iaddrbookimapiprop.md) для использования в преобразовании MAPI в MIME. Установите для этого параметра **null,** если адресная книга больше не нужна; В этом случае интерфейс освобождается и преобразователь не использует адресную книгу. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов функции успешно.
    
## <a name="remarks"></a>Примечания

Преобразование сообщения MAPI в поток MIME обычно не требует входа в профиль MAPI. Однако для указания адресной книги MAPI для преобразования необходимо войти в профиль, чтобы получить адресную книгу.
  
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
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

