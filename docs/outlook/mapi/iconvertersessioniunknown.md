---
title: Иконвертерсессион IUnknown
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
  
Позволяет выполнять преобразование между объектами MIME и сообщениями MAPI. Это может быть удобно при переносе сообщений через Интернет.
  
|||
|:-----|:-----|
|Предоставлено:  <br/> |CLSID_IConverterSession  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IConverterSession  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|**[сетадрбук](iconvertersession-setadrbook.md)** <br/> |Задает необязательную адресную книгу MAPI, используемую преобразователем MAPI to MIME для разрешения неоднозначных адресов при преобразовании сообщения MAPI в поток MIME.  <br/> |
|**[сетенкодинг](iconvertersession-setencoding.md)** <br/> |Инициализирует кодировку, используемую при преобразовании.  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
|**[миметомапи](iconvertersession-mimetomapi.md)** <br/> |Преобразует поток MIME в сообщение MAPI.  <br/> |
|**[мапитомиместм](iconvertersession-mapitomimestm.md)** <br/> |Преобразует сообщение MAPI в поток MIME.  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
|**[сеттекствраппинг](iconvertersession-settextwrapping.md)** <br/> |Задает ширину обтекания текста для потока MIME, возвращаемого преобразователем в **мапитомиместм**.  <br/> |
|**[сетсавеформат](iconvertersession-setsaveformat.md)** <br/> |Задает формат, который преобразователь возвращает поток MIME в **мапитомиместм**.  <br/> |
| *Элемент PlaceHolder*  <br/> | *Не поддерживается или не задокументировано.*  <br/> |
|**[сетчарсет](iconvertersession-setcharset.md)** <br/> |Задает необязательный набор символов, используемый преобразователем MAPI для преобразования MIME при преобразовании сообщения MAPI в поток MIME.  <br/> |
   
## <a name="remarks"></a>Примечания

Вызовите **сетенкодинг** , прежде чем использовать **мапитомиместм** для выполнения преобразования. 
  
## <a name="see-also"></a>См. также



[Сведения об API преобразования MAPI-MIME](about-the-mapi-mime-conversion-api.md)
  
[Константы MAPI](mapi-constants.md)

