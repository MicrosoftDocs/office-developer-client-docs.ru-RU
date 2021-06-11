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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Parameters

 _lpUid_
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая определяет открытый раздел профилей. Передача NULL для  _параметра lpUid_ открывает раздел профилей вызывающего пользователя. 
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют открытие раздела профилей. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** успешно возвращаться, возможно, до полного доступности раздела профилей для вызываемой. Если раздел профилей не доступен, последующий вызов объекта может привести к ошибке. 
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. По умолчанию объекты открываются только для чтения, и звонителям не следует работать с предположением о том, что разрешение на чтение и записи было предоставлено. 
    
 _lppProfileObj_
  
> [вышел] Указатель на указатель на открытый раздел профиля.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Раздел профилей был успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка изменить раздел профиля только для чтения или получить доступ к объекту, для которого вызываемая не имеет достаточных разрешений.
    
MAPI_E_NOT_FOUND 
  
> Раздел профиля, связанный с идентификатором записи, переданным в _lpEntryID, не существует._
    
MAPI_E_UNKNOWN_FLAGS 
  
> Использовались зарезервированные или неподтверченные флаги, поэтому операция не была завершена.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISupport::OpenProfileSection** реализован для всех объектов поддержки. Поставщики услуг и службы сообщений звонят **в OpenProfileSection,** чтобы открыть профильный раздел и получить указатель на реализацию интерфейса **IProfSect.** 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **OpenProfileSection** открывает разделы профилей только для чтения, если в параметре  _ulFlags_ не задан флаг MAPI_MODIFY, а разрешения достаточно. Установка этого флага не гарантирует разрешение на чтение и написание; разрешения, которые вы получили, зависят от уровня доступа и объекта. 
  
Если **OpenProfileSection** пытается открыть несуществовной раздел профиля только для чтения, он возвращает MAPI_E_NOT_FOUND. Если **OpenProfileSection** пытается открыть несуществовной раздел профиля в качестве чтения или записи, он создает раздел профилей и возвращает **указатель IProfSect.** 
  
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

