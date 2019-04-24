---
title: Иконвертерсессионсетадрбук
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326896"
---
# <a name="iconvertersessionsetadrbook"></a>IConverterSession::SetAdrBook

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает необязательную адресную книгу MAPI, используемую преобразователем MAPI to MIME для разрешения неоднозначных адресов при преобразовании сообщения MAPI в поток MIME.
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a>Параметры

 _адресной_
  
> возврата Указатель на интерфейс [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) , который будет использоваться в преобразовании MAPI в MIME. Если адресная книга больше не нужна, установите для этого параметра **значение NULL** . При этом интерфейс освобождается и сбрасывается без использования адресной книги. 
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов функции выполнен успешно.
    
## <a name="remarks"></a>Замечания

Для преобразования сообщения MAPI в поток MIME обычно не требуется вход в профиль MAPI. Однако чтобы указать адресную книгу MAPI для преобразования, необходимо войти в профиль, чтобы получить адресную книгу.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мапимиме. cpp  <br/> |Импортемлтоимессаже  <br/> |MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.  <br/> |
|Мапимиме. cpp  <br/> |Експортимессажетоемл  <br/> |MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.  <br/> |
   
## <a name="see-also"></a>См. также



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

