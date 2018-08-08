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
ms.openlocfilehash: a89b1a93b2b03f97426a3988739e9b0d8411f113
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808803"
---
# <a name="iconvertersession--iunknown"></a>IConverterSession : IUnknown

  
  
**Относится к**: Outlook 
  
Обеспечивает преобразование между объектами MIME и сообщения MAPI. Это может быть полезно в обмен сообщениями через Интернет.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |CLSID_IConverterSession  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|**[SetAdrBook](iconvertersession-setadrbook.md)** <br/> |Задает необязательный MAPI адресной книге, MAPI для конвертера MIME для разрешения неоднозначных адреса при преобразовании сообщения MAPI в MIME-поток.  <br/> |
|**[SetEncoding](iconvertersession-setencoding.md)** <br/> |Инициализирует кодировку для использования при преобразовании.  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
|**[MIMEToMAPI](iconvertersession-mimetomapi.md)** <br/> |Преобразование MIME-поток сообщений MAPI.  <br/> |
|**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)** <br/> |Преобразование сообщения MAPI в MIME-поток.  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
|**[SetTextWrapping](iconvertersession-settextwrapping.md)** <br/> |Задает ширину потока MIME, который возвращает преобразователь в **MAPIToMIMEStm**обтекания.  <br/> |
|**[SetSaveFormat](iconvertersession-setsaveformat.md)** <br/> |Задает формат, что преобразователь возвращает MIME-поток в **MAPIToMIMEStm**.  <br/> |
| *Заполнитель члена*  <br/> | *Не поддерживается, документированных.*  <br/> |
|**[SetCharSet](iconvertersession-setcharset.md)** <br/> |Задает набора необязательный символ, что MAPI-MIME преобразователь использует при преобразовании сообщения MAPI в MIME-поток.  <br/> |
   
## <a name="remarks"></a>Замечания

Вызовите **SetEncoding** перед использованием **MAPIToMIMEStm** для выполнения преобразования. 
  
## <a name="see-also"></a>См. также



[Сведения об API преобразования MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[��������� MAPI](mapi-constants.md)

