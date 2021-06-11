---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419522"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Назначает новое имя в профиль.
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpszOldProfileName_
  
> [in] Указатель на текущее имя профиля для переименования.
    
 _lpszOldPassword_
  
> [in] Всегда NULL.
    
 _lpszNewProfileName_
  
> [in] Указатель на новое имя профиля для переименования.
    
 _ulUIParam_
  
> [in] Ручка родительского окна любых диалогов или окон, отображаемого этим методом. 
    
 _ulFlags_
  
> [in] Всегда NULL.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Профиль был успешно переименован.
    
MAPI_E_LOGON_FAILED 
  
> Пароль профиля неправильный.
    
MAPI_E_USER_CANCEL 
  
> Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне. 
    
## <a name="remarks"></a>Примечания

Метод **IProfAdmin::RenameProfile** назначает новое имя для профиля, если оно имеет его. Если профиль для переименования используется клиентом, когда называется **RenameProfile,** **renameProfile** пометит профиль и возвращает его S_OK вместо попытки операции переименования во время использования профиля. Когда профиль больше не используется, **RenameProfile** назначает ему новое имя. 
  
Старые и новые имена профиля могут иметь длину до 64 символов и включать следующие символы:
  
- Все буквы, включая символы акцента и символы подчеркнуть.
    
- Встроенные пробелы, но не ведущие и не ведущие.
    
_LpszPassword_ всегда должен быть NULL или указателем для строки нулевой длины. 
  
## <a name="see-also"></a>См. также



[IProfAdmin : IUnknown](iprofadminiunknown.md)

