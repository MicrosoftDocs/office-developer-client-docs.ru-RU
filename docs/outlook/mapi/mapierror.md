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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет подробные сведения об ошибке, обычно создаваемой операционной системой, MAPI или поставщиком услуг. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
   
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

 **Улверсион**
  
> Номер версии структуры. Элемент **улверсион** используется для последующего расширения и должен иметь значение мапи_еррор_версион, которое в настоящее время определено как нулевое. 
    
 **Лпсзеррор**
  
> Указатель на строку с описанием ошибки. Эта строка будет иметь формат Юникод, если параметр _ulFlags_ для метода, в котором используется эта структура, имеет значение мапи_уникоде. 
    
 **Лпсзкомпонент**
  
> Указатель на строку, описывающую компонент, который сформировал ошибку. Эта строка будет иметь формат Юникод, если параметр _ulFlags_ для метода, в котором используется эта структура, имеет значение мапи_уникоде. 
    
 **Улловлевелеррор**
  
> Значение ошибки на низком уровне, используемое только в том случае, если возвращаемая ошибка является нижним уровнем.
    
 **Улконтекст**
  
> Значение, представляющее расположение в компоненте, на которое указывает элемент **лпсзкомпонент** , определяющий место возникновения ошибки. 
    
## <a name="remarks"></a>Примечания

Структура **мапиеррор** используется для описания сведений об ошибках. Клиенты и поставщики услуг передают указатель на структуру **мапиеррор** в параметре _лппмапиеррор_ метода [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) . **GetLastError** возвращает сведения о предыдущей ошибке, возникшей в объекте. Вызывающие абоненты **GetLastError** освобождают память для структуры **мапиеррор** , вызывая [мапифрибуффер](mapifreebuffer.md).
  
Элемент **лпсзкомпонент** можно использовать для сопоставления файла справки компонента, если он существует. Поставщики услуг должны ограничить размер строки компонента до 30 символов, чтобы ее можно было легко отобразить в диалоговом окне. Элемент **улконтекст** также можно использовать для ссылки на раздел справки в Интернете для распространенных ошибок. 
  
Так как поставщики услуг не обязаны предоставлять подробные сведения об ошибке, клиенты не должны ожидать, что ни один из членов структуры **мапиеррор** , возвращаемых для хранения допустимых данных. Тем не менее, по крайней мере в MAPI настоятельно рекомендуется, чтобы поставщики задают сведения в элементах **лпсзкомпонент** и **улконтекст** . 
  
Дополнительные сведения об обработке ошибок в MAPI можно найти в разделе [Обработка ошибок](error-handling-in-mapi.md).
  
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

