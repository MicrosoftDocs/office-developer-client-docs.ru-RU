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
ms.openlocfilehash: e5f329ef0d3483683d5c94ed38c6631d86e77b93
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809083"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**Относится к**: Outlook 
  
Откроется раздел текущего профиля и возвращает указатель [IProfSect](iprofsectimapiprop.md) для дальнейшей доступа. 
  
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
  
> [in] Указатель на структуру [MAPIUID](mapiuid.md) , идентифицирующий раздела профиля. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к раздела профиля. Значение NULL вызывает параметр _lppProfSect_ для возврата указателя на стандартный интерфейс раздела профиля, **IProfSect**.
    
 _ulFlags_
  
> [in] Битовая маска, что управляет доступом к разделу профиль флаги. Можно задать следующие флажки:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** для возврата успешно, возможно перед профиль раздела доступными для клиента. Если в разделе профиль не поддерживается, последующие подключения к нему может вызвать ошибку. 
    
MAPI_FORCE_ACCESS
  
> Позволяет получить доступ к разделу профиля, которая не относится к поставщику.
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. По умолчанию разделы профилей открываются с разрешением только для чтения и клиенты не должны работать предполагается, что что назначено разрешение чтения и записи. 
    
 _lppProfSect_
  
> [out] Указатель на указатель на раздел профилей.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> В разделе профилей успешно открыт.
    
MAPI_E_NO_ACCESS 
  
> Предпринята попытка получить доступ к раздела профиля, для которого вызывающий не имеет разрешений.
    
MAPI_E_NOT_FOUND 
  
> В разделе запрошенные профиля не существует.
    
## <a name="remarks"></a>Замечания

Метод **IMAPISession::OpenProfileSection** открывает раздела профиля или объект, который поддерживает интерфейс **IProfSect** . Разделы профилей используются для чтения и записи данных в профиль сеанса. 
  
Нельзя использовать **OpenProfileSection** для открытия разделов профиля, собственных поставщиков отдельные службы, если не указать MAPI_FORCE_ACCESS с помощью параметра _ulFlags_ . 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Несколько клиентов могут открывать профиля с разрешением только для чтения, но только один клиент может открыть профиля с разрешением на чтение и запись. Если другой клиент имеет откройте попытаться открыть путем вызова **OpenProfileSection** с установленным флагом MAPI_MODIFY раздела профиля, вызов завершится с ошибкой, возвращая MAPI_E_NO_ACCESS. 
  
Происходит сбой операции open только для чтения, если разделе открыт для записи. 
  
Можно создать профиля путем вызова **OpenProfileSection** с флагом MAPI_MODIFY и несуществующий **MAPIUID** структуры с помощью параметра _lpUID_ . Не забудьте указать MAPI_MODIFY. Если необходимо задать _lpUID_ для указания на несуществующий **MAPIUID** и **OpenProfileSection** задано значение использовать режим по умолчанию доступа только для чтения, вызов завершится с ошибкой с MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)

