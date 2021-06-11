---
title: IMsgServiceAdminOpenProfileSection
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.OpenProfileSection
api_type:
- COM
ms.assetid: 7f24910a-e14e-44a1-8477-d8968130ba74
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 32ebdea3a594b5adf5d46dc081098d3628ae145b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437114"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
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
  
> Указатель на [структуру MAPIUID,](mapiuid.md) идентифицируемую в разделе профилей. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (IID), который представляет интерфейс, используемый для доступа к разделу профилей. Передача NULL приводит к возвращению указателя к стандартному интерфейсу в _параметре lppProfSect._ Стандартным интерфейсом для раздела профилей **является IProfSect**.
    
 _ulFlags_
  
> [in] Битмаска флагов, которые контролируют доступ к разделу профилей. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** успешно возвращаться, возможно, до того, как профильный раздел будет полностью доступен клиенту вызова. Если раздел профилей не доступен, последующий вызов может привести к ошибке. 
    
MAPI_MODIFY 
  
> Запросы на чтение и написание разрешений. По умолчанию разделы профилей открываются с разрешения только для чтения, и клиенты не должны работать с предположением о том, что разрешение на чтение и записи было предоставлено. 
    
MAPI_FORCE_ACCESS
  
> Позволяет получить доступ ко всем разделам профилей, даже к разделам, которые принадлежат отдельным поставщикам услуг.
    
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

Метод **IMsgServiceAdmin::OpenProfileSection** открывает профильный раздел, объект, который поддерживает [интерфейс IProfSect.](iprofsectimapiprop.md) Разделы профилей используются для чтения сведений из профиля сеанса и записи в него. 
  
 **OpenProfileSection** нельзя использовать для открытия разделов профилей, которые принадлежат отдельным поставщикам услуг, если MAPI_FORCE_ACCESS не используется. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Несколько клиентов могут открыть раздел профилей с разрешения только для чтения, но только один клиент может открыть раздел профилей с разрешения на чтение и написание. Если у другого клиента открыт раздел профилей, который вы попытаетесь открыть, позвонив **в OpenProfileSection** с набором флага MAPI_MODIFY, вызов не удастся, возвращая MAPI_E_NO_ACCESS. 
  
Открытая операция только для чтения сбой, если раздел открыт для записи. 
  
Вы можете создать раздел профилей, позвонив **в OpenProfileSection** с флагом MAPI_MODIFY и несуществовацией [структуры MAPIUID](mapiuid.md) в параметре _lpUID._ Обязательно укажите MAPI_MODIFY. Если  _установлено, что lpUID_ будет указать на несуществовую **MAPIUID,** а **OpenProfileSection** будет использовать режим доступа только для чтения по умолчанию, вызов сбой MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI использует **метод IMsgServiceAdmin::OpenProfileSection** для открытия раздела профилей.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

