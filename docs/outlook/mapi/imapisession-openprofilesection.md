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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Открывает раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшего доступа. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Параметры

 _lpUID_
  
> [in] Указатель на структуру [MAPIUID,](mapiuid.md) которая определяет раздел профиля. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к разделу профиля. При передаче NULL параметр _lppProfSect_ возвращает указатель на стандартный интерфейс раздела профиля **IProfSect.**
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет доступом к разделу профиля. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** успешно возвращаться, возможно, до того, как раздел профиля будет полностью доступен вызываемому клиенту. Если раздел профиля не доступен, последующий вызов может привести к ошибке. 
    
MAPI_FORCE_ACCESS
  
> Разрешает доступ к разделу профиля, который не принадлежит поставщику.
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. По умолчанию разделы профилей открываются с разрешением только на чтение, и клиенты не должны работать при предположении, что разрешение на чтение и записи предоставлено. 
    
 _lppProfSect_
  
> [out] Указатель на указатель на раздел профиля.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Раздел профиля успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка доступа к разделу профиля, для которого у вызываемого пользователя недостаточно разрешений.
    
MAPI_E_NOT_FOUND 
  
> Запрашиваемая часть профиля не существует.
    
## <a name="remarks"></a>Примечания

Метод **IMAPISession::OpenProfileSection** открывает раздел профиля или объект, который поддерживает **интерфейс IProfSect.** Разделы профиля используются для чтения сведений из профиля сеанса и записи в него. 
  
**OpenProfileSection** нельзя использовать для открытия разделов профилей, которые принадлежат отдельным поставщикам услуг, если не указать MAPI_FORCE_ACCESS в параметре _ulFlags._ 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Несколько клиентов могут открывать раздел профиля с разрешением только на чтение, но только один клиент может открыть раздел профиля с разрешением на чтение и записи. Если другой клиент открывает раздел профиля, который вы попытаетесь открыть, вызывая **OpenProfileSection** с установленным флагом MAPI_MODIFY, вызов не удастся, и MAPI_E_NO_ACCESS. 
  
Операция открытия только для чтения не удастся, если раздел открыт для записи. 
  
Можно создать раздел профиля, вызывая **OpenProfileSection** с флагом MAPI_MODIFY и несущестукой структурой **MAPIUID** в параметре _lpUID._ Обязательно укажите MAPI_MODIFY. Если вы установите  _для lpUID_ значение, указывав на несущесту **mapIUID,** а **OpenProfileSection** будет использовать режим доступа только для чтения по умолчанию, вызов не будет MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

