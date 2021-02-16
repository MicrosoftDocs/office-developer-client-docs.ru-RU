---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411388"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Параметры

 _lpUid_
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая определяет открываемую секцию профиля. Передача NULL для  _параметра lpUid_ открывает раздел профиля вызывающего. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет открытием раздела профиля. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** успешно возвращаться, возможно, до того, как раздел профиля будет полностью доступен вызываемой. Если раздел профиля не доступен, последующий вызов объекта может привести к ошибке. 
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. По умолчанию объекты открываются как объекты только для чтения, и вызывающим не следует работать при предположении, что разрешение на чтение и записи предоставлено. 
    
 _lppProfileObj_
  
> [out] Указатель на указатель на открытый раздел профиля.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Раздел профиля успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка изменить раздел профиля, доступный только для чтения, или получить доступ к объекту, у которого у вызываемого объекта недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> Раздел профиля, связанный с идентификатором записи, переданным _в lpEntryID, не существует._
    
MAPI_E_UNKNOWN_FLAGS 
  
> Использовались зарезервированные или неподтверченные флаги, поэтому операция не была завершена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::OpenProfileSection** реализован для всех объектов поддержки. Поставщики услуг и службы сообщений вызвать **OpenProfileSection,** чтобы открыть раздел профиля и получить указатель на реализацию интерфейса **IProfSect.** 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **OpenProfileSection** открывает разделы профиля только для чтения, если в параметре  _ulFlags_ не установлен флаг MAPI_MODIFY, а разрешения достаточно. Установка этого флага не гарантирует разрешение на чтение и записи; предоставленные разрешения зависят от уровня доступа и объекта. 
  
Если **OpenProfileSection** пытается открыть несущестуный раздел профиля только для чтения, он возвращает MAPI_E_NOT_FOUND. Если **OpenProfileSection** пытается открыть несущестуный раздел профиля как чтение и записи, он создает раздел профиля и возвращает **указатель IProfSect.** 
  
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

