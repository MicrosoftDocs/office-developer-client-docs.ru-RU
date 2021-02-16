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
  
> Указатель на структуру [MAPIUID,](mapiuid.md) которая определяет раздел профиля. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса ( IID), который представляет интерфейс, который будет использоваться для доступа к разделу профиля. Передача NULL приводит к возвращению указателя на стандартный интерфейс в _параметре lppProfSect._ Стандартным интерфейсом для раздела профиля **является IProfSect.**
    
 _ulFlags_
  
> [in] Битоваяmas флагов, которая управляет доступом к разделу профиля. Можно установить следующие флаги:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** успешно возвращаться, возможно, до того, как раздел профиля будет полностью доступен вызываемому клиенту. Если раздел профиля не доступен, последующий вызов может вызвать ошибку. 
    
MAPI_MODIFY 
  
> Запрашивает разрешение на чтение и записи. По умолчанию разделы профилей открываются с разрешением только на чтение, и клиенты не должны работать при предположении, что разрешение на чтение и записи предоставлено. 
    
MAPI_FORCE_ACCESS
  
> Разрешает доступ ко всем разделам профилей, даже тем, которые принадлежат отдельным поставщикам услуг.
    
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

Метод **IMsgServiceAdmin::OpenProfileSection** открывает раздел профиля, объект, который поддерживает [интерфейс IProfSect.](iprofsectimapiprop.md) Разделы профиля используются для чтения сведений из профиля сеанса и записи в него. 
  
 **OpenProfileSection** нельзя использовать для открытия разделов профилей, владельцем MAPI_FORCE_ACCESS отдельных поставщиков услуг. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Несколько клиентов могут открыть раздел профиля с разрешением только на чтение, но только один клиент может открыть раздел профиля с разрешением на чтение и написание. Если другой клиент открывает раздел профиля, который вы попытаетесь открыть, вызывая **OpenProfileSection** с установленным флагом MAPI_MODIFY, вызов не удастся, и MAPI_E_NO_ACCESS. 
  
Операция открытия только для чтения не удастся, если раздел открыт для записи. 
  
Вы можете создать раздел профиля, вызывая **OpenProfileSection** с флагом MAPI_MODIFY и несущестукой структурой [MAPIUID](mapiuid.md) в параметре _lpUID._ Обязательно укажите MAPI_MODIFY. Если вы установите  _для lpUID_ значение, указывав на несущесту **mapIUID,** а **OpenProfileSection** будет использовать режим доступа только для чтения по умолчанию, вызов не будет MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |MFCMAPI использует метод **IMsgServiceAdmin::OpenProfileSection** для открытия раздела профиля.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

