---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432319"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Разрешает преобразование между объектами MIME и сообщениями MAPI. Это может быть полезно при транспортировке сообщений через Интернет.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |CLSID_IConverterSession  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Указывает необязательные адресные книги MAPI, которые преобразователь MAPI в MIME использует для разрешения неоднозначных адресов при преобразовании сообщения MAPI в поток MIME.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Инициализирует кодику, используемую во время преобразования.  <br/> |
| *Член-заметель*  <br/> | *Не поддерживается и не документируется.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Преобразует поток MIME в сообщение MAPI.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Преобразует сообщение MAPI в поток MIME.  <br/> |
| *Член-заметель*  <br/> | *Не поддерживается и не документируется.*  <br/> |
| *Член-заметель*  <br/> | *Не поддерживается и не документируется.*  <br/> |
| *Член-заметель*  <br/> | *Не поддерживается и не документируется.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Задает ширину обтекать текстом для потока MIME, который преобразователь возвращает в **MAPIToMIMEStm.**  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Задает формат, в который преобразователь возвращает поток MIME в **MAPIToMIMEStm.**  <br/> |
| *Член-заметель*  <br/> | *Не поддерживается и не документируется.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Указывает необязательный набор символов, который преобразователь MAPI в MIME использует при преобразовании сообщения MAPI в поток MIME.  <br/> |
   
## <a name="remarks"></a>Примечания

Вызовите **Метод SetEncoding** перед использованием **MAPIToMIMEStm для** преобразования. 
  
## <a name="see-also"></a>См. также



[Сведения об API преобразования MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[Константы MAPI](mapi-constants.md)

