---
title: иконвертерсессионсетчарсет
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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Задает необязательный набор символов, используемый преобразователем MAPI для преобразования MIME при преобразовании сообщения MAPI в поток MIME.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Параметры

 _фаппли_
  
> возврата Указывает, следует ли использовать для преобразования определенный набор знаков. Установите для этого параметра **значение true** , чтобы применить кодировку в последующих преобразованиях. Установите для этого параметра **значение false** , если вы больше не хотите применять определенный набор знаков и вернуться к значениям по умолчанию для последующих сообщений. 
    
 _хчарсет_
  
> возврата Дескриптор набора символов, как определено в мимеоле. h почты Windows. Укажите **значение NULL** , чтобы запретить применение определенного набора символов. Для значений, отличных от **null** , используйте функцию, например [мимеолежеткодепажечарсет](https://msdn.microsoft.com/library/ms714746%28VS.85%29.aspx) , для получения дескриптора для набора символов. 
    
 _ксетапплитипе_
  
> возврата Указывает способ применения набора символов для преобразования сообщения, как определено в мимеоле. h почты Windows.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов функции выполнен успешно.
    
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Мапимиме. cpp  <br/> |импортемлтоимессаже  <br/> |MFCMAPI использует Миметомапи для преобразования EML файла в сообщение MAPI.  <br/> |
|Мапимиме. cpp  <br/> |експортимессажетоемл  <br/> |MFCMAPI использует Мапитомиместм для преобразования сообщения MAPI в файл EML.  <br/> |
   
## <a name="see-also"></a>См. также



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

