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
ms.openlocfilehash: 3edcb422eb0e3dd415d49c5e014c8b69095e7ec1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577207"
---
# <a name="iconvertersessionsetencoding"></a>IConverterSession::SetEncoding

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Инициализирует кодировку для использования при преобразовании.
  
```cpp
HRESULT IConverterSession:: SetEncoding ( 
     ENCODINGTYPE et 
);
```

## <a name="parameters"></a>Параметры

_et_
  
> Значение [ENCODINGTYPE](http://msdn.microsoft.com/en-us/library/aa374936%28VS.85%29.aspx) . Поддерживаются только следующие значения: 
    
   - IET_BASE64
   - IET_UUENCODE
   - IET_QP
   - IET_7BIT
   - IET_8BIT
    
## <a name="return-value"></a>������������ ��������

E_INVALIDARG
  
> Недопустимый тип кодировки передается.
    
## <a name="remarks"></a>Замечания

Вызовите **SetEncoding** перед использованием [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md) для выполнения преобразования. 
  
Используйте **SetEncoding** , чтобы установить кодировку только внешний сообщения из почтового элемента. Microsoft Outlook 2010 и Microsoft Outlook 2013 выберите кодировку для отдельных вложений. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.  <br/> |
   
## <a name="see-also"></a>См. также

- [IConverterSession : IUnknown](iconvertersessioniunknown.md)
- [IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
- [IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
- [IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
- [IConverterSession::SetCharSet](iconvertersession-setcharset.md)
- [IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
- [IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)
- [��������� MAPI](mapi-constants.md)

