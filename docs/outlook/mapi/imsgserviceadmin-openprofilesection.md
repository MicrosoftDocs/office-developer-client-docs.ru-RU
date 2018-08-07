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
ms.openlocfilehash: 954dc467a0d83466b1b16a3ead5b6404d372ecab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809355"
---
# <a name="imsgserviceadminopenprofilesection"></a>IMsgServiceAdmin::OpenProfileSection

  
  
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
  
> Указатель на структуру [MAPIUID](mapiuid.md) , идентифицирующий раздела профиля. 
    
 _lpInterface_
  
> [in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к раздела профиля. Передача значение NULL, приводит к указатель на его стандартный интерфейс, возвращаемых в параметре _lppProfSect_ . Стандартный интерфейс для профиля — **IProfSect**.
    
 _ulFlags_
  
> [in] Битовая маска, что управляет доступом к разделу профиль флаги. Можно задать следующие флажки:
    
MAPI_DEFERRED_ERRORS 
  
> Позволяет **OpenProfileSection** для возврата успешно, возможно перед профиль раздела доступными для клиента. Если в разделе профиль не поддерживается, последующие подключения к нему может вызвать ошибку. 
    
MAPI_MODIFY 
  
> Запросы на разрешение чтения и записи. По умолчанию разделы профилей открываются с разрешением только для чтения и клиенты не должны работать предполагается, что что назначено разрешение чтения и записи. 
    
MAPI_FORCE_ACCESS
  
> Разрешает доступ всех разделах профилей, даже теми, поставщиками отдельные службы.
    
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

Метод **IMsgServiceAdmin::OpenProfileSection** открывает раздел профиля, объект, который поддерживает интерфейс [IProfSect](iprofsectimapiprop.md) . Разделы профилей используются для чтения и записи данных в профиль сеанса. 
  
 **OpenProfileSection** не может использоваться для открытия разделов профиля, принадлежащие отдельные службы поставщиков, если не используется MAPI_FORCE_ACCESS. 
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Несколько клиентов могут открывать профиля с разрешением только для чтения, но только один клиент может открыть профиля с разрешением на чтение и запись. Если другой клиент имеет откройте попытаться открыть путем вызова **OpenProfileSection** с установленным флагом MAPI_MODIFY раздела профиля, вызов завершится с ошибкой, возвращая MAPI_E_NO_ACCESS. 
  
Происходит сбой операции open только для чтения, если разделе открыт для записи. 
  
Можно создать профиля путем вызова **OpenProfileSection** с флагом MAPI_MODIFY и несуществующий [MAPIUID](mapiuid.md) структуры с помощью параметра _lpUID_ . Убедитесь, что вы установили MAPI_MODIFY. Если необходимо задать _lpUID_ для указания на несуществующий **MAPIUID** и **OpenProfileSection** задано значение использовать режим по умолчанию доступа только для чтения, вызов завершится с ошибкой с MAPI_E_NOT_FOUND. 
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |OpenProfileSection  <br/> |Mfcmapi (en) использует метод **IMsgServiceAdmin::OpenProfileSection** для открытия профиля.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

