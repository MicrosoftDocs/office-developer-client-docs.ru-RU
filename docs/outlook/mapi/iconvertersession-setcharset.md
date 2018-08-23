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
ms.openlocfilehash: 69023d2c13037fb52a4d1dc4f7376efbd839aebc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581701"
---
# <a name="iconvertersessionsetcharset"></a>IConverterSession::SetCharSet

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает, что необязательный символ установить, MAPI на MIME конвертера использование при преобразовании сообщения MAPI в MIME-поток.
  
```cpp
HRESULT SetCharset( 
     BOOL fApply, 
     HCHARSET hcharset, 
     CSETAPPLYTYPE csetapplytype); 
```

## <a name="parameters"></a>Параметры

 _fApply_
  
> [in] Указывает, следует ли использовать определенные набор знаков для преобразования. Присвойте этому параметру значение **true,** Чтобы применить набор знаков в последующие преобразования. Присвойте этому параметру значение **false** , если вы больше не хотите применить любого заданного набора знаков и вернуться на значения по умолчанию для последующих сообщений. 
    
 _hcharset_
  
> [in] Дескриптор кодировку, как определено в mimeole.h почты Windows. Укажите **значение null,** чтобы указать, что не нужно применить любого заданного набора знаков. Для значений, **значение null** используйте функции [MimeOleGetCodePageCharset](http://msdn.microsoft.com/en-us/library/ms714746%28VS.85%29.aspx) для получения дескриптора набор символов. 
    
 _csetapplytype_
  
> [in] Указывает, как применять набор символов для преобразования в сообщении, как определено в mimeole.h почты Windows.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK
  
> Вызов функции выполнен успешно.
    
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MapiMime.cpp  <br/> |ImportEMLToIMessage  <br/> |Mfcmapi (en) используется MimeToMAPI для преобразования EML-файла в сообщение MAPI.  <br/> |
|MapiMime.cpp  <br/> |ExportIMessageToEML  <br/> |Mfcmapi (en) используется MAPIToMIMEStm для преобразования MAPI сообщения EML-файла.  <br/> |
   
## <a name="see-also"></a>См. также



[IConverterSession : IUnknown](iconvertersessioniunknown.md)
  
[IConverterSession::MAPIToMIMEStm](iconvertersession-mapitomimestm.md)
  
[IConverterSession::MIMEToMAPI](iconvertersession-mimetomapi.md)
  
[IConverterSession::SetAdrBook](iconvertersession-setadrbook.md)
  
[IConverterSession::SetEncoding](iconvertersession-setencoding.md)
  
[IConverterSession::SetSaveFormat](iconvertersession-setsaveformat.md)
  
[IConverterSession::SetTextWrapping](iconvertersession-settextwrapping.md)

