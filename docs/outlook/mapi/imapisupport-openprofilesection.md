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
ms.openlocfilehash: 2e1f546d33d4781f60df56b12fce437d1e7bd675
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588225"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Откроется раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Параметры

 _lpUid_
  
> [in] Указатель на структуру [MAPIUID](mapiuid.md) , который определяет раздел профилей, чтобы открыть. Значение NULL для параметра _lpUid_ откроется раздел профилей вызывающего абонента. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, который управляет способа открытия раздела профиля. Можно задать следующие флажки:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** для возврата успешно, возможно перед профиль раздел полностью доступен для вызова. Если недоступен в разделе профилей, вызов последующих объектов может привести к ошибке. 
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. По умолчанию объекты открываются только для чтения и звонящие не должны работать предполагается, что что назначено разрешение чтения и записи. 
    
 _lppProfileObj_
  
> [out] Указатель на указатель на раздел открыт профилей.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> В разделе профилей успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка изменения раздела профиля только для чтения или для доступа к объекту, для которого вызывающий не имеет разрешений.
    
MAPI_E_NOT_FOUND 
  
> Раздел профиля, связанный с идентификатором записи, переданные в _lpEntryID_не существует.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Зарезервированные или неподдерживаемые флаги использовались и, таким образом, операция не завершена.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISupport::OpenProfileSection** применяется для всех объектов поддержки. Поставщики службы и службы сообщений вызов **OpenProfileSection** открытие раздела профиля и получить указатель на его реализация интерфейса **IProfSect** . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

 **OpenProfileSection** открывает разделах профиля с доступом только для чтения, если не задан флаг MAPI_MODIFY в параметре _ulFlags_ и разрешение является достаточным. Этот флаг установлен не гарантирует разрешение на чтение и запись. разрешения, которые будут предоставлены зависят от вам уровень доступа и объект. 
  
Если **OpenProfileSection** пытается открыть несуществующий профилей раздел только для чтения, возвращает MAPI_E_NOT_FOUND. Если **OpenProfileSection** пытается открыть несуществующий профилей раздел для чтения и записи, он создает в разделе профилей и возвращает указатель **IProfSect** . 
  
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

