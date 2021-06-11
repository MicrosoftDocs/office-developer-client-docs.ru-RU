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
ms.openlocfilehash: 682e75c4e0a2f60dbd46a13b0b737ca4a8e18f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409148"
---
# <a name="mapierror"></a>MAPIERROR

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет подробные сведения об ошибке, обычно генерируемой операционной системой, MAPI или поставщиком услуг. 
  
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

## <a name="members"></a>"Участники"

 **ulVersion**
  
> Номер версии структуры. Член **ulVersion** используется для будущего расширения и должен быть задат MAPI_ERROR_VERSION, который в настоящее время определяется как ноль. 
    
 **lpszError**
  
> Указатель на строку, описываемую ошибку. Эта строка будет в формате Юникод, если параметр  _ulFlags_ для метода, в котором используется эта структура, MAPI_UNICODE. 
    
 **lpszComponent**
  
> Указатель на строку, описываемую компонентом, который вызвал ошибку. Эта строка будет в формате Юникод, если параметр  _ulFlags_ для метода, в котором используется эта структура, MAPI_UNICODE. 
    
 **ulLowLevelError**
  
> Значение ошибки низкого уровня, которое используется только при возврате ошибки, является низкоуровневой.
    
 **ulContext**
  
> Значение, которое представляет расположение в компоненте, на которое указывает член **lpszComponent,** который определяет место, где произошла ошибка. 
    
## <a name="remarks"></a>Примечания

Структура **MAPIERROR** используется для описания сведений об ошибках. Клиенты и поставщики услуг передают указатель структуре **MAPIERROR** в _параметре lppMAPIError_ метода [IMAPIProp::GetLastError.](imapiprop-getlasterror.md) **GetLastError возвращает** сведения о предыдущей ошибке, которая произошла в объекте. Вызыватели **GetLastError** освободить память для **структуры MAPIERROR,** позвонив [MAPIFreeBuffer](mapifreebuffer.md).
  
Элемент **lpszComponent** можно использовать для картографии файла справки компонента, если он существует. Поставщики услуг должны ограничить размер строки компонентов 30 символами, чтобы она легко отображалась в диалоговом окне. Член **ulContext** также может использоваться для ссылки на раздел справки в Интернете для распространенных ошибок. 
  
Поскольку поставщики услуг не обязаны предоставлять подробные сведения об ошибках, клиенты не должны ожидать, что кто-либо из членов структуры **MAPIERROR,** которые возвращаются, будет содержать допустимые данные. Однако как минимум MAPI настоятельно рекомендует поставщикам указывать сведения в **членах lpszComponent** и **ulContext.** 
  
Дополнительные сведения об обработке ошибок в MAPI см. в [дополнительных сведениях об обработке ошибок.](error-handling-in-mapi.md)
  
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

