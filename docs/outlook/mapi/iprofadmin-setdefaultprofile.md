---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cf5060ba2113032fe1e13e5417590006808a53e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809514"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**Относится к**: Outlook 
  
Устанавливает или удаляет профиль клиента по умолчанию.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Параметры

 _lpszProfileName_
  
> [in] Указатель на имя профиля, который будет по умолчанию, или значение NULL. Установка _lpszProfileName_ значение NULL указывает, что **SetDefaultProfile** следует удалить существующий профиль по умолчанию, вследствие чего клиенту без значения по умолчанию. 
    
 _ulFlags_
  
> [in] Битовая маска флагов, определяющее тип string, на который указывает _lpszProfileName_. Можно задать следующий флаг:
    
MAPI_UNICODE 
  
> Имя профиля — в формате Юникод. Если флаг MAPI_UNICODE не установлен, в формате ANSI — это имя профиля.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Профиль по умолчанию было успешно установлено или удалено.
    
MAPI_E_NOT_FOUND 
  
> Указанный профиль не существует.
    
## <a name="remarks"></a>Замечания

Метод **IProfAdmin::SetDefaultProfile** устанавливает определенный профиль в качестве профиля по умолчанию клиента или очищает текущего профиля по умолчанию. Профиль по умолчанию является профиль, используемый автоматически при каждом клиент начинает сеанс MAPI. **SetDefaultProfile** также устанавливает свойство **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) нового профиля по умолчанию имеет значение TRUE.
  
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Чтобы начать сеанс с профилем по умолчанию, передача флаг MAPI_USE_DEFAULT функции [MAPILogonEx](mapilogonex.md) . 
  
## <a name="see-also"></a>См. также



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Каноническое свойство PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

