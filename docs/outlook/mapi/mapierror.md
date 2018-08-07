---
title: MAPIERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIERROR
api_type:
- COM
ms.assetid: e04c2228-aa0a-4958-b5b2-6467e93ab613
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d0ddff638e26940ea74932a8a491455f67cc8dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809866"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Относится к**: Outlook 
  
Предоставляет подробные сведения об ошибке, обычно создаются в операционной системе, MAPI или поставщика услуг. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _MAPIERROR
{
  ULONG ulVersion;
  LPSTR lpszError;
  LPSTR lpszComponent;
  ULONG ulLowLevelError;
  ULONG ulContext;
} MAPIERROR, FAR * LPMAPIERROR;

```

## <a name="members"></a>Members

 **ulVersion**
  
> Номер версии структуры. Член **ulVersion** используется для расширения в будущем и должен иметь значение MAPI_ERROR_VERSION, которая в настоящее время имеет значение 0. 
    
 **lpszError**
  
> Указатель на строку с описанием ошибки. Эта строка будет в формате Юникод, если для параметра _ulFlags_ методу, в котором используется эта структура является значение MAPI_UNICODE. 
    
 **lpszComponent**
  
> Указатель на строку, которая описывает компонент, вызвавшей ошибку. Эта строка будет в формате Юникод, если для параметра _ulFlags_ методу, в котором используется эта структура является значение MAPI_UNICODE. 
    
 **ulLowLevelError**
  
> Значение ошибки низкого уровня, который используется только в том случае, если ошибка должно быть возвращено низкого уровня.
    
 **ulContext**
  
> Значение, представляющее расположение в компоненте, на который указывает **lpszComponent** элемент, который определяет, где произошла ошибка. 
    
## <a name="remarks"></a>Замечания

Структура **MAPIERROR** используется для описания сведения об ошибке. Клиенты и поставщиков услуг передать указатель на структуру **MAPIERROR** с помощью параметра _lppMAPIError_ метода [IMAPIProp::GetLastError](imapiprop-getlasterror.md) . **Код последней ошибки** возвращается сведения о возникшей на объект предыдущей ошибки. Вызывающие **GetLastError** освободить память для структуры **MAPIERROR** путем вызова метода [MAPIFreeBuffer](mapifreebuffer.md).
  
Член **lpszComponent** может использоваться для сопоставления файл справки компонента, если он существует. Поставщики услуг следует ограничить размер строки компонент до 30 символов, чтобы легко может отображаться в диалоговом окне. Член **ulContext** можно также ссылаться на раздел справки для наиболее распространенных ошибок. 
  
Так как поставщиков услуг не требуется предоставить подробные сведения об ошибке, клиенты не следует ожидать члены структуры **MAPIERROR** , возвращенных содержит допустимых данных. Тем не менее в минимальные MAPI настоятельно рекомендуется указать, что поставщики сведения в **lpszComponent** и **ulContext** члены. 
  
Дополнительные сведения об обработке ошибок в MAPI можно [Обработки ошибок](error-handling-in-mapi.md).
  
## <a name="see-also"></a>См. также



[IABLogon::GetLastError](iablogon-getlasterror.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIControl::GetLastError](imapicontrol-getlasterror.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISession::GetLastError](imapisession-getlasterror.md)
  
[IMAPISupport::GetLastError](imapisupport-getlasterror.md)
  
[IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md)
  
[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)
  
[IMAPITable::GetLastError](imapitable-getlasterror.md)
  
[IMsgServiceAdmin::GetLastError](imsgserviceadmin-getlasterror.md)
  
[IMSLogon::GetLastError](imslogon-getlasterror.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IProfAdmin::GetLastError](iprofadmin-getlasterror.md)
  
[IProviderAdmin::GetLastError](iprovideradmin-getlasterror.md)


[Структуры MAPI](mapi-structures.md)

