---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439921"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Parameters

 _lpUID_
  
> [in] Указатель на [структуру MAPIUID,](mapiuid.md) идентифицируемую в разделе профилей. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к разделу профилей. Передача NULL заставляет _параметр lppProfSect_ возвращать указатель в стандартный интерфейс **профиля IProfSect.**
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют доступ к разделу профилей. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** успешно возвращаться, возможно, до того, как профильный раздел будет полностью доступен клиенту вызова. Если раздел профилей не доступен, последующий вызов может привести к ошибке. 
    
MAPI_FORCE_ACCESS
  
> Разрешает доступ к разделу профилей, который не принадлежит поставщику.
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. По умолчанию разделы профилей открываются с разрешения только для чтения, и клиенты не должны работать с предположением о том, что разрешение на чтение и записи было предоставлено. 
    
 _lppProfSect_
  
> [вышел] Указатель на указатель в разделе профиль.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Раздел профилей был успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Была предпринята попытка получить доступ к разделу профилей, для которого вызываемая не имеет достаточных разрешений.
    
MAPI_E_NOT_FOUND 
  
> Запрашиваемая часть профиля не существует.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::OpenProfileSection** открывает профильный раздел или объект, который поддерживает **интерфейс IProfSect.** Разделы профилей используются для чтения сведений из профиля сеанса и записи в него. 
  
Вы не можете использовать **OpenProfileSection** для открытия разделов профилей, которые принадлежат отдельным поставщикам услуг, если вы не MAPI_FORCE_ACCESS в параметре _ulFlags._ 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Несколько клиентов могут открыть раздел профилей с разрешения только для чтения, но только один клиент может открыть раздел профилей с разрешения на чтение и написание. Если у другого клиента открыт раздел профилей, который вы попытаетесь открыть, позвонив **в OpenProfileSection** с набором флага MAPI_MODIFY, вызов не удастся, возвращая MAPI_E_NO_ACCESS. 
  
Открытая операция только для чтения сбой, если раздел открыт для записи. 
  
Вы можете создать раздел профилей, позвонив **в OpenProfileSection** с флагом MAPI_MODIFY и несуществовацией **структуры MAPIUID** в параметре _lpUID._ Убедитесь, что вы указываете MAPI_MODIFY. Если  _установлено, что lpUID_ будет указать на несуществовую **MAPIUID,** а **OpenProfileSection** будет использовать режим доступа только для чтения по умолчанию, вызов сбой MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

