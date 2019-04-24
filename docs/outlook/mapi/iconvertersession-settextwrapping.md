---
title: Иконвертерсессионсеттекствраппинг
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetTextWrapping
api_type:
- COM
ms.assetid: 8674b288-43a3-6376-35ca-9dbaa3a1851e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a8a6546c38c629c193c1978998c95918943fe5c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336633"
---
# <a name="iconvertersessionsettextwrapping"></a>IConverterSession::SetTextWrapping

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Задает ширину обтекания текста для потока MIME, который будет возвращен преобразователем в [иконвертерсессион:: мапитомиместм](iconvertersession-mapitomimestm.md).
  
```cpp
HRESULT IConverterSession::SetTextWrapping ( 
    BOOL    fWrapText, 
    ULONG   ulWrapWidth 
);
```

## <a name="parameters"></a>Параметры

 *Фвраптекст* 
  
> возврата Указывает, следует ли переносить текст или нет.
    
 *Улврапвидс* 
  
> возврата Используемая ширина обтекания текста.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK
  
> Вызов выполнен успешно.
    
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
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetCharSet](iconvertersession-setcharset.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)


[Константы MAPI](mapi-constants.md)

